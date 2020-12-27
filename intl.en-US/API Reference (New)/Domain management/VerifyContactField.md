# VerifyContactField

Verifies the information of a domain name contact. Whether some parameters are required is subject to the requirements of the relevant domain name registry.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=VerifyContactField&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|VerifyContactField|The operation that you want to perform. Set the value to **VerifyContactField**. |
|Province|String|No|Beijing|The province where the domain name contact is located, in English. |
|TelArea|String|No|86|The international telephone code of the country or region where the domain name contact is located. For example, the international telephone code of China is **86**. |
|Telephone|String|No|13800000000|The phone number of the domain name contact. |
|City|String|No|Beijing|The city where the domain name contact is located, in English. |
|RegistrantOrganization|String|No|Zhang San|The English name of the domain name registrant. |
|Country|String|No|CN|The code of the country or region where the domain name contact is located, such as **CN**and **US**. |
|RegistrantName|String|No|Zhang San|The English name of the domain name contact. |
|Address|String|No|Rd. Xitucheng|The address of the domain name contact, in English. |
|Email|String|No|test@test.com|The email address of the domain name contact. |
|PostalCode|String|No|10000|The postal code of the region where the domain name contact is located. |
|ZhProvince|String|No|北京|The province where the contact is located, in Chinese.

**Note:** This parameter applies only to the Alibaba Cloud China site \(aliyun.com\). |
|RegistrantType|String|No|1|The type of the domain name registrant. Valid values:

-   **1**: individual
-   **2**: enterprise |
|TelExt|String|No|01|The extension number of the phone number of the domain name contact. |
|ZhRegistrantOrganization|String|No|张三|The Chinese name of the domain name registrant.

**Note:** This parameter applies only to the Alibaba Cloud China site \(aliyun.com\). |
|ZhRegistrantName|String|No|张三|The Chinese name of the domain name contact.

**Note:** This parameter applies only to the Alibaba Cloud China site \(aliyun.com\). |
|DomainName|String|No|Aliyun.com|The domain name whose contact information you want to verify. |
|ZhAddress|String|No|西土城路|The address of the domain name contact, in Chinese.

**Note:** This parameter applies only to the Alibaba Cloud China site \(aliyun.com\). |
|ZhCity|String|No|北京市|The city where the domain name contact is located, in Chinese.

**Note:** This parameter applies only to the Alibaba Cloud China site \(aliyun.com\). |
|Lang|String|No|en|The language of the error message returned. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to verify the information of the domain name contact. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|ABAC3BAC-FCFA-4DAE-B47C-FA4105CB07C6|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/?Action=VerifyContactField
&<Common request parameters>
```

Sample success responses

`XML` format

```
<VerifyContactFieldResponse>
    <RequestId>ABAC3BAC-FCFA-4DAE-B47C-FA4105CB07C6</RequestId>
</VerifyContactFieldResponse>
```

`JSON` format

```
{
    "RequestId":"ABAC3BAC-FCFA-4DAE-B47C-FA4105CB07C6"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

