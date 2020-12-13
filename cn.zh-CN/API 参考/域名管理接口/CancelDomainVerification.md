# CancelDomainVerification

调用CancelDomainVerification取消域名实名认证审核。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=CancelDomainVerification&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CancelDomainVerification|系统规定参数。取值：CancelDomainVerification。 |
|ActionType|String|是|activate|操作类型。取值：

 -   **activate**：新购。
-   **renew**：续费。
-   **redeem**：赎回。 |
|InstanceId|String|是|S2019270W570xxxx|域名实例编号，通过查询域名列表[QueryDomainList](~~67712~~)接口获取。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认值为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|0AC0AF67-D303-4EB9-B20E-B4D4B2C3F97B|唯一请求识别码。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?ActionType=activate
&InstanceId=S2019270W570xxxx
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CancelDomainVerificationResponse>
  <RequestId>0AC0AF67-D303-4EB9-B20E-B4D4B2C3F97B</RequestId>
</CancelDomainVerificationResponse>
```

`JSON` 格式

```
{
  "RequestId": "0AC0AF67-D303-4EB9-B20E-B4D4B2C3F97B"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

