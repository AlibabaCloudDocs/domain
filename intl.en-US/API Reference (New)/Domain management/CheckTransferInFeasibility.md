# CheckTransferInFeasibility

Checks whether a domain name can be transferred to Alibaba Cloud.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=CheckTransferInFeasibility&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CheckTransferInFeasibility|The operation that you want to perform. Set the value to **CheckTransferInFeasibility**. |
|DomainName|String|Yes|Aliyun.com|The domain name that you want to check. |
|TransferAuthorizationCode|String|No|test|The key that is used to transfer the domain name to Alibaba Cloud. |
|Lang|String|No|en|The language of the error message returned. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used for the check. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CanTransfer|Boolean|false|Indicates whether the domain name can be transferred to Alibaba Cloud. Valid values:

-   **true**: The domain name can be transferred to Alibaba Cloud.
-   **false**: The domain name cannot be transferred to Alibaba Cloud. |
|Code|String|CheckTransferResult.DomainTransferProhibited|The error code that the system returned when the domain name cannot be transferred to Alibaba Cloud. |
|Message|String|This domain name is in transfer prohibited status, so it cannot be transferred. You can contact your original registrar to change its status.|The error message that the system returned when the domain name cannot be transferred to Alibaba Cloud. |
|ProductId|String|2a|The ID of the Domains service. |
|RequestId|String|FC0D6B89-2353-4D64-BD80-6606A7DBD7C1|The ID of the request. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=CheckTransferInFeasibility
&DomainName=test.com
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CheckTransferInFeasibilityResponse>
    <RequestId>60D2283F-36EA-46D4-A38D-15B5A2C455E3</RequestId>
    <CanTransfer>true</CanTransfer>
    <ProductId>2a</ProductId>
</CheckTransferInFeasibilityResponse>
```

`JSON` format

```
{
    "CanTransfer":true,
    "ProductId":"2a",
    "RequestId":"CE82EB4C-882D-430B-A908-E0BECFC35025"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

