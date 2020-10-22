# DeleteRegistrantProfile

Deletes a registrant profile.

**Note:** If the request is successful, the system deletes the specified registrant profile.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=DeleteRegistrantProfile&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteRegistrantProfile|The operation that you want to perform. Set the value to **DeleteRegistrantProfile**. |
|RegistrantProfileId|Long|Yes|3600000|The ID of the registrant profile to be deleted. You can call the QueryRegistrantProfiles operation to query the ID of a created registrant profile. For more information, see [QueryRegistrantProfiles](~~67701~~). |
|Lang|String|No|en|The language of the error message to return. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that you use to delete the registrant profile. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|C50E41A0-09F1-4491-8DB8-AF55BD2D0CC8|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/? Action=DeleteRegistrantProfile
&RegistrantProfileId=3600000
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteRegistrantProfileResponse>
      <RequestId>C50E41A0-09F1-4491-8DB8-AF55BD2D0CC8</RequestId>
</DeleteRegistrantProfileResponse>
```

`JSON` format

```
{
  "RequestId": "C50E41A0-09F1-4491-8DB8-AF55BD2D0CC8"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

