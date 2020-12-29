# PollTaskResult

调用PollTaskResult获取已经执行完成（包含执行成功和执行失败并超过重试次数）的域名任务详情列表。

## API描述

该接口需要配合[AcknowledgeTaskResult](~~69366~~)确认任务结果。任务结果确认后，对应任务记录将无法从该接口查询到。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=PollTaskResult&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|PollTaskResult|系统规定参数。取值：**PollTaskResult**。 |
|PageNum|Integer|是|1|页码。 |
|PageSize|Integer|是|20|分页大小。最大值为**1000**。 |
|TaskResultStatus|Integer|否|2|任务结果类型，取值：

 -   **2**：成功。
-   **3**：失败。 |
|InstanceId|String|否|S20181T0WLI85212|域名实例编号。

 信息模板创建成功后由系统自动生成，您可以调用[QueryRegistrantProfiles](~~67701~~)接口查询信息模板编号。 |
|TaskNo|String|否|75addb07-28a3-450e-b5ec-test|任务编号。 |
|DomainName|String|否|example.com|域名。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPageNum|Integer|1|当前页码。 |
|Data|Array of TaskDetail| |任务详情列表。 |
|TaskDetail| | | |
|CreateTime|String|2018-03-26 15:08:20|任务创建时间。 |
|DomainName|String|example.com|域名。 |
|ErrorMsg|String|The operation is successful.|任务执行失败消息。 |
|InstanceId|String|S201817141000000|域名实例编号。 |
|TaskDetailNo|String|15fee9d10d514bada66bd08c5723c583|任务详情编号。 |
|TaskNo|String|b95bc334-f7d8-4f39-8a62-4c4302a243d8|任务编号。 |
|TaskResult|String|test|任务结果。 |
|TaskStatus|String|EXECUTE\_SUCCESS|任务状态。可能值：

 -   **WAITING\_EXECUTE**：等待执行。
-   **EXECUTING**：执行中。
-   **EXECUTE\_SUCCESS**：执行成功。
-   **EXECUTE\_FAILURE**：执行失败。 |
|TaskStatusCode|Integer|2|任务状态码。可能值：

 -   **0**：等待执行。
-   **1**：执行中。
-   **2**：执行成功。
-   **3**：执行失败。 |
|TaskType|String|CHG\_DNS|任务类型。 |
|TaskTypeDescription|String|修改DNS|任务类型描述。如果切换了Lang参数，该字段会切换语言。 |
|TryCount|Integer|0|任务详情重试次数。 |
|UpdateTime|String|2018-03-26 15:22:18|最近一次任务详情执行时间。 |
|NextPage|Boolean|false|是否有下一页。 |
|PageSize|Integer|1|分页大小。 |
|PrePage|Boolean|false|是否有上一页。 |
|RequestId|String|E879DC07-38EE-4408-9F33-73B30CD965CD|唯一请求识别码。 |
|TotalItemNum|Integer|10|总条数。 |
|TotalPageNum|Integer|10|总页数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=PollTaskResult
&PageNum=1
&PageSize=20
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PollTaskResultResponse>
    <Data>
        <TaskDetail>
            <TryCount>0</TryCount>
            <TaskDetailNo>15fee9d10d514bada66bd08c5723c583</TaskDetailNo>
            <TaskNo>b95bc334-f7d8-4f39-8a62-4c4302a243d8</TaskNo>
            <CreateTime>2018-03-26 15:08:20</CreateTime>
            <InstanceId>S201817141000000</InstanceId>
            <UpdateTime>2018-03-26 15:22:18</UpdateTime>
            <TaskStatus>EXECUTE_SUCCESS</TaskStatus>
            <DomainName>test.com</DomainName>
            <TaskTypeDescription>DNS Modification</TaskTypeDescription>
            <TaskStatusCode>2</TaskStatusCode>
            <ErrorMsg>The operation is successful.</ErrorMsg>
            <TaskType>CHG_DNS</TaskType>
        </TaskDetail>
    </Data>
    <TotalItemNum>10</TotalItemNum>
    <PageSize>1</PageSize>
    <CurrentPageNum>1</CurrentPageNum>
    <RequestId>C2CB6161-7971-4EB6-BC16-92A2BA3816D9</RequestId>
    <TotalPageNum>10</TotalPageNum>
</PollTaskResultResponse>
```

`JSON` 格式

```
{
    "CurrentPageNum":1,
    "Data":{
        "TaskDetail":[{
            "CreateTime":"2018-03-26 15:08:20",
            "DomainName":"test.com",
            "ErrorMsg":"The operation is successful.",
            "InstanceId":"S201817141000000",
            "TaskDetailNo":"15fee9d10d514bada66bd08c5723c583",
            "TaskNo":"b95bc334-f7d8-4f39-8a62-4c4302a243d8",
            "TaskStatus":"EXECUTE_SUCCESS",
            "TaskStatusCode":2,
            "TaskType":"CHG_DNS",
            "TaskTypeDescription":"DNS Modification",
            "TryCount":0,
            "UpdateTime":"2018-03-26 15:22:18"
        }]
    },
    "PageSize":1,
    "RequestId":"E879DC07-38EE-4408-9F33-73B30CD965CD",
    "TotalItemNum":10,
    "TotalPageNum":10
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

