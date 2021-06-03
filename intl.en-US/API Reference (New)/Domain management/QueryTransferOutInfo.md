# QueryTransferOutInfo

Queries the transfer-out information of a domain name.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryTransferOutInfo&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryTransferOutInfo|The operation that you want to perform. Set the value to **QueryTransferOutInfo**. |
|DomainName|String|Yes|test.com|The domain name whose transfer-out information you want to query. |
|Lang|String|No|en|The language of the error message to return. Valid values:

-   **zh:** Chinese
-   **en:** English

Default value:**en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Email|String|test@test.com|The email address to which the transfer key was sent. |
|ExpirationDate|String|2018-04-13 19:57:56|The time when the transfer key expired. |
|PendingRequestDate|String|2018-04-13 19:57:56|The time when the registry transfer request was received. |
|RequestId|String|BBEC5A50-DFDF-482E-8343-B4EB0105E055|The ID of the request. |
|ResultCode|String|clientRejected|The error code that indicates the reason why the transfer failed. |
|ResultMsg|String|Transfer out rejected|The error message that indicates the reason why the transfer failed. |
|Status|Integer|8|The transfer status. Valid values:

-   **1:**verifying the mobile phone.
-   **2:**verifying the email address.
-   **3:** The transfer key is obtained.
-   **4:**transferring \(The registry transfer request is received.\)
-   **5:**transfer successful.
-   **8:**transfer failed. |
|TransferAuthorizationCodeSendDate|String|2018-04-13 19:57:56|The time when the transfer key was obtained. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=QueryTransferOutInfo
&DomainName=test.com
&<Common request parameters>

```

Sample success responses

`XML` format

```
<QueryTransferOutInfoResponse>
    <Status>3</Status>
    <RequestId>6F23B2C0-0355-4685-BB39-342956C5118B</RequestId>
    <TransferAuthorizationCodeSendDate>2018-03-29 19:57:56</TransferAuthorizationCodeSendDate>
    <ExpirationDate>2018-04-13 19:57:56</ExpirationDate>
</QueryTransferOutInfoResponse>
```

`JSON` format

```
{
	"Status":3,
	"RequestId":"BBEC5A50-DFDF-482E-8343-B4EB0105E055",
	"TransferAuthorizationCodeSendDate":"2018-03-29 19:57:56",
	"ExpirationDate":"2018-04-13 19:57:56"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

