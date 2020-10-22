# QueryTaskDetailHistory

Queries the historical details of a domain name task by page.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryTaskDetailHistory&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryTaskDetailHistory|The operation that you want to perform. Set the value to **QueryTaskDetailHistory**. |
|PageSize|Integer|Yes|1|The number of entries to return on each page. |
|TaskNo|String|Yes|75addb07-28a3-450e-b5ec-test|The ID of the task that you want to query.

 **Note:** You can call the QueryTaskList operation to query the task ID. For more information, see [QueryTaskList](~~67709~~). |
|Lang|String|No|en|The language of the error message to return. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that you use to query the task. |
|DomainName|String|No|test.com|The domain name of the task that you want to query. |
|DomainNameCursor|String|No|test.com|The cursor of the domain name. |
|TaskStatus|Integer|No|0|The status of the task. Valid values:

 -   **0**: to be executed
-   **1**: being executed
-   **2**: successful
-   **3**: failed |
|TaskDetailNoCursor|String|No|75addb07-28a3-450e-b5ec|The cursor of the task details. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CurrentPageCursor|Struct| |The cursor of the current page. |
|CreateTime|String|2019-07-30 00:00:00|The time when the task was created. |
|DomainName|String|test.com|The domain name of the task that was queried. |
|ErrorMsg|String|Successful|The task execution result. |
|InstanceId|String|S1234456789|The instance ID of the domain name that was queried. |
|TaskDetailNo|String|75addb07-28a3-450e-b5ec-2342|The ID of the task details. |
|TaskNo|String|75addb07-28a3-450e-b5ec-test|The ID of the task that was queried. |
|TaskStatus|String|EXECUTE\_SUCCESS|The status of the task. Valid values:

 -   **WAITING\_EXECUTE**: to be executed
-   **EXECUTING**: being executed
-   **EXECUTE\_SUCCESS**: successful
-   **EXECUTE\_FAILURE**: failed |
|TaskStatusCode|Integer|2|The status code of the task. Valid values:

 -   **0**: to be executed
-   **1**: being executed
-   **2**: successful
-   **3**: failed |
|TaskType|String|CHG\_DNS|The type of the task. Valid values:

 -   **CHG\_HOLDER**: updates the registrant information.
-   **CHG\_DNS**: changes Domain Name System \(DNS\) servers.
-   **SET\_WHOIS\_PROTECT**: sets privacy protection for the domain name.
-   **UPDATE\_ADMIN\_CONTACT**: updates the administrative contacts.
-   **UPDATE\_BILLING\_CONTACT**: updates the payer information.
-   **UPDATE\_TECH\_CONTACT**: updates the information about the technical support.
-   **SET\_UPDATE\_PROHIBITED**: sets the security lock for the domain name.
-   **SET\_TRANSFER\_PROHIBITED**: sets the transfer lock for the domain name.
-   **ORDER\_ACTIVATE**: creates a registration order.
-   **ORDER\_RENEW**: creates a renewal order.
-   **ORDER\_REDEEM**: creates a redemption order.
-   **CREATE\_DNSHOST**: creates a DNS host.
-   **UPDATE\_DNSHOST**: updates the information about a DNS host.
-   **SYNC\_DNSHOST**: synchronizes the information about a DNS host. |
|TaskTypeDescription|String|Change DNS servers|The description of the task type. |
|TryCount|Integer|0|The number of query attempts. |
|UpdateTime|String|2019-07-30 00:00:00|The last time when the task was executed. |
|NextPageCursor|Struct| |The cursor of the next page. |
|CreateTime|String|2019-07-30 00:00:00|The time when the task was created. |
|DomainName|String|test.com|The domain name of the task that was queried. |
|ErrorMsg|String|The domain name has an update lock.|The task execution result. |
|InstanceId|String|S1234567890|The instance ID of the domain name that was queried. |
|TaskDetailNo|String|75addb07-28a3-450e-b5ec-2424|The ID of the task details. |
|TaskNo|String|75addb07-28a3-450e-b5ec-test|The ID of the task that was queried. |
|TaskStatus|String|EXECUTE\_FAILURE|The status of the task. Valid values:

 -   **WAITING\_EXECUTE**: to be executed
