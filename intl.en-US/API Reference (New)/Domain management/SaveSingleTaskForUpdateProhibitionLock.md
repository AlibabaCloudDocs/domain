# SaveSingleTaskForUpdateProhibitionLock

Submits a task to enable the update prohibition lock for a domain name.

You can call the [QueryTaskDetailList](~~67710~~) operation to query the task execution result.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForUpdateProhibitionLock&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveSingleTaskForUpdateProhibitionLock|The operation that you want to perform. Set the value to **SaveSingleTaskForUpdateProhibitionLock**. |
|DomainName|String|Yes|test1.com|The domain name for which you want to enable the update prohibition lock. |
|Status|Boolean|Yes|false|Specifies whether the update prohibition lock is enabled. Valid values:

-   **true:** enabled
-   **false:** disabled |
|Lang|String|No|en|The language of the error message to return. Valid values:

-   **zh:** Chinese
-   **en:** English

Default value:**en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|F51977F9-2B40-462B-BCCD-CF5BB1E9DB56|The ID of the request. |
|TaskNo|String|d3babb0a-c939-4c25-8c65-c47b65f5492a|The ID of the task that was submitted. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=SaveSingleTaskForUpdateProhibitionLock
&DomainName=test1.com
&Status=false
&<Common request parameters>

```

Sample success responses

`XML` format

```
<SaveSingleTaskForUpdateProhibitionLockResponse>
      <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
      <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
</SaveSingleTaskForUpdateProhibitionLockResponse>
```

`JSON` format

```
{
	"TaskNo":"d3babb0a-c939-4c25-8c65-c47b65f5492a",
	"RequestId":"F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

