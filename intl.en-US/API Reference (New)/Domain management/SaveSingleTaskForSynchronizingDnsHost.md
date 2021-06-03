# SaveSingleTaskForSynchronizingDnsHost

Submits a task to synchronize DNS host information. This operation can be used to handle problems such as missing and inconsistent DNS hosts.

You can call the [QueryTaskDetailList](~~67710~~) operation to query the task execution result.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForSynchronizingDnsHost&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveSingleTaskForSynchronizingDnsHost|The operation that you want to perform. Set the value to **SaveSingleTaskForSynchronizingDnsHost**. |
|InstanceId|String|Yes|ST2017120814571100001303|The instance ID corresponding to the domain name for which you want to synchronize DNS host information. You can call the QueryDomainList operation to query the instance ID. |
|Lang|String|No|en|The language of the error message to return. Valid values:

-   **zh:** Chinese
-   **en:** English

Default value:**en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|0F1B3547-BE50-4206-8F78-9540FFB85BC1|The ID of the request. |
|TaskNo|String|e9b8e8b4-7334-4548-9cec-c30b6891f292|The ID of the task that was submitted. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=SaveSingleTaskForSynchronizingDnsHost
&InstanceId=ST2017120814571100001303
&<Common request parameters>

```

Sample success responses

`XML` format

```
<SaveSingleTaskForSynchronizingDnsHostResponse>
  <TaskNo>e9b8e8b4-7334-4548-9cec-c30b6891f292</TaskNo>
  <RequestId>0F1B3547-BE50-4206-8F78-9540FFB85BC1</RequestId>
</SaveSingleTaskForSynchronizingDnsHostResponse>
```

`JSON` format

```
{
	"requestId":"0F1B3547-BE50-4206-8F78-9540FFB85BC1",
	"taskNo":"e9b8e8b4-7334-4548-9cec-c30b6891f292"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

