# QueryEmailVerification

调用QueryEmailVerification查询邮箱验证结果。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryEmailVerification&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryEmailVerification|系统规定参数，取值：**QueryEmailVerification**。 |
|Email|String|否|abc@aliyun.com|待查询的邮箱。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认值为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|ConfirmIp|String|42.\*.\*.31|完成邮箱验证的电脑IP地址。 |
|Email|String|abc@aliyun.com|查询到的邮箱。 |
|EmailVerificationNo|String|72b36ba0572e423bbb3f19640896\*\*\*\*|邮箱验证编号（默认为系统自动生成的流水号）。 |
|GmtCreate|String|2019-02-19 16:38:07|数据库记录的邮箱创建时间。 |
|GmtModified|String|2019-02-19 16:40:38|数据库记录的邮箱更新时间。 |
|RequestId|String|FC4F7D02-8A83-4E37-B935-2D48A1B8423E|唯一请求识别码。 |
|SendIp|String|42.\*.\*.115|用户发起邮件验证的IP地址。 |
|TokenSendTime|String|2019-02-19 16:38:07|邮箱验证Token的发送时间。 |
|UserId|String|140692647406\*\*\*\*|用户ID。 |
|VerificationStatus|Integer|1|邮箱验证状态。取值：

 -   **0**：等待验证。
-   **1**：验证成功。 |
|VerificationTime|String|2019-02-19 16:40:38|完成邮箱验证的具体时间。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=QueryEmailVerification
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<QueryEmailVerificationResponse>
  <ConfirmIp>42.*.*.31</ConfirmIp>
  <TokenSendTime>2019-02-19 16:38:07</TokenSendTime>
  <Email>abc@aliyun.com</Email>
  <RequestId>FC4F7D02-8A83-4E37-B935-2D48A1B8423E</RequestId>
  <VerificationStatus>1</VerificationStatus>
  <SendIp>42.*.*.115</SendIp>
  <VerificationTime>2019-02-19 16:40:38</VerificationTime>
  <EmailVerificationNo>72b36ba0572e423bbb3f19640896****</EmailVerificationNo>
  <UserId>140692647406****</UserId>
  <GmtCreate>2019-02-19 16:38:07</GmtCreate>
  <GmtModified>2019-02-19 16:40:38</GmtModified>
</QueryEmailVerificationResponse>
```

`JSON` 格式

```
{
	"ConfirmIp": "42.*.*.31",
	"TokenSendTime": "2019-02-19 16:38:07",
	"Email": "abc@aliyun.com",
	"RequestId": "FC4F7D02-8A83-4E37-B935-2D48A1B8423E",
	"VerificationStatus": 1,
	"SendIp": "42.*.*.115",
	"VerificationTime": "2019-02-19 16:40:38",
	"EmailVerificationNo": "72b36ba0572e423bbb3f19640896****",
	"UserId": "140692647406****",
	"GmtCreate": "2019-02-19 16:38:07",
	"GmtModified": "2019-02-19 16:40:38"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