-   **EXECUTING**: being executed
-   **EXECUTE\_SUCCESS**: successful
-   **EXECUTE\_FAILURE**: failed |
|TaskStatusCode|Integer|3|The status code of the task. Valid values:

 -   **0**: to be executed
-   **1**: being executed
-   **2**: successful
-   **3**: failed |
|TaskType|String|CHG\_DNS|The type of the task. Valid values:

 -   **CHG\_HOLDER**: updates the registrant information.
-   **CHG\_DNS**: changes DNS servers.
-   **SET\_WHOIS\_PROTECT**: sets privacy protection for the domain name.
-   **UPDATE\_ADMIN\_CONTACT**: updates the administrative contacts.
-   **UPDATE\_BILLING\_CONTACT**: updates the payer information.
-   **UPDATE\_TECH\_CONTACT**: updates the information about the technical support.
-   **SET\_UPDATE\_PROHIBITED**: sets the security lock for the domain name.
-   **SET\_TRANSFER\_PROHIBITED**: sets the transfer lock for the domain name.
-   **ORDER\_ACTIVATE**: creates a registration order.
-   **ORDER\_RENEW**: creates a renewal order.
-   **ORDER\_REDEEM**: creates a redemption order.
-   **CREATE\_DNSHOST**: creates a DNS host.
-   **UPDATE\_DNSHOST**: updates the information about a DNS host.
-   **SYNC\_DNSHOST**: synchronizes the information about a DNS host. |
|TaskTypeDescription|String|Change DNS servers|The description of the task type. |
|TryCount|Integer|5|The number of query attempts. |
|UpdateTime|String|2019-07-30 00:00:00|The last time when the task was executed. |
|Objects|Array| |The details of the task. |
|CreateTime|String|2019-07-30 00:00:00|The time when the task was created. |
|DomainName|String|test.com|The domain name of the task that was queried. |
|ErrorMsg|String|The domain name has an update lock.|The task execution result. |
|InstanceId|String|S123456789|The instance ID of the domain name that was queried. |
|TaskDetailNo|String|75addb07-28a3-450e-b5ec-4234|The ID of the task details. |
|TaskNo|String|75addb07-28a3-450e-b5ec-test|The ID of the task that was queried. |
|TaskStatus|String|EXECUTE\_FAILURE|The status of the task. Valid values:

 -   **WAITING\_EXECUTE**: to be executed
-   **EXECUTING**: being executed
-   **EXECUTE\_SUCCESS**: successful
-   **EXECUTE\_FAILURE**: failed |
|TaskStatusCode|Integer|3|The status code of the task. Valid values:

 -   **0**: to be executed
-   **1**: being executed
-   **2**: successful
-   **3**: failed |
|TaskType|String|CHG\_DNS|The type of the task. Valid values:

 -   **CHG\_HOLDER**: updates the registrant information.
