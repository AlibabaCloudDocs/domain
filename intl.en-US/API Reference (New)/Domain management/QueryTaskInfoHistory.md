# QueryTaskInfoHistory

Queries the historical domain name tasks within your account by page.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryTaskInfoHistory&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryTaskInfoHistory|The operation that you want to perform. Set the value to **QueryTaskInfoHistory**. |
|PageSize|Integer|Yes|2|The number of entries to return on each page. |
|TaskNoCursor|String|No|aa634d3f-927e-4d17-9d2c-test|The task ID that you enter at the cursor of a page when you turn pages. This parameter is a technical parameter. |
|CreateTimeCursor|Long|No|1522080000000|The cursor of the date when the task was created. This parameter is a technical parameter. |
|BeginCreateTime|Long|No|1522080000000|The beginning of the time range to query. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. Only query by day is supported. |
|EndCreateTime|Long|No|1522080000000|The end of the time range to query. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. Only query by day is supported. |
|Lang|String|No|en|The language of the error message returned. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to query the historical domain name tasks. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CurrentPageCursor|Struct| |The cursor of the current page. |
|Clientip|String|127.0.0.1|The IP address of the client that is used to submit the task. |
|CreateTime|String|2017-11-01 17:22:51|The time when the task was created. The time follows the ISO 8601 standard in the yyyy-MM-ddThh:mm:ssZ format. The time is displayed in UTC. |
|CreateTimeLong|Long|1509528171000|The timestamp when the task was created. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|TaskNo|String|aa634d3f-927e-4d17-9d2c-test|The ID of the task. |
|TaskNum|Integer|1|The number of domain names involved in the task. |
|TaskStatus|String|COMPLETE|The status of the task. Valid values:

-   **WAITING\_EXECUTE**: The task is waiting to be run.
-   **EXECUTING**: The task is running.
-   **COMPLETE**: The task is run. |
|TaskStatusCode|Integer|3|The status code of the task. Valid values:

-   **1**: The task is waiting to be run.
-   **2**: The task is running.
-   **3**: The task is run. |
|TaskType|String|CHG\_DNS|The type of the task. Valid values:

-   **CHG\_HOLDER**: Update the registrant information.
-   **CHG\_DNS**: Change the DNS server.
-   **SET\_WHOIS\_PROTECT**: Enable WHOIS privacy protection.
-   **UPDATE\_ADMIN\_CONTACT**: Update the administrator information.
-   **UPDATE\_BILLING\_CONTACT**: Update the payer information.
-   **UPDATE\_TECH\_CONTACT**: Update the technician information.
-   **SET\_UPDATE\_PROHIBITED**: Enable the security lock for the domain name.
-   **SET\_TRANSFER\_PROHIBITED**: Enable the transfer prohibition lock for the domain name.
-   **ORDER\_ACTIVATE**: Create a registration order.
-   **ORDER\_RENEW**: Create a renewal order.
-   **ORDER\_REDEEM**: Create a redemption order.
-   **CREATE\_DNSHOST**: Create a DNS server.
-   **UPDATE\_DNSHOST**: Update a DNS server.
-   **UPDATE\_REGISTRANT\_CONTACT**: Update the registration contact.
-   **DELETE\_DOMAIN**: Delete the domain name.
-   **SYNC\_DNSHOST**: Synchronize a DNS server. |
|TaskTypeDescription|String|DNS server change|The description of the task type. |
|NextPageCursor|Struct| |The cursor of the next page. |
|Clientip|String|127.0.0.1|The IP address of the client that is used to submit the task. |
|CreateTime|String|2017-10-27 13:07:07|The time when the task was created. The time follows the ISO 8601 standard in the yyyy-MM-ddThh:mm:ssZ format. The time is displayed in UTC. |
|CreateTimeLong|Long|1509080827000|The timestamp when the task was created. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|TaskNo|String|8f112aa1-98be-48c3-82f8-test|The ID of the task. |
|TaskNum|Integer|15|The number of domain names involved in the task. |
|TaskStatus|String|COMPLETE|The status of the task. Valid values:

-   **WAITING\_EXECUTE**: The task is waiting to be run.
-   **EXECUTING**: The task is running.
-   **COMPLETE**: The task is run. |
|TaskStatusCode|Integer|3|The status code of the task. Valid values:

-   **1**: The task is waiting to be run.
-   **2**: The task is running.
-   **3**: The task is run. |
|TaskType|String|CHG\_DNS|The type of the task. Valid values:

