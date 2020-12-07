# SubmitEmailVerification

调用SubmitEmailVerification接口发送邮箱验证邮件。

## API描述

收到验证邮件后您需要在3天内登录邮箱完成验证。如果验证邮件已过期，您可以调用[ResendEmailVerification](~~67734~~)接口重新发送验证邮件。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SubmitEmailVerification&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SubmitEmailVerification|系统规定参数，取值：**SubmitEmailVerification**。 |
|Email|String|是|aaa@test.com|需要完成验证的邮箱，多个邮箱之间使用英文逗号（,）隔开。 |
|SendIfExist|Boolean|否|false|验证邮件已经存在时是否重新发送邮件。取值：

 -   **true**：重新发送验证邮件。
-   **false**：不重新发送验证邮件。

 默认值为**false**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认值为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为127.0.0.1。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|ExistList|Array| |验证邮件已经存在列表。 |
|Code|String|SendTokenQuotaExceeded|返回code。 |
|Email|String|aaa@test.com|验证邮箱。 |
|Message|String|The maximum number of attempts allowed to send the email verification link is exceeded.|返回信息。 |
|FailList|Array| |验证邮件发送失败列表。 |
|Code|String|SendTokenQuotaExceeded|返回code。 |
|Email|String|bbb@test.com|验证邮箱。 |
|Message|String|The maximum number of attempts allowed to send the email verification link is exceeded|返回信息。 |
|SuccessList|Array| |验证邮件发送成功列表。 |
|Code|String|Success|返回code。 |
|Email|String|ccc@test.com|验证邮箱。 |
|Message|String|Success|返回信息。 |
|RequestId|String|E2A8A5EF-DF8A-4C48-8FD4-9F6BD71AB26D|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=SubmitEmailVerification
&Email=aaa@test.com
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SubmitEmailVerificationResponse>
  <existList>
        <email>aaa@test.com</email>
  </existList>
  <failList>
        <code>SendTokenQuotaExceeded</code>
        <email>bbb@test.com</email>
        <message>The maximum number of attempts allowed to send the email verification link is exceeded.</message>
  </failList>
  <requestId>E2A8A5EF-DF8A-4C48-8FD4-9F6BD71AB26D</requestId>
  <successList>
        <email>ccc@test.com</email>
  </successList>
  <successList>
        <email>ddd@test.com</email>
  </successList>
</SubmitEmailVerificationResponse>
```

`JSON` 格式

```
{
  "existList": [
    {
      "email": "aaa@test.com"
    }
  ],
  "failList": [
    {
      "code": "SendTokenQuotaExceeded",
      "email": "bbb@test.com",
      "message": "The maximum number of attempts allowed to send the email verification link is exceeded."
    }
  ],
  "requestId": "E2A8A5EF-DF8A-4C48-8FD4-9F6BD71AB26D",
  "successList": [
    {
      "email": "ccc@test.com"
    },
    {
      "email": "ddd@test.com"
    }
  ]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