-   **CHG\_DNS**: changes DNS servers.
-   **SET\_WHOIS\_PROTECT**: sets privacy protection for the domain name.
-   **UPDATE\_ADMIN\_CONTACT**: updates the administrative contacts.
-   **UPDATE\_BILLING\_CONTACT**: updates the payer information.
-   **UPDATE\_TECH\_CONTACT**: updates the information about the technical support.
-   **SET\_UPDATE\_PROHIBITED**: sets the security lock for the domain name.
-   **SET\_TRANSFER\_PROHIBITED**: sets the transfer lock for the domain name.
-   **ORDER\_ACTIVATE**: creates a registration order.
-   **ORDER\_RENEW**: creates a renewal order.
-   **ORDER\_REDEEM**: creates a redemption order.
-   **CREATE\_DNSHOST**: creates a DNS host.
-   **UPDATE\_DNSHOST**: updates the information about a DNS host.
-   **SYNC\_DNSHOST**: synchronizes the information about a DNS host. |
|TaskTypeDescription|String|Change DNS servers|The description of the task type. |
|TryCount|Integer|5|The number of query attempts. |
|UpdateTime|String|2019-07-30 00:00:00|The last time when the task was executed. |
|PageSize|Integer|2|The number of entries returned per page. |
|PrePageCursor|Struct| |The cursor of the previous page. |
|CreateTime|String|2019-07-30 00:00:00|The time when the task was created. |
|DomainName|String|test.com|The domain name of the task that was queried. |
|ErrorMsg|String|The domain name has an update lock.|The task execution result. |
|InstanceId|String|S123456789|The instance ID of the domain name that was queried. |
|TaskDetailNo|String|75addb07-28a3-450e-b5ec-123|The ID of the task details. |
|TaskNo|String|75addb07-28a3-450e-b5ec-test|The ID of the task that was queried. |
|TaskStatus|String|EXECUTE\_FAILURE|The status of the task. Valid values:

 -   **WAITING\_EXECUTE**: to be executed
-   **EXECUTING**: being executed
-   **EXECUTE\_SUCCESS**: successful
-   **EXECUTE\_FAILURE**: failed |
|TaskStatusCode|Integer|3|The status code of the task. Valid values:

 -   **0**: to be executed
-   **1**: being executed
-   **2**: successful
-   **3**: failed |
|TaskType|String|CHG\_DNS|The type of the task. Valid values:

 -   **CHG\_HOLDER**: updates the registrant information.
-   **CHG\_DNS**: changes DNS servers.
-   **SET\_WHOIS\_PROTECT**: sets privacy protection for the domain name.
-   **UPDATE\_ADMIN\_CONTACT**: updates the administrative contacts.
-   **UPDATE\_BILLING\_CONTACT**: updates the payer information.
-   **UPDATE\_TECH\_CONTACT**: updates the information about the technical support.
-   **SET\_UPDATE\_PROHIBITED**: sets the security lock for the domain name.
-   **SET\_TRANSFER\_PROHIBITED**: sets the transfer lock for the domain name.
-   **ORDER\_ACTIVATE**: creates a registration order.
-   **ORDER\_RENEW**: creates a renewal order.
-   **ORDER\_REDEEM**: creates a redemption order.
-   **CREATE\_DNSHOST**: creates a DNS host.
-   **UPDATE\_DNSHOST**: updates the information about a DNS host.
-   **SYNC\_DNSHOST**: synchronizes the information about a DNS host. |
|TaskTypeDescription|String|Change DNS servers|The description of the task type. |
|TryCount|Integer|5|The number of query attempts. |
|UpdateTime|String|2019-07-30 00:00:00|The last time when the task was executed. |
|RequestId|String|548CAE74-88F8-402F-8C12-97E747389C51|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=QueryTaskDetailHistory
&PageSize=1
&TaskNo=75addb07-28a3-450e-b5ec-test
&<Common request parameters>
```

Sample success responses

`XML` format

```
<QueryTaskDetailHistoryResponse>
  <currentPageCursor></currentPageCursor>
  <nextPageCursor></nextPageCursor>
  <pageSize>2</pageSize>
  <prePageCursor></prePageCursor>
  <requestId>CCE5DABB-48DF-403C-A7A1-A8F8B4F530CA</requestId>
</QueryTaskDetailHistoryResponse>
```

`JSON` format

```
{
  "currentPageCursor": {},
  "nextPageCursor": {},
  "objects": [],
  "pageSize": 2,
  "prePageCursor": {},
  "requestId": "CCE5DABB-48DF-403C-A7A1-A8F8B4F530CA"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

