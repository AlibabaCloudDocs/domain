# VerifyEmail

Verifies the token that was received at the email address of a domain name.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=VerifyEmail&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|VerifyEmail|The operation that you want to perform. Set the value to **VerifyEmail**. |
|Token|String|Yes|0b32247496409441e9e179ea7c2e0\*\*\*\*|The token that was received in the email.

 After a verification email is sent, you can log on to your email server and check the token in the email that you have received. |
|Lang|String|No|en|The language of the error message to return. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that you use to verify the token. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|FD3AD289-83EE-4E32-803A-CF1B3A8EEE64|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/? Action=VerifyEmail
&Token=0b32247496409441e9e179ea7c2e0****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<VerifyEmailResponse>
      <RequestId>FD3AD289-83EE-4E32-803A-CF1B3A8EEE64</RequestId>
</VerifyEmailResponse>
```

`JSON` format

```
{
    "requestId":"FD3AD289-83EE-4E32-803A-CF1B3A8EEE64"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