-   **CHG\_HOLDER**: Update the registrant information.
-   **CHG\_DNS**: Change the DNS server.
-   **SET\_WHOIS\_PROTECT**: Enable WHOIS privacy protection.
-   **UPDATE\_ADMIN\_CONTACT**: Update the administrator information.
-   **UPDATE\_BILLING\_CONTACT**: Update the payer information.
-   **UPDATE\_TECH\_CONTACT**: Update the technician information.
-   **SET\_UPDATE\_PROHIBITED**: Enable the security lock for the domain name.
-   **SET\_TRANSFER\_PROHIBITED**: Enable the transfer prohibition lock for the domain name.
-   **ORDER\_ACTIVATE**: Create a registration order.
-   **ORDER\_RENEW**: Create a renewal order.
-   **ORDER\_REDEEM**: Create a redemption order.
-   **CREATE\_DNSHOST**: Create a DNS server.
-   **UPDATE\_DNSHOST**: Update a DNS server.
-   **UPDATE\_REGISTRANT\_CONTACT**: Update the registration contact.
-   **DELETE\_DOMAIN**: Delete the domain name.
-   **SYNC\_DNSHOST**: Synchronize a DNS server. |
|TaskTypeDescription|String|DNS server change|The description of the task type. |
|Objects|Array of TaskInfoHistory| |The information of the task. |
|Clientip|String|127.0.0.1|The IP address of the client that is used to submit the task. |
|CreateTime|String|2017-11-01 17:22:51|The time when the task was created. The time follows the ISO 8601 standard in the yyyy-MM-ddThh:mm:ssZ format. The time is displayed in UTC. |
|CreateTimeLong|Long|1509528171000|The timestamp when the task was created. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|TaskNo|String|aa634d3f-927e-4d17-9d2c-test|The ID of the task. |
|TaskNum|Integer|1|The number of domain names involved in the task. |
|TaskStatus|String|COMPLETE|The status of the task. Valid values:

-   **WAITING\_EXECUTE**: The task is waiting to be run.
-   **EXECUTING**: The task is running.
-   **COMPLETE**: The task is run. |
|TaskStatusCode|Integer|3|The status code of the task. Valid values:

-   **1**: The task is waiting to be run.
-   **2**: The task is running.
-   **3**: The task is run. |
|TaskType|String|CHG\_DNS|The type of the task. Valid values:

-   **CHG\_HOLDER**: Update the registrant information.
-   **CHG\_DNS**: Change the DNS server.
-   **SET\_WHOIS\_PROTECT**: Enable WHOIS privacy protection.
-   **UPDATE\_ADMIN\_CONTACT**: Update the administrator information.
-   **UPDATE\_BILLING\_CONTACT**: Update the payer information.
-   **UPDATE\_TECH\_CONTACT**: Update the technician information.
-   **SET\_UPDATE\_PROHIBITED**: Enable the security lock for the domain name.
-   **SET\_TRANSFER\_PROHIBITED**: Enable the transfer prohibition lock for the domain name.
-   **ORDER\_ACTIVATE**: Create a registration order.
-   **ORDER\_RENEW**: Create a renewal order.
-   **ORDER\_REDEEM**: Create a redemption order.
-   **CREATE\_DNSHOST**: Create a DNS server.
-   **UPDATE\_DNSHOST**: Update a DNS server.
-   **UPDATE\_REGISTRANT\_CONTACT**: Update the registration contact.
-   **DELETE\_DOMAIN**: Delete the domain name.
-   **SYNC\_DNSHOST**: Synchronize a DNS server. |
|TaskTypeDescription|String|DNS server change|The description of the task type. |
|PageSize|Integer|2|The number of entries returned per page. |
|PrePageCursor|Struct| |The cursor of the previous page. |
|Clientip|String|127.0.0.1|The IP address of the client that is used to submit the task. |
|CreateTime|String|2017-11-01 17:19:47|The time when the task was created. The time follows the ISO 8601 standard in the yyyy-MM-ddThh:mm:ssZ format. The time is displayed in UTC. |
|CreateTimeLong|Long|1509527987000|The timestamp when the task was created. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|TaskNo|String|f9baa3d5-33b9-4c81-8847-test|The ID of the task. |
|TaskNum|Integer|15|The number of domain names involved in the task. |
|TaskStatus|String|COMPLETE|The status of the task. Valid values:

-   **WAITING\_EXECUTE**: The task is waiting to be run.
-   **EXECUTING**: The task is running.
-   **COMPLETE**: The task is run. |
|TaskStatusCode|Integer|3|The status code of the task. Valid values:

-   **1**: The task is waiting to be run.
-   **2**: The task is running.
-   **3**: The task is run. |
|TaskType|String|CHG\_DNS|The type of the task. Valid values:

