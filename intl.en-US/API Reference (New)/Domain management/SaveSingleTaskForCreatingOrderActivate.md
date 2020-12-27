# SaveSingleTaskForCreatingOrderActivate

Submits a task for registering a domain name.

## Description

To register a domain name, you must specify the domain name, domain name registrant, and Domain Name System \(DNS\) server. You can specify the domain name registrant by specifying the ID of a registrant profile or manually entering the information about the registrant. By default, Alibaba Cloud DNS servers are used. You can also use custom DNS servers.

You can call the [QueryTaskDetailList](~~67710~~)operation to query the running result of the task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForCreatingOrderActivate&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveSingleTaskForCreatingOrderActivate|The operation that you want to perform. Set the value to **SaveSingleTaskForCreatingOrderActivate**. |
|DomainName|String|Yes|test.com|The domain name that you want to register.

 **Note:** You must specify the domain name registrant when you register a domain name. The domain name fails to be registered if no domain name registrant is specified. You can use the **RegistrantProfileId**parameter to specify a registrant profile. You can also use parameters such as **RegistrantType**and **ZhRegistrantOrganization**to define a domain name registrant. |
|RegistrantProfileId|Long|No|123|The ID of the registrant profile. The profile includes information such as the name of the domain name registrant, the contact for the domain name, phone number, and email address. We recommend that you use a registrant profile to specify the domain name registrant when you register a domain name. If you have created a registrant profile, you can call the [QueryRegistrantProfiles](~~67701~~)operation to query the ID of the registrant profile.

 **Note:** If this parameter is specified, you do not need to specify the following parameters: **RegistrantType**, **ZhRegistrantOrganization**, **ZhRegistrantName**, **ZhProvince**, **ZhCity**, **ZhAddress**, **RegistrantOrganization**, **RegistrantName**, **Province**, **City**, **Address**, **PostalCode**, **Country**, **TelArea**, **Telephone**, **TelExt**, and **Email**. |
|RegistrantType|String|No|1|The type of the domain name registrant. Valid values:

 -   **1**: individual
-   **2**: enterprise or organization

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|ZhRegistrantOrganization|String|No|Test|The Chinese name of the domain name registrant.

 **Note:** This parameter applies only to the Domains service at the Alibaba Cloud China site \(aliyun.com\). This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|ZhRegistrantName|String|No|Test|The Chinese name of the domain name contact.

 **Note:** This parameter applies only to the Domains service at the Alibaba Cloud China site \(aliyun.com\). This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|ZhProvince|String|No|北京|The province where the domain name registrant is located, in Chinese.

 **Note:** This parameter applies only to the Domains service at the Alibaba Cloud China site \(aliyun.com\). This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|ZhCity|String|No|北京市|The city where the domain name registrant is located, in Chinese.

 **Note:** This parameter applies only to the Domains service at the Alibaba Cloud China site \(aliyun.com\). This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|ZhAddress|String|No|朝阳区|The address of the domain name registrant, in Chinese.

 **Note:** This parameter applies only to the Domains service at the Alibaba Cloud China site \(aliyun.com\). This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|RegistrantOrganization|String|No|ce shi|The English name of the domain name registrant.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|RegistrantName|String|No|ce shi|The English name of the domain name contact.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|Province|String|No|bei jing|The province where the domain name registrant is located, in English.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|City|String|No|bei jing shi|The city where the domain name registrant is located, in English.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|Address|String|No|chao yang qu|The address of the domain name registrant, in English.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|PostalCode|String|No|1234567|The postal code of the region where the domain name registrant is located.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|Country|String|No|CN|The code of the country or region where the domain name registrant is located, such as **CN**.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|TelArea|String|No|86|The international telephone code of the country or region where the domain name registrant is located. For example, the international telephone code of China is **86**.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|Telephone|String|No|12345678|The phone number of the domain name registrant.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|TelExt|String|No|1234|The extension number of the phone number of the domain name registrant.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|Email|String|No|test@aliyun.com|The email address of the domain name registrant.

 **Note:** This parameter is valid and required only when the **RegistrantProfileId**parameter is not specified. Otherwise, the domain name fails to be registered. |
|AliyunDns|Boolean|No|true|Specifies whether to use Alibaba Cloud DNS servers. Valid values: **true**and **false**. Default value: **true**.

 **Note:**

-   If the value is set to **true**, do not specify the **Dns1**and **Dns2**parameters. Otherwise, the **Dns1**and **Dns2**parameters do not take effect.
-   If the value is set to **false**, specify the **Dns1**and **Dns2**parameters. |
|Dns1|String|No|ns1.aliyun.com|The custom DNS server 1.

 **Note:**

-   This parameter is valid and required only when the **AliyunDns**parameter is set to **false**.
-   Make sure that the custom DNS server is valid. Otherwise, the registration may fail. |
|Dns2|String|No|ns2.aliyun.com|The custom DNS server 2.

 **Note:**

-   This parameter is valid and required only when the **AliyunDns**parameter is set to **false**.
-   Make sure that the custom DNS server is valid. Otherwise, the registration may fail. |
|PermitPremiumActivation|Boolean|No|false|Specifies whether to allow registration of domain names that contain premium words. Valid values:

 -   **false**: The registration of domain names that contain premium words is not allowed.
-   **true**: The registration of domain names that contain premium words is allowed.

 Default value: **false**. |
|PromotionNo|String|No|123123|The ID of the coupon that you want to use. |
|SubscriptionDuration|Integer|No|1|The subscription duration of the domain name. Unit: **year**. Default value: **1**. Maximum value: **10**. |
|EnableDomainProxy|Boolean|No|false|Specifies whether to enable privacy protection for the domain name. Valid values:

 -   **true**: Privacy protection is enabled.
-   **false**: Privacy protection is disabled.

 Default value: **true**. |
|UsePromotion|Boolean|No|false|Specifies whether to use coupons. Valid values:

 -   **false**: Coupons are not used.
-   **true**: Coupons are used.

 Default value: **false**. |
|TrademarkDomainActivation|Boolean|No|false|Specifies whether to allow registration of domain names that contain trademark words.

 -   **false**: The registration of domain names that contain trademark words is not allowed.
-   **true**: The registration of domain names that contain trademark words is allowed. |
|UseCoupon|Boolean|No|false|Specifies whether to use vouchers. Valid values:

 -   **true**: Vouchers are used.
-   **false**: Vouchers are not used.

 Default value: **false**. |
|CouponNo|String|No|123456|The ID of the voucher that you want to use. By default, the value of this parameter is a string. |
|Lang|String|No|en|The language of the error message returned. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to register the domain name. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|The ID of the request. |
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|The ID of the task that was submitted. |

## Examples

Sample requests

```
http://domain.aliyuncs.com/?Action=SaveSingleTaskForCreatingOrderActivate
&RegistrantProfileId=123
&DomainName=test.com
&<Common request parameters>
```

Sample success responses

`XML` format

```
<SaveSingleTaskForCreatingOrderActivateResponse>
      <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
      <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
</SaveSingleTaskForCreatingOrderActivateResponse>
```

`JSON` format

```
{    
  "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
  "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

