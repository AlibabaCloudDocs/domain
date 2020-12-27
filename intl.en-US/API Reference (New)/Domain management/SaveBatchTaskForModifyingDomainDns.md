# SaveBatchTaskForModifyingDomainDns

Submits a task for changing the domain name system \(DNS\) servers of multiple domain names at a time.

You can call the [QueryTaskDetailList](~~67710~~)operation to query the running result of the task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveBatchTaskForModifyingDomainDns&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveBatchTaskForModifyingDomainDns|The operation that you want to perform. Set the value to **SaveBatchTaskForModifyingDomainDns**. |
|AliyunDns|Boolean|Yes|false|Specifies whether to change the DNS server to the Alibaba Cloud DNS server. Valid values:

 -   **true**: yes
-   **false**: no |
|DomainName.N|RepeatList|Yes|test1.com|The domain name whose DNS server you want to change. |
|DomainNameServer.N|RepeatList|No|ns1.test.com|The DNS servers that you want to change. This parameter is required only when **AliyunDns** is set to **false**. |
|Lang|String|No|en|The language of the error message returned. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to submit the task. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|6A862A8A-E7AB-4C4E-8946-A74122D9CC4B|The ID of the request. |
|TaskNo|String|35fb2fb7-d4d6-4478-9408-22cb63696b86|The ID of the task that was submitted. |

## Examples

Sample requests

```
http://domain.aliyuncs.com/?Action=SaveBatchTaskForModifyingDomainDns
&AliyunDns=false
&DomainName.1=test1.com
&DomainName.2=test2.com
&DomainNameServer.1=ns1.test.com
&DomainNameServer.2=ns2.test.com
&<Common request parameters>
```

Sample success responses

`XML` format

```
<SaveBatchTaskForModifyingDomainDnsResponse>
  <TaskNo>35fb2fb7-d4d6-4478-9408-22cb63696b86</TaskNo>
  <RequestId>6A862A8A-E7AB-4C4E-8946-A74122D9CC4B</RequestId></SaveBatchTaskForModifyingDomainDnsResponse>
```

`JSON` format

```
{
  "requestId": "689C17B3-6AE0-45FB-8E41-4491A02C9999",
  "taskNo": "fce12087-6c9f-4dcd-92df-d3829b7f19bc"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

