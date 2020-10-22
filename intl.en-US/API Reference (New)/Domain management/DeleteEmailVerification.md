# DeleteEmailVerification

Deletes one or more verified email addresses.

**Note:** After you delete a verified email address from your registrant information, you must verify the email address again if you need to add the email address to your registrant information.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=DeleteEmailVerification&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteEmailVerification|The operation that you want to perform. Set the value to **DeleteEmailVerification**. |
|Email|String|Yes|test1@aliyun.com,test2@aliyun.com|The email address that you want to delete. Separate multiple email addresses with commas \(,\). |
|Lang|String|No|en|The language of the error message to return. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that you use to delete one or more verified email addresses. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|FailList|Array| |The information about the email address that failed to be deleted. |
|Code|String|ParameterIllegall|The code returned for the request. |
|Email|String|test1@aliyun.com|The email address that you attempted to delete. |
|Message|String|Parameter error|The message returned for the request. |
|SuccessList|Array| |The information about the email address that was deleted. |
|Code|String|Success|The code returned for the request. |
|Email|String|test2@aliyun.com|The email address that you attempted to delete. |
|Message|String|Success|The message returned for the request. |
|RequestId|String|7A3D0E4A-0D4B-4BD0-90D7-A61DF8DD26AE|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/? Action=DeleteEmailVerification
&Email=test1@aliyun.com,test2@aliyun.com
&<Common request parameters>
```

Sample success responses

`XML` format

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

`JSON` format

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

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

