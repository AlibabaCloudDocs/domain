# DeleteEmailVerification

调用DeleteEmailVerification接口删除已经验证通过的邮箱。

**说明：** 删除后如需继续使用该邮箱，您需要重新完成邮箱验证。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=DeleteEmailVerification&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteEmailVerification|系统规定参数，取值：**DeleteEmailVerification**。 |
|Email|String|是|test1@aliyun.com,test2@aliyun.com|待删除的邮箱，多个邮箱之间使用英文逗号（,）隔开。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认值为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为127.0.0.1。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|FailList|Array| |邮箱删除失败列表。 |
|Code|String|ParameterIllegall|返回code。 |
|Email|String|test1@aliyun.com|删除失败的邮箱。 |
|Message|String|Parameter error|邮箱删除失败返回的信息。 |
|SuccessList|Array| |邮箱删除成功列表。 |
|Code|String|Success|返回code。 |
|Email|String|test2@aliyun.com|删除成功的邮箱。 |
|Message|String|Success|邮箱删除成功返回的信息。 |
|RequestId|String|7A3D0E4A-0D4B-4BD0-90D7-A61DF8DD26AE|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=DeleteEmailVerification
&Email=test1@aliyun.com,test2@aliyun.com
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DeleteEmailVerificationResponse>
  <failList>
        <code>ParameterIllegall</code>
        <email>test1@aliyun.com</email>
        <message>Parameter error</message>
  </failList>
  <requestId>7A3D0E4A-0D4B-4BD0-90D7-A61DF8DD26AE</requestId>
  <successList>
        <email>test2@aliyun.com</email>
  </successList>
</DeleteEmailVerificationResponse>
```

`JSON` 格式

```
{
  "failList": [
    {
      "code": "ParameterIllegall",
      "email": "test1@aliyun.com",
      "message": "Parameter error"
    }
  ],
  "requestId": "7A3D0E4A-0D4B-4BD0-90D7-A61DF8DD26AE",
  "successList": [
    {
      "email": "test2@aliyun.com"
    }
  ]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

