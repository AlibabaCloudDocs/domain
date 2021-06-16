# SaveSingleTaskForCreatingDnsHost

Submits a task for creating a DNS server.

## Description

You can call the [QueryTaskDetailList](~~67710~~) operation to query the task execution result.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForCreatingDnsHost&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveSingleTaskForCreatingDnsHost|The operation that you want to perform. Set the value to **SaveSingleTaskForCreatingDnsHost**. |
|InstanceId|String|Yes|S1234567890|The instance ID of the domain name. You can call the [QueryDomainList](~~67712~~) operation to query the instance ID. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|DnsName|String|Yes|dns1|The name of the DNS server. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to send the request. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|0F1B3547-BE50-4206-8F78-9540FFB85BC1|The unique ID of the request. |
|TaskNo|String|e9b8e8b4-7334-4548-9cec-c30b6891f292|The ID of the task. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=SaveSingleTaskForCreatingDnsHost
&DnsName=dns1
&InstanceId=S1234567890
&Ip.1=218.xx.xx.236
&<Common request parameters>
```

Sample success responses

`XML` format

```
HTTP/1.1 200 OK
Content-Type:application/xml

<SaveSingleTaskForCreatingDnsHostResponse>
<TaskNo>e9b8e8b4-7334-4548-9cec-c30b6891f292</TaskNo>
<RequestId>0F1B3547-BE50-4206-8F78-9540FFB85BC1</RequestId>
</SaveSingleTaskForCreatingDnsHostResponse>
```

`JSON` format

```
HTTP/1.1 200 OK
Content-Type:application/json

{
  "requestId" : "0F1B3547-BE50-4206-8F78-9540FFB85BC1",
  "taskNo" : "e9b8e8b4-7334-4548-9cec-c30b6891f292"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