-   **CHG\_HOLDER**: Update the registrant information.
-   **CHG\_DNS**: Change the DNS server.
-   **SET\_WHOIS\_PROTECT**: Enable WHOIS privacy protection.
-   **UPDATE\_ADMIN\_CONTACT**: Update the administrator information.
-   **UPDATE\_BILLING\_CONTACT**: Update the payer information.
-   **UPDATE\_TECH\_CONTACT**: Update the technician information.
-   **SET\_UPDATE\_PROHIBITED**: Enable the security lock for the domain name.
-   **SET\_TRANSFER\_PROHIBITED**: Enable the transfer prohibition lock for the domain name.
-   **ORDER\_ACTIVATE**: Create a registration order.
-   **ORDER\_RENEW**: Create a renewal order.
-   **ORDER\_REDEEM**: Create a redemption order.
-   **CREATE\_DNSHOST**: Create a DNS server.
-   **UPDATE\_DNSHOST**: Update a DNS server.
-   **UPDATE\_REGISTRANT\_CONTACT**: Update the registration contact.
-   **DELETE\_DOMAIN**: Delete the domain name.
-   **SYNC\_DNSHOST**: Synchronize a DNS server. |
|TaskTypeDescription|String|DNS server change|The description of the task type. |
|RequestId|String|EB3FCCBA-CA1F-4D31-9F34-test|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=QueryTaskInfoHistory
&PageSize=2
&<Common request parameters>
```

Sample success responses

`XML` format

```
<QueryTaskInfoHistoryResponse>
      <Objects>
            <TaskInfoHistory>
                  <Clientip>127.0.0.1</Clientip>
                  <TaskNo>aa634d3f-927e-4d17-9d2c-test</TaskNo>
                  <CreateTime>2017-11-01 17:22:51</CreateTime>
                  <TaskStatus>COMPLETE</TaskStatus>
                  <TaskNum>1</TaskNum>
                  <TaskStatusCode>3</TaskStatusCode>
                  <TaskType>CHG_DNS</TaskType>
                  <CreateTimeLong>1509528171000</CreateTimeLong>
            </TaskInfoHistory>
            <TaskInfoHistory>
                  <Clientip>127.0.0.1</Clientip>
                  <TaskNo>f9baa3d5-33b9-4c81-8847-test</TaskNo>
                  <CreateTime>2017-11-01 17:19:47</CreateTime>
                  <TaskStatus>COMPLETE</TaskStatus>
                  <TaskNum>15</TaskNum>
                  <TaskStatusCode>3</TaskStatusCode>
                  <TaskType>CHG_DNS</TaskType>
                  <CreateTimeLong>1509527987000</CreateTimeLong>
            </TaskInfoHistory>
      </Objects>
      <PageSize>2</PageSize>
      <NextPageCursor>
            <TaskNo>8f112aa1-98be-48c3-82f8-test</TaskNo>
            <CreateTime>2017-10-27 13:07:07</CreateTime>
            <CreateTimeLong>1509080827000</CreateTimeLong>
      </NextPageCursor>
      <RequestId>EB3FCCBA-CA1F-4D31-9F34-test</RequestId>
      <CurrentPageCursor>
            <Clientip>127.0.0.1</Clientip>
            <TaskNo>aa634d3f-927e-4d17-9d2c-test</TaskNo>
            <CreateTime>2017-11-01 17:22:51</CreateTime>
            <TaskStatus>COMPLETE</TaskStatus>
            <TaskNum>1</TaskNum>
            <TaskStatusCode>3</TaskStatusCode>
            <TaskType>CHG_DNS</TaskType>
            <CreateTimeLong>1509528171000</CreateTimeLong>
      </CurrentPageCursor>
</QueryTaskInfoHistoryResponse>
```

`JSON` format

```
{
  "currentPageCursor": {
    "clientip": "127.0.0.1",
    "createTime": "2017-11-01 17:22:51",
    "createTimeLong": 1509528171000,
    "taskNo": "aa634d3f-927e-4d17-9d2c-test",
    "taskNum": 1,
    "taskStatus": "COMPLETE",
    "taskStatusCode": 3,
    "taskType": "CHG_DNS"
  },
  "nextPageCursor": {
    "createTime": "2017-10-27 13:07:07",
    "createTimeLong": 1509080827000,
    "taskNo": "8f112aa1-98be-48c3-82f8-test"
  },
  "objects": [
    {
      "clientip": "127.0.0.1",
      "createTime": "2017-11-01 17:22:51",
      "createTimeLong": 1509528171000,
      "taskNo": "aa634d3f-927e-4d17-9d2c-test",
      "taskNum": 1,
      "taskStatus": "COMPLETE",
      "taskStatusCode": 3,
      "taskType": "CHG_DNS"
    },
    {
      "clientip": "127.0.0.1",
      "createTime": "2017-11-01 17:19:47",
      "createTimeLong": 1509527987000,
      "taskNo": "f9baa3d5-33b9-4c81-8847-test",
      "taskNum": 15,
      "taskStatus": "COMPLETE",
      "taskStatusCode": 3,
      "taskType": "CHG_DNS"
    }
  ],
  "pageSize": 2,
  "prePageCursor": {},
  "requestId": "6EB5D9B8-AD99-4423-9D02-test"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

