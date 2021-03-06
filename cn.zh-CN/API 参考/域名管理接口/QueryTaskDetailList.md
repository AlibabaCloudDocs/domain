# QueryTaskDetailList

调用QueryTaskDetailList分页查询指定域名任务的详情列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryTaskDetailList&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryTaskDetailList|系统规定参数。取值：**QueryTaskDetailList**。 |
|PageNum|Integer|是|1|分页页码。 |
|PageSize|Integer|是|1|分页大小，最大值为**1000**。 |
|TaskNo|String|是|75addb07-28a3-450e-b5ec-test|任务编号。 |
|TaskStatus|Integer|否|2|任务状态。取值：

 -   **0**：等待执行。
-   **1**：执行中。
-   **2**：成功。
-   **3**：失败。 |
|InstanceId|String|否|S20179H1BBI9test|域名实例编号。 |
|DomainName|String|否|example.com|域名。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.0|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPageNum|Integer|1|当前页码。 |
|Data|Array of TaskDetail| |任务列表。 |
|TaskDetail| | | |
|CreateTime|String|2018-01-25 20:46:57|任务创建时间。 |
|DomainName|String|example.com|域名。 |
|ErrorMsg|String|The operation is successful.|任务执行失败消息。 |
|InstanceId|String|S20179H1BBI9test|域名实例编号。 |
|TaskDetailNo|String|75addb07-28a3-450e-b5ec-test|任务详情编号。 |
|TaskNo|String|60d6e201-8ee5-47ab-8fdc-test|任务编号。 |
|TaskResult|String|12345|任务执行结果，用于记录部分任务类型执行后的任务结果。 |
|TaskStatus|String|EXECUTE\_SUCCESS|任务状态。取值：

 -   **WAITING\_EXECUTE**：等待执行。
-   **EXECUTING**：执行中。
-   **EXECUTE\_SUCCESS**：执行成功。
-   **EXECUTE\_FAILURE**：执行失败。 |
|TaskStatusCode|Integer|2|任务状态码。取值：

 -   **0**：等待执行。
-   **1**：执行中。
-   **2**：执行成功。
-   **3**：执行失败。 |
|TaskType|String|ORDER\_RENEW|任务类型。取值：

 -   **CHG\_HOLDER**：修改所有者信息。
-   **CHG\_DNS**：修改DNS。
-   **SET\_WHOIS\_PROTECT**：设置隐私保护。
-   **UPDATE\_ADMIN\_CONTACT**：修改管理者信息。
-   **UPDATE\_BILLING\_CONTACT**：修改付费者信息。
-   **UPDATE\_TECH\_CONTACT**：修改技术者信息。
-   **SET\_UPDATE\_PROHIBITED**：设置域名安全锁。
-   **SET\_TRANSFER\_PROHIBITED**：设置域名转移锁。
-   **ORDER\_ACTIVATE**：创建注册订单。
-   **ORDER\_RENEW**：创建续费订单。
-   **ORDER\_REDEEM**：创建赎回订单。
-   **CREATE\_DNSHOST**：创建DNS host。
-   **UPDATE\_DNSHOST**：更新DNS host。
-   **SYNC\_DNSHOST**：同步DNS host。 |
|TaskTypeDescription|String|创建续费订单|任务类型描述。 |
|TryCount|Integer|0|任务详情重试次数。 |
|UpdateTime|String|2018-01-25 20:47:01|最近一次任务详情执行时间。 |
|NextPage|Boolean|true|是否有下一页。 |
|PageSize|Integer|2|分页大小。 |
|PrePage|Boolean|false|是否有上一页。 |
|RequestId|String|6A2320E4-D870-49C9-A6DC-test|唯一请求识别码。 |
|TotalItemNum|Integer|1|总数。 |
|TotalPageNum|Integer|1|总页数。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=QueryTaskDetailList
&PageNum=1
&PageSize=1
&TaskNo=75addb07-28a3-450e-b5ec-test
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PrePage>false</PrePage>
<CurrentPageNum>1</CurrentPageNum>
<PageSize>2</PageSize>
<RequestId>6A2320E4-D870-49C9-A6DC-test</RequestId>
<TotalPageNum>1</TotalPageNum>
<Data>
    <TaskDetail>
        <DomainName>example.com</DomainName>
        <InstanceId>S20179H1BBI9test</InstanceId>
        <TaskNo>60d6e201-8ee5-47ab-8fdc-test</TaskNo>
        <TaskStatusCode>2</TaskStatusCode>
        <CreateTime>2018-01-25 20:46:57</CreateTime>
        <ErrorMsg>The operation is successful.</ErrorMsg>
        <TaskStatus>EXECUTE_SUCCESS</TaskStatus>
        <TaskTypeDescription>创建续费订单</TaskTypeDescription>
        <TryCount>0</TryCount>
        <TaskType>ORDER_RENEW</TaskType>
        <UpdateTime>2018-01-25 20:47:01</UpdateTime>
        <TaskResult>12345</TaskResult>
        <TaskDetailNo>75addb07-28a3-450e-b5ec-test</TaskDetailNo>
    </TaskDetail>
</Data>
<TotalItemNum>1</TotalItemNum>
<NextPage>true</NextPage>
```

`JSON` 格式

```
{
    "PrePage": false,
    "CurrentPageNum": 1,
    "PageSize": 2,
    "RequestId": "6A2320E4-D870-49C9-A6DC-test",
    "TotalPageNum": 1,
    "Data": {
        "TaskDetail": {
            "DomainName": "example.com",
            "InstanceId": "S20179H1BBI9test",
            "TaskNo": "60d6e201-8ee5-47ab-8fdc-test",
            "TaskStatusCode": 2,
            "CreateTime": "2018-01-25 20:46:57",
            "ErrorMsg": "The operation is successful.",
            "TaskStatus": "EXECUTE_SUCCESS",
            "TaskTypeDescription": "创建续费订单",
            "TryCount": 0,
            "TaskType": "ORDER_RENEW",
            "UpdateTime": "2018-01-25 20:47:01",
            "TaskResult": 12345,
            "TaskDetailNo": "75addb07-28a3-450e-b5ec-test"
        }
    },
    "TotalItemNum": 1,
    "NextPage": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

