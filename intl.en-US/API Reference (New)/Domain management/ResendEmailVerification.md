# ResendEmailVerification

Sends a new verification email to one or more email addresses.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=ResendEmailVerification&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|ResendEmailVerification|The operation that you want to perform. Set the value to **ResendEmailVerification**. |
|Email|String|Yes|test1@aliyun.com,test2@aliyun.com|The email address to which you want to send a new verification email. Separate multiple email addresses with commas \(,\). |
|Lang|String|No|en|The language of the error message to return. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that you use to send a new verification email. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|FailList|Array| |The information about the email address to which a new verification email failed to be sent. |
|Code|String|SendTokenQuotaExceeded|The code returned for the request. |
|Email|String|test1@aliyun.com|The email address to which you attempted to send a new verification email. |
|Message|String|The maximum number of attempts allowed to send the email verification link is exceeded.|The message returned for the request. |
|SuccessList|Array| |The information about the email address to which a new verification email was sent. |
|Code|String|Success|The code returned for the request. |
|Email|String|test2@aliyun.com|The email address to which you attempted to send a new verification email. |
|Message|String|Success|The message returned for the request. |
|RequestId|String|0EA54E99-DB48-4CE3-A099-6ED8E451B8AC|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/? Action=ResendEmailVerification
&Email=test1@aliyun.com,test2@aliyun.com
&<Common request parameters>
```

Sample success responses

`XML` format

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

`JSON` format

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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

