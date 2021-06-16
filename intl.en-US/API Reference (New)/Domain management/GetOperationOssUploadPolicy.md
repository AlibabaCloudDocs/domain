# GetOperationOssUploadPolicy

Queries the storage information about the materials to be reviewed.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=GetOperationOssUploadPolicy&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|GetOperationOssUploadPolicy|The operation that you want to perform. Set the value to **GetOperationOssUploadPolicy**. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|AuditType|Integer|No|1|The type of the operation that triggers the review. Valid values:

 **1**: offline transfer of domain names |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Accessid|String|hObpgEXoca42\*\*\*\*|The AccessKey ID. |
|EncodedPolicy|String|eyJleHBpcmF0aW9uIjoiMjAaMC0wNy0wMlQxKToyMDoxMS44ODRaIiwiY29uZGl0aW9ucyI6W1siY29udGVudC1sZW5ndGgtcmFuZ2UiLDAsNTI0Mjg4MDBdLFsic3RhcnRzLXdpdGgiLCIka2V5IiwiMTIxOTU0MTE2MTIxMzA1Ny9PRkZMSU5FX1RSQU5TRkVSLzE1OTM2ODg1MTE4ODMi\*\*\*\*|The encryption policy. |
|ExpireTime|String|1593688811881|The expiration time. |
|FileDir|String|1219541161213157/OFFLINE\_TRANSFER/159368851\*\*\*\*|The URL of the file. |
|Host|String|//\*\*\*-basic-cert.oss-cn-\*\*\*.aliyuncs.com/|The endpoint of Object Storage Service \(OSS\). |
|RequestId|String|9DFCF6F8-243C-40EC-8035-4B12FEFD7D011|The ID of the request. |
|Signature|String|pNVECGkyL0tl4bKXekV5ErZ\*\*\*\*|The signature. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/?Action=GetOperationOssUploadPolicy
&<Common request parameters>
```

Sample success responses

`XML` format

```
<GetOperationOssUploadPolicyResponse>
  <FileDir>1219541161213157/OFFLINE_TRANSFER/159368851****</FileDir>
  <EncodedPolicy>eyJleHBpcmF0aW9uIjoiMjAaMC0wNy0wMlQxKToyMDoxMS44ODRaIiwiY29uZGl0aW9ucyI6W1siY29udGVudC1sZW5ndGgtcmFuZ2UiLDAsNTI0Mjg4MDBdLFsic3RhcnRzLXdpdGgiLCIka2V5IiwiMTIxOTU0MTE2MTIxMzA1Ny9PRkZMSU5FX1RSQU5TRkVSLzE1OTM2ODg1MTE4ODMi****</EncodedPolicy>
  <RequestId>9DFCF6F8-243C-40EC-8035-4B12FEFD7D011</RequestId>
  <Accessid>hObpgEXoca42****</Accessid>
  <Signature>pNVECGkyL0tl4bKXekV5ErZ****</Signature>
  <Host>//***-basic-cert.oss-cn-***.aliyuncs.com/</Host>
  <ExpireTime>1593688811881</ExpireTime>
</GetOperationOssUploadPolicyResponse>
```

`JSON` format

```
{
    "FileDir": "1219541161213157/OFFLINE_TRANSFER/159368851****", 
    "EncodedPolicy": "eyJleHBpcmF0aW9uIjoiMjAaMC0wNy0wMlQxKToyMDoxMS44ODRaIiwiY29uZGl0aW9ucyI6W1siY29udGVudC1sZW5ndGgtcmFuZ2UiLDAsNTI0Mjg4MDBdLFsic3RhcnRzLXdpdGgiLCIka2V5IiwiMTIxOTU0MTE2MTIxMzA1Ny9PRkZMSU5FX1RSQU5TRkVSLzE1OTM2ODg1MTE4ODMi****", 
    "RequestId": "9DFCF6F8-243C-40EC-8035-4B12FEFD7D011", 
    "Accessid": "hObpgEXoca42****", 
    "Signature": "pNVECGkyL0tl4bKXekV5ErZ****", 
    "Host": "//***-basic-cert.oss-cn-***.aliyuncs.com/", 
    "ExpireTime": "1593688811881"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

