# SubmitEmailVerification

Sends a verification email to one or more email addresses.

## Description

After a verification email is received, you must log on to your email server and click the link in the verification email within three days. If the verification email has expired, you can call the ResendEmailVerification operation to send a new email for verification.For more information, see [ResendEmailVerification](~~67734~~).

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SubmitEmailVerification&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SubmitEmailVerification|The operation that you want to perform. Set the value to **SubmitEmailVerification**. |
|Email|String|Yes|aaa@test.com|The email address that you want to verify. Separate multiple email addresses with commas \(,\). |
|SendIfExist|Boolean|No|false|Specifies whether to send a new email when a verification email exists. Valid values:

 -   **true**
-   **false**

 Default value: **false**. |
|Lang|String|No|en|The language of the error message to return. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that you use to send a verification email. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|ExistList|Array| |The information about the email address where a verification email exists. |
|Code|String|SendTokenQuotaExceeded|The code returned for the request. |
|Email|String|aaa@test.com|The email address that you attempted to verify. |
|Message|String|The maximum number of attempts allowed to send the email verification link is exceeded.|The message returned for the request. |
|FailList|Array| |The information about the email address to which a verification email failed to be sent. |
|Code|String|SendTokenQuotaExceeded|The code returned for the request. |
|Email|String|bbb@test.com|The email address that you attempted to verify. |
|Message|String|The maximum number of attempts allowed to send the email verification link is exceeded|The message returned for the request. |
|SuccessList|Array| |The information about the email address to which a verification email was sent. |
|Code|String|Success|The code returned for the request. |
|Email|String|ccc@test.com|The email address that you attempted to verify. |
|Message|String|Success|The message returned for the request. |
|RequestId|String|E2A8A5EF-DF8A-4C48-8FD4-9F6BD71AB26D|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/? Action=SubmitEmailVerification
&Email=aaa@test.com
&<Common request parameters>
```

Sample success responses

`XML` format

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

`JSON` format

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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

