# SubmitOperationCredentials

Submits the materials to be reviewed for a self-service operation.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SubmitOperationCredentials&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SubmitOperationCredentials|The operation that you want to perform. Set the value to **SubmitOperationCredentials**. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|AuditRecordId|Long|No|1|The ID of the review record. |
|RegType|Integer|No|1|The type of the domain name registrant. Valid values:

 -   **1**: individual
-   **2**: enterprise |
|AuditType|Integer|No|1|The type of the operation that triggers the review. Valid values:

 **1**: offline transfer of domain names |
|Credentials|String|No|\[\{"credentialType":"SHSQB",""credentialUrl":"11212121/1212d\*\*/sqb.jpg"\},\{"credentialType":"SFZZM",""credentialUrl":"11212121/1212d\*\*/sfzzm.jpg"\}\]|The information about the materials to be reviewed. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|9DFCF6F8-243C-40EC-8035-4B12FEFX7D98|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/?Action=SubmitOperationCredentials&AuditRecordId=1&RegType=1&AuditType=1&Credentials=[{"credentialType":"SHSQB",""credentialUrl":"11212121/1212d**/sqb.jpg"},{"credentialType":"SFZZM",""credentialUrl":"11212121/1212d**/sfzzm.jpg"}]
&<Common request parameters>
```

Sample success responses

`XML` format

```
<SubmitOperationCredentialsResponse>
  <RequestId>9DFCF6F8-243C-40EC-8035-4B12FEFX7D98</RequestId>
</SubmitOperationCredentialsResponse>
```

`JSON` format

```
{"RequestId":"9DFCF6F8-243C-40EC-8035-4B12FEFX7D98"}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

