# PollTaskResult

Queries the details about completed domain name tasks, including successful tasks and tasks that still failed after the maximum number of attempts.

## Description

You can call the [AcknowledgeTaskResult](~~69366~~) operation to query the running result of a domain name task. After you query the running result of a domain name task, you cannot call the PollTaskResult operation to query this task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=PollTaskResult&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|PollTaskResult|The operation that you want to perform. Set the value to **PollTaskResult**. |
|PageNum|Integer|Yes|1|The number of the page to return. |
|PageSize|Integer|Yes|20|The number of entries to return on each page. Maximum value: **1000**. |
|TaskResultStatus|Integer|No|2|The running result of the task. Valid values:

-   **2**: The task is run.
-   **3**: The task fails to be run. |
|InstanceId|String|No|S20181T0WLI85212|The instance ID of the domain name.

The system automatically generates the instance ID after a registrant profile is created. You can call the [QueryRegistrantProfiles](~~67701~~)operation to query the ID of a created registrant profile. |
|TaskNo|String|No|75addb07-28a3-450e-b5ec-test|The ID of the task. |
|DomainName|String|No|example.com|The domain name. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used for the query. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CurrentPageNum|Integer|1|The page number of the returned page. |
|Data|Array of TaskDetail| |The details of the tasks. |
|TaskDetail| | | |
|CreateTime|String|2018-03-26 15:08:20|The time when the task was created. |
|DomainName|String|example.com|The domain name. |
|ErrorMsg|String|The operation is successful.|The message that indicates the running result of the task. |
|InstanceId|String|S201817141000000|The instance ID of the domain name. |
|TaskDetailNo|String|15fee9d10d514bada66bd08c5723c583|The ID of the task details. |
|TaskNo|String|b95bc334-f7d8-4f39-8a62-4c4302a243d8|The ID of the task. |
|TaskResult|String|test|The running result of the task. |
|TaskStatus|String|EXECUTE\_SUCCESS|The status of the task. Valid values:

-   **WAITING\_EXECUTE**: The task is waiting to be run.
-   **EXECUTING**: The task is being run.
-   **EXECUTE\_SUCCESS**: The task is run.
-   **EXECUTE\_FAILURE**: The task fails to be run. |
|TaskStatusCode|Integer|2|The status code of the task. Valid values:

-   **0**: The task is waiting to be run.
-   **1**: The task is being run.
-   **2**: The task is run.
-   **3**: The task fails to be run. |
|TaskType|String|CHG\_DNS|The type of the task. |
|TaskTypeDescription|String|DNS server change|The description of the task type. If you change the value of the Lang parameter, the value of this parameter is presented in another language. |
|TryCount|Integer|0|The number of the query retries. |
|UpdateTime|String|2018-03-26 15:22:18|The time when the task was last run. |
|NextPage|Boolean|false|Indicates whether the current page is followed by another page. |
|PageSize|Integer|1|The number of entries returned per page. |
|PrePage|Boolean|false|Indicates whether the current page follows another page. |
|RequestId|String|E879DC07-38EE-4408-9F33-73B30CD965CD|The ID of the request. |
|TotalItemNum|Integer|10|The total number of entries returned. |
|TotalPageNum|Integer|10|The total number of pages returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=PollTaskResult
&PageNum=1
&PageSize=20
&<Common request parameters>
```

Sample success responses

`XML` format

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
            <ErrorMsg>The operation is successful. </ErrorMsg>
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

`JSON` format

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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

