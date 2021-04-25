# SetDefaultRegistrantProfile

Sets a registrant profile as the default profile.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SetDefaultRegistrantProfile&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SetDefaultRegistrantProfile|The operation that you want to perform. Set the value to **SetDefaultRegistrantProfile**. |
|RegistrantProfileId|Long|Yes|1234567|The ID of the registrant profile to be set as the default profile.

The system automatically generates an ID after a registrant profile is created. You can call the [QueryRegistrantProfiles](~~67701~~) operation to query the ID of a created registrant profile. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to set the default profile. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|4D73432C-7600-4779-ACBB-C3B5CA145D32|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/?Action=SetDefaultRegistrantProfile
&RegistrantProfileId=1234567
&<Common request parameters>
```

Sample success responses

`XML` format

```
<SetDefaultRegistrantProfileResponse>
  <RequestId>4D73432C-7600-4779-ACBB-C3B5CA145D32</RequestId>
</SetDefaultRegistrantProfileResponse>
```

`JSON` format

```
{
    "RequestId": "4D73432C-7600-4779-ACBB-C3B5CA145D32"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

