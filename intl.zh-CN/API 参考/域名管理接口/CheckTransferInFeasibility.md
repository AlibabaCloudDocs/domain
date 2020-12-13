# CheckTransferInFeasibility

调用CheckTransferInFeasibility校验域名是否可以转入。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=CheckTransferInFeasibility&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CheckTransferInFeasibility|系统规定参数。取值：**CheckTransferInFeasibility**。 |
|DomainName|String|是|Aliyun.com|需要校验的域名。 |
|TransferAuthorizationCode|String|否|test|域名转入密码。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CanTransfer|Boolean|false|是否可以转入。取值：

 -   **true**：可以转入。
-   **false**：不可以转入。 |
|Code|String|CheckTransferResult.DomainTransferProhibited|不可转入时，返回错误代码。 |
|Message|String|This domain name is in transfer prohibited status, so it cannot be transferred. You can contact your original registrar to change its status.|不可转入时，返回错误描述。 |
|ProductId|String|2a|域名产品的编号。 |
|RequestId|String|FC0D6B89-2353-4D64-BD80-6606A7DBD7C1|唯一请求识别码。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CheckTransferInFeasibility
&DomainName=test.com
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CheckTransferInFeasibilityResponse>
    <RequestId>60D2283F-36EA-46D4-A38D-15B5A2C455E3</RequestId>
    <CanTransfer>true</CanTransfer>
    <ProductId>2a</ProductId>
</CheckTransferInFeasibilityResponse>
```

`JSON` 格式

```
{
    "CanTransfer":true,
    "ProductId":"2a",
    "RequestId":"CE82EB4C-882D-430B-A908-E0BECFC35025"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

