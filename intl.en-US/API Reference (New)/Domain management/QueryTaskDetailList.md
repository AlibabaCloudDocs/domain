# QueryTaskDetailList

Queries the details of a specific domain name task by page.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryTaskDetailList&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryTaskDetailList|The operation that you want to perform. Set the value to **QueryTaskDetailList**. |
|PageNum|Integer|Yes|1|The number of the page to return. |
|PageSize|Integer|Yes|1|The number of entries to return on each page. Maximum value: **1000**. |
|TaskNo|String|Yes|75addb07-28a3-450e-b5ec-test|The ID of the task. |
|TaskStatus|Integer|No|2|The status of the task. Valid values:

 -   **0**: The task is waiting to be run.
-   **1**: The task is being run.
-   **2**: The task is run.
-   **3**: The task fails to be run. |
|InstanceId|String|No|S20179H1BBI9test|The instance ID of the domain name. |
|DomainName|String|No|example.com|The domain name. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.0|The IP address of the client that is used for the query. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CurrentPageNum|Integer|1|The page number of the returned page. |
|Data|Array of TaskDetail| |The details of the task. |
|TaskDetail| | | |
|CreateTime|String|2018-01-25 20:46:57|The time when the task was created. |
|DomainName|String|example.com|The domain name. |
|ErrorMsg|String|The operation is successful.|The message that indicates the result of the task. |
|InstanceId|String|S20179H1BBI9test|The instance ID of the domain name. |
|TaskDetailNo|String|75addb07-28a3-450e-b5ec-test|The ID of the task details that is returned. |
|TaskNo|String|60d6e201-8ee5-47ab-8fdc-test|The ID of the task. |
|TaskResult|String|12345|The result of the task. |
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
|TaskType|String|ORDER\_RENEW|The type of the task. Valid values:

 -   **CHG\_HOLDER**: The task is run to modify the domain name registrant.
-   **CHG\_DNS**: The task is run to change the DNS servers for the domain name.
-   **SET\_WHOIS\_PROTECT**: The task is run to configure privacy protection for the domain name.
-   **UPDATE\_ADMIN\_CONTACT**: The task is run to modify the information about the administrator of the domain name.
-   **UPDATE\_BILLING\_CONTACT**: The task is run to modify the information about the payer for the domain name.
-   **UPDATE\_TECH\_CONTACT**: The task is run to modify the information about the technical support for the domain name.
-   **SET\_UPDATE\_PROHIBITED**: The task is run to configure the security lock for the domain name.
-   **SET\_TRANSFER\_PROHIBITED**: The task is run to configure the transfer lock for the domain name.
-   **ORDER\_ACTIVATE**: The task is run to create a registration order for the domain name.
-   **ORDER\_RENEW**: The task is run to create a renewal order for the domain name.
-   **ORDER\_REDEEM**: The task is run to create a redemption order for the domain name.
-   **CREATE\_DNSHOST**: The task is run to create a DNS server for the domain name.
-   **UPDATE\_DNSHOST**: The task is run to update the information about a DNS server for the domain name.
-   **SYNC\_DNSHOST**: The task is run to synchronize a DNS server for the domain name. |
|TaskTypeDescription|String|Create a renewal order|The description of the task type. |
|TryCount|Integer|0|The number of the query retries. |
|UpdateTime|String|2018-01-25 20:47:01|The last time when the task was run. |
|NextPage|Boolean|true|Indicates whether the current page is followed by another page. |
|PageSize|Integer|2|The number of entries returned per page. |
|PrePage|Boolean|false|Indicates whether the current page follows another page. |
|RequestId|String|6A2320E4-D870-49C9-A6DC-test|The ID of the request. |
|TotalItemNum|Integer|1|The total number of entries returned. |
|TotalPageNum|Integer|1|The total number of pages returned. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/? Action=QueryTaskDetailList
&PageNum=1
&PageSize=1
&TaskNo=75addb07-28a3-450e-b5ec-test
&<Common request parameters>
```

Sample success responses

`XML` format

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
        <ErrorMsg>The operation is successful. </ErrorMsg>
        <TaskStatus>EXECUTE_SUCCESS</TaskStatus>
        <TaskTypeDescription>Create a renewal order</TaskTypeDescription>
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

`JSON` format

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
            "TaskTypeDescription": "Create a renewal order",
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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

