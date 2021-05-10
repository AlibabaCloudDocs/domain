# SubmitOperationCredentials

调用SubmitOperationCredentials提交自助业务待审核的证件资料。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SubmitOperationCredentials&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SubmitOperationCredentials|系统规定参数。取值：**SubmitOperationCredentials**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|AuditRecordId|Long|否|1|审核记录ID。 |
|RegType|Integer|否|1|域名持有者类型。取值：

 -   **1**：个人。
-   **2**：企业。 |
|AuditType|Integer|否|1|审核类型。取值：

 **1**：线下转移域名。 |
|Credentials|String|否|\[\{"credentialType":"SHSQB",""credentialUrl":"11212121/1212d\*\*/sqb.jpg"\},\{"credentialType":"SFZZM",""credentialUrl":"11212121/1212d\*\*/sfzzm.jpg"\}\]|待审核的证件资料信息。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|9DFCF6F8-243C-40EC-8035-4B12FEFX7D98|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=SubmitOperationCredentials&AuditRecordId=1&RegType=1&AuditType=1&Credentials=[{"credentialType":"SHSQB",""credentialUrl":"11212121/1212d**/sqb.jpg"},{"credentialType":"SFZZM",""credentialUrl":"11212121/1212d**/sfzzm.jpg"}]
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SubmitOperationCredentialsResponse>
  <RequestId>9DFCF6F8-243C-40EC-8035-4B12FEFX7D98</RequestId>
</SubmitOperationCredentialsResponse>
```

`JSON` 格式

```
{"RequestId":"9DFCF6F8-243C-40EC-8035-4B12FEFX7D98"}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

