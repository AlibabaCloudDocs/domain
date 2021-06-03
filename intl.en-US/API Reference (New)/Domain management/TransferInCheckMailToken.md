# TransferInCheckMailToken

Verifies the token sent to the email address of the domain name registrant.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=TransferInCheckMailToken&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|TransferInCheckMailToken|The operation that you want to perform. Set the value to **TransferInCheckMailToken**. |
|Token|String|Yes|3bdbaa0e-faa2-4ad2-98f4-bcfeb0237054|The token in the email that the domain name registrant receives. |
|Lang|String|No|en|The language of the error message to return. Valid values:

-   **zh:** Chinese
-   **en:** English

Default value:**en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|FailList| |test.com|The domain names that failed verification. |
|RequestId|String|AF7D4DCE-0776-47F2-A9B2-6FB85A87AA60|The ID of the request. |
|SuccessList| |test.com|The domain names that passed verification. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=TransferInCheckMailToken
&Token=3bdbaa0e-faa2-4ad2-98f4-bcfeb0237054
&<Common request parameters>

```

Sample success responses

`XML` format

```
<TransferInCheckMailTokenResponse>
    <FailList></FailList>
    <RequestId>C99AA313-4A94-4896-915B-4D4043C063DA</RequestId>
    <SuccessList>
        <SuccessDomain>test.com</SuccessDomain>
    </SuccessList>
</TransferInCheckMailTokenResponse>
```

`JSON` format

```
{
	"FailList":{
		"FailDomain":[]
	},
	"RequestId":"3E5677B5-6F55-4518-9A55-A9CE57313C9D",
	"SuccessList":{
		"SuccessDomain":[
			"test.com"
		]
	}
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

