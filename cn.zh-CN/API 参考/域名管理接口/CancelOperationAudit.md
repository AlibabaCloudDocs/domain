# CancelOperationAudit

调用CancelOperationAudit取消自助业务审核。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=CancelOperationAudit&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CancelOperationAudit|系统规定参数。取值：**CancelOperationAudit**。 |
|AuditRecordId|Long|是|1|审核记录ID。您可以通过[QueryOperationAuditInfoList](~~172568~~)接口查询审核记录ID。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|9KFCF6F8-243C-40EC-8035-4B12KKFD7D90|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=CancelOperationAudit
&AuditRecordId=1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CancelOperationAuditResponse>
  <RequestId>9KFCF6F8-243C-40EC-8035-4B12KKFD7D90</RequestId>
</CancelOperationAuditResponse>
```

`JSON` 格式

```
{"RequestId":"9KFCF6F8-243C-40EC-8035-4B12KKFD7D90"}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

