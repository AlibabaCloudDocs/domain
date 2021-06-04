# SaveSingleTaskForQueryingTransferAuthorizationCode

Submits a task to obtain a domain name transfer key.

You can call the [QueryTaskDetailList](~~67710~~) operation to query the task execution result. The transfer key is returned in the TaskResult field of the corresponding task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForQueryingTransferAuthorizationCode&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveSingleTaskForQueryingTransferAuthorizationCode|The operation that you want to perform. Set the value to **SaveSingleTaskForQueryingTransferAuthorizationCode**. |
|DomainName|String|Yes|test.com|The domain name for which you want to obtain the transfer key. |
|Lang|String|No|en|The language of the error message to return. Valid values:

-   **zh:** Chinese
-   **en:** English

Default value:**en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|AF7D4DCE-0776-47F2-A9B2-6FB85A87AA60|The ID of the request. |
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|The ID of the task that was submitted. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=SaveSingleTaskForQueryingTransferAuthorizationCode
&DomainName=test.com
&<Common request parameters>

```

Sample success responses

`XML` format

```
<SaveSingleTaskForQueryingTransferAuthorizationCodeResponse>
    <TaskNo>3bdbaa0e-faa2-4ad2-98f4-bcfeb0237054</TaskNo>
    <RequestId>EEB28AA7-6051-4E71-B2CC-DAAFB2DF6BCA</RequestId>
</SaveSingleTaskForQueryingTransferAuthorizationCodeResponse>
```

`JSON` format

```
{
	"TaskNo":"939b6918-be3b-4c4f-b949-93553da52dca",
	"RequestId":"492D1868-1384-4219-8F8B-7EB44534A72A"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

