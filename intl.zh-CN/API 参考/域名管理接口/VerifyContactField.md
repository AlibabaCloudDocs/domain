# VerifyContactField

调用VerifyContactField校验域名联系人信息。部分参数是否必传将根据注册局要求而定。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=VerifyContactField&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|VerifyContactField|系统规定参数。取值：**VerifyContactField**。 |
|Province|String|否|Bei jing|省份（英文）。 |
|TelArea|String|否|86|电话国家代码，例如中国的电话国家代码为**86**。 |
|Telephone|String|否|13800000000|电话。 |
|City|String|否|Bei jing|城市（英文）。 |
|RegistrantOrganization|String|否|zhang san|域名持有者名称（英文）。 |
|Country|String|否|CN|国家代码，例如**CN**、**US**。 |
|RegistrantName|String|否|zhang san|联系人名称（英文）。 |
|Address|String|否|Rd. xitucheng|详细地址（英文）。 |
|Email|String|否|test@test.com|电子邮箱。 |
|PostalCode|String|否|10000|邮政编码。 |
|ZhProvince|String|否|北京|省份（中文）。

 **说明：** 该参数仅适用于中国站。 |
|RegistrantType|String|否|1|域名持有者类型。取值：

 -   **1**：个人。
-   **2**：企业。 |
|TelExt|String|否|01|分机号码。 |
|ZhRegistrantOrganization|String|否|张三|域名持有者名称（中文）。

 **说明：** 该参数仅适用于中国站。 |
|ZhRegistrantName|String|否|张三|联系人名称（中文）。

 **说明：** 该参数仅适用于中国站。 |
|DomainName|String|否|Aliyun.com|域名。 |
|ZhAddress|String|否|西土城路|详细地址（中文）。

 **说明：** 该参数仅适用于中国站。 |
|ZhCity|String|否|北京市|城市（中文）。

 **说明：** 该参数仅适用于中国站。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|ABAC3BAC-FCFA-4DAE-B47C-FA4105CB07C6|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=VerifyContactField
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<VerifyContactFieldResponse>
    <RequestId>ABAC3BAC-FCFA-4DAE-B47C-FA4105CB07C6</RequestId>
</VerifyContactFieldResponse>
```

`JSON` 格式

```
{
    "RequestId":"ABAC3BAC-FCFA-4DAE-B47C-FA4105CB07C6"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

