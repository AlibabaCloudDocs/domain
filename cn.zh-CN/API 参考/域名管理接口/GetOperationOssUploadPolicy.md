# GetOperationOssUploadPolicy

调用GetOperationOssUploadPolicy获取审核资料的存储信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=GetOperationOssUploadPolicy&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetOperationOssUploadPolicy|系统规定参数。取值：**GetOperationOssUploadPolicy**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|AuditType|Integer|否|1|审核类型。取值：

 **1**：线下转移域名。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Accessid|String|hObpgEXoca42\*\*\*\*|访问ID。 |
|EncodedPolicy|String|eyJleHBpcmF0aW9uIjoiMjAaMC0wNy0wMlQxKToyMDoxMS44ODRaIiwiY29uZGl0aW9ucyI6W1siY29udGVudC1sZW5ndGgtcmFuZ2UiLDAsNTI0Mjg4MDBdLFsic3RhcnRzLXdpdGgiLCIka2V5IiwiMTIxOTU0MTE2MTIxMzA1Ny9PRkZMSU5FX1RSQU5TRkVSLzE1OTM2ODg1MTE4ODMi\*\*\*\*|加密策略。 |
|ExpireTime|String|1593688811881|过期时间。 |
|FileDir|String|1219541161213157/OFFLINE\_TRANSFER/159368851\*\*\*\*|文件地址。 |
|Host|String|//\*\*\*-basic-cert.oss-cn-\*\*\*.aliyuncs.com/|OSS Endpoint。 |
|RequestId|String|9DFCF6F8-243C-40EC-8035-4B12FEFD7D011|请求ID。 |
|Signature|String|pNVECGkyL0tl4bKXekV5ErZ\*\*\*\*|签名数据。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=GetOperationOssUploadPolicy
&<公共请求参数>
```

正常返回示例

`XML` 格式

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

`JSON` 格式

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

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

