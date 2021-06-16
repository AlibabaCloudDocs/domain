# CancelOperationAudit

Cancels the review for a self-service operation.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=CancelOperationAudit&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CancelOperationAudit|The operation that you want to perform. Set the value to **CancelOperationAudit**. |
|AuditRecordId|Long|Yes|1|The ID of the review record. You can call the [QueryOperationAuditInfoList](~~172568~~) operation to query the review record ID. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|9KFCF6F8-243C-40EC-8035-4B12KKFD7D90|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/?Action=CancelOperationAudit
&AuditRecordId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CancelOperationAuditResponse>
  <RequestId>9KFCF6F8-243C-40EC-8035-4B12KKFD7D90</RequestId>
</CancelOperationAuditResponse>
```

`JSON` format

```
{"RequestId":"9KFCF6F8-243C-40EC-8035-4B12KKFD7D90"}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

