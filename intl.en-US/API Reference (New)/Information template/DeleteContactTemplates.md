# DeleteContactTemplates

Deletes multiple registrant profiles at a time.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=DeleteContactTemplates&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteContactTemplates|The operation that you want to perform. Set the value to DeleteContactTemplates. |
|RegistrantProfileIds|String|Yes|1234567|The IDs of the registrant profiles to be deleted.

The system automatically generates an ID after a registrant profile is created. You can call the [QueryRegistrantProfiles](~~67701~~) operation to query the ID of a created registrant profile. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to delete registrant profiles. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|4D73432C-7600-4779-ACBB-C3B5CA145D32|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/?Action=DeleteContactTemplates
&RegistrantProfileIds=1234567
&<Common request parameters>
```

Sample success responses

`XML` format

```
<DeleteContactTemplatesResponse>
  <RequestId>4D73432C-7600-4779-ACBB-C3B5CA145D32</RequestId>
</DeleteContactTemplatesResponse>
```

`JSON` format

```
{
    "RequestId": "4D73432C-7600-4779-ACBB-C3B5CA145D32"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

