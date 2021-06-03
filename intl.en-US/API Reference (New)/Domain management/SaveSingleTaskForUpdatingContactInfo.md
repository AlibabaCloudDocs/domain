# SaveSingleTaskForUpdatingContactInfo

Submits a task to modify the information of a domain name.

You can call the [QueryTaskDetailList](~~67710~~) operation to query the task execution result.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForUpdatingContactInfo&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveSingleTaskForUpdatingContactInfo|The operation that you want to perform. Set the value to **SaveSingleTaskForUpdatingContactInfo**. |
|ContactType|String|Yes|registrant|The type of the contact. Valid values:

-   **registrant**
-   **admin**
-   **billing**
-   **tech** |
|DomainName|String|Yes|test.com|The domain name whose information you want to modify. |
|RegistrantProfileId|Long|Yes|1|The ID of the registrant profile. |
|AddTransferLock|Boolean|No|false|Specifies whether to enable transfer prohibition. This parameter is valid only when the value of the **ContactType** parameter is **registrant**. It specifies whether the domain name can be transferred out within 60 days after the registrant information is modified. Default value:**false** \(no transfer prohibition\). |
|InstanceId|String|No|S123456789|The instance ID of the domain name. |
|Lang|String|No|en|The language of the error message to return. Valid values:

-   **zh:** Chinese
-   **en:** English

Default value:**en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|The ID of the request. |
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|The ID of the task that was submitted. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=SaveSingleTaskForUpdatingContactInfo
&ContactType=registrant
&DomainName=test.com
&RegistrantProfileId=1
&<Common request parameters>

```

Sample success responses

`XML` format

```
<SaveSingleTaskForUpdatingContactInfoResponse>
      <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
      <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
</SaveSingleTaskForUpdatingContactInfoResponse>
```

`JSON` format

```
{
	"TaskNo":"3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
	"RequestId":"40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

