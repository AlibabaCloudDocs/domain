# ResendEmailVerification

调用ResendEmailVerification接口重新发送验证邮件。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=ResendEmailVerification&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ResendEmailVerification|系统规定参数，取值：**ResendEmailVerification**。 |
|Email|String|是|test1@aliyun.com,test2@aliyun.com|待重新获取验证邮件的邮箱，多个邮箱之间使用英文逗号（,）隔开。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认值为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为127.0.0.1。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|FailList|Array| |验证邮件发送失败列表。 |
|Code|String|SendTokenQuotaExceeded|返回code。 |
|Email|String|test1@aliyun.com|验证邮箱。 |
|Message|String|The maximum number of attempts allowed to send the email verification link is exceeded.|返回信息。 |
|SuccessList|Array| |验证邮件发送成功列表。 |
|Code|String|Success|返回code。 |
|Email|String|test2@aliyun.com|验证邮箱。 |
|Message|String|Success|返回信息。 |
|RequestId|String|0EA54E99-DB48-4CE3-A099-6ED8E451B8AC|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=ResendEmailVerification
&Email=test1@aliyun.com,test2@aliyun.com
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<ResendEmailVerificationResponse>
  <failList>
        <code>SendTokenQuotaExceeded</code>
        <email>test1@aliyun.com</email>
        <message>The maximum number of attempts allowed to send the email verification link is exceeded.</message>
  </failList>
  <failList>
        <code>ParameterIllegall</code>
        <email>test2@aliyun.com</email>
        <message>Parameter error</message>
  </failList>
  <requestId>0EA54E99-DB48-4CE3-A099-6ED8E451B8AC</requestId>
</ResendEmailVerificationResponse>
```

`JSON` 格式

```
{
  "failList": [
    {
      "code": "SendTokenQuotaExceeded",
      "email": "test1@aliyun.com",
      "message": "The maximum number of attempts allowed to send the email verification link is exceeded."
    },
    {
      "code": "ParameterIllegall",
      "email": "test2@aliyun.com",
      "message": "Parameter error"
    }
  ],
  "requestId": "0EA54E99-DB48-4CE3-A099-6ED8E451B8AC",
  "successList": []
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

