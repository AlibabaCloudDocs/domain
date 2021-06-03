# AcknowledgeTaskResult

Confirms detailed task results.

After task results are confirmed,you cannot query them by calling the [PollTaskResult](~~69361~~) operation.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=AcknowledgeTaskResult&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AcknowledgeTaskResult|The operation that you want to perform. Set the value to **AcknowledgeTaskResult**. |
|TaskDetailNo.N|RepeatList|Yes|2659c29493e94416b297a7691340ccc4|The ID of the task details. |
|Lang|String|No|en|The language of the error message to return. Valid values:

-   **zh:** Chinese
-   **en:** English

Default value:**en** |
|UserClientIp|String|No|127.0.0.1|The IP address of the client. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|D6CB3623-4726-4947-AC2B-2C6E673B447C|The ID of the request. |
|Result|Integer|1|The number of successful tasks. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=AcknowledgeTaskResult
&TaskDetailNo.1=2659c29493e94416b297a7691340ccc4
&<Common request parameters>

```

Sample success responses

`XML` format

```
<AcknowledgeTaskResultResponse>
    <Result>2</Result>
    <RequestId>25DE4410-3E4D-493E-A5E2-927DB738CCEB</RequestId>
</AcknowledgeTaskResultResponse>
```

`JSON` format

```
{
	"Result":2,
	"RequestId":"270F04F2-6086-4B54-A86B-A1956F231CEC"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

