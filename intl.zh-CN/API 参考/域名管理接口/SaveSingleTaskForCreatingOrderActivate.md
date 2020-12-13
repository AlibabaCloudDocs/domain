# SaveSingleTaskForCreatingOrderActivate

调用SaveSingleTaskForCreatingOrderActivate提交域名注册任务。

## API描述

注册域名需同时填写您想注册的域名、域名持有者信息及DNS。您可以通过域名信息模板编号来关联域名的持有者信息或者手动填写域名持有者信息，DNS可以默认使用阿里云DNS或者填写自定义DNS。

任务执行结果请通过[QueryTaskDetailList](~~67710~~)接口查询。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForCreatingOrderActivate&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveSingleTaskForCreatingOrderActivate|系统规定参数。取值：**SaveSingleTaskForCreatingOrderActivate**。 |
|DomainName|String|是|test.com|想要注册的域名。

 **说明：** 注册域名时必须指定域名持有者信息，不指定域名持有者信息会导致域名注册失败。您可以通过**RegistrantProfileId**参数指定信息模板定义域名持有者信息，或通过定义**RegistrantType**、**ZhRegistrantOrganization**等参数来定义域名持有者信息。 |
|RegistrantProfileId|Long|否|123|域名信息模板编号（信息模板包含域名持有者名称、域名联系人、电话、邮箱等信息），推荐填写域名信息模板编号进行域名注册。如果您已经创建了域名注册信息模板，可通过调用[QueryRegistrantProfiles](~~67701~~)接口查询域名信息模板编号。

 **说明：** 传入本参数后，无需再传入**RegistrantType**、**ZhRegistrantOrganization**、**ZhRegistrantName**、**ZhProvince**、**ZhCity**、**ZhAddress**、**RegistrantOrganization**、**RegistrantName**、**Province**、**City**、**Address**、**PostalCode**、**Country**、**TelArea**、**Telephone**、**TelExt**和**Email**参数。 |
|RegistrantType|String|否|1|域名持有者类型。取值：

 -   **1**：个人。
-   **2**：企业、组织等。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|ZhRegistrantOrganization|String|否|测试|域名持有者名称（中文）。

 **说明：** 该参数仅适用于中国站。当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|ZhRegistrantName|String|否|测试|域名联系人（中文）。

 **说明：** 该参数仅适用于中国站。当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|ZhProvince|String|否|北京|省份（中文）。

 **说明：** 该参数仅适用于中国站。当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|ZhCity|String|否|北京市|城市（中文）。

 **说明：** 该参数仅适用于中国站。当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|ZhAddress|String|否|朝阳区|详细地址（中文）。

 **说明：** 该参数仅适用于中国站。当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|RegistrantOrganization|String|否|ce shi|域名持有者名称（英文）。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|RegistrantName|String|否|ce shi|域名联系人（英文）。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|Province|String|否|bei jing|省份（英文）。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|City|String|否|bei jing shi|城市（英文）。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|Address|String|否|chao yang qu|详细地址（英文）。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|PostalCode|String|否|1234567|邮政编码。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|Country|String|否|CN|国家代码，例如**CN**。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|TelArea|String|否|86|电话国家代码，例如中国为**86**。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|Telephone|String|否|12345678|电话号码。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|TelExt|String|否|1234|分机号码。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|Email|String|否|test@aliyun.com|电子邮箱。

 **说明：** 当未传入**RegistrantProfileId**参数时，本参数才可用且必须传入，如果不传入会导致域名注册失败。 |
|AliyunDns|Boolean|否|true|是否使用阿里云DNS，取值为**true**\|**false**，默认为**true**。

 **说明：**

-   取值为**true**时，您无需再传入**Dns1**和**Dns2**参数，否则传入的**Dns1**和**Dns2**参数不会生效。
-   取值为**false**时，您还需要传入**Dns1**和**Dns2**参数。 |
|Dns1|String|否|ns1.aliyun.com|自定义DNS1。

 **说明：**

-   当**AliyunDns**取值为**false**时，本参数才可用且必须传入。
-   请务必确保自定义DNS的正确性，否则可能导致注册失败。 |
|Dns2|String|否|ns2.aliyun.com|自定义DNS2。

 **说明：**

-   当**AliyunDns**取值为**false**时，本参数才可用且必须传入。
-   请务必确保自定义DNS的正确性，否则可能导致注册失败。 |
|PermitPremiumActivation|Boolean|否|false|是否允许注册白金词，取值：

 -   **false**：不允许。
-   **true**：允许。

 默认值为**false**。 |
|PromotionNo|String|否|123123|优惠券编号。 |
|SubscriptionDuration|Integer|否|1|购买周期，单位为**年**。默认为**1年**，最长可购买**10年**。 |
|EnableDomainProxy|Boolean|否|false|是否开启域名隐私保护服务。取值：

 -   **true**：开启。
-   **false**：不开启。

 默认值为**true**。 |
|UsePromotion|Boolean|否|false|是否使用优惠券，取值：

 -   **false**：不允许。
-   **true**：允许。

 默认值为**false**。 |
|TrademarkDomainActivation|Boolean|否|false|是否允许注册商标词，取值：

 -   **false**：不允许。
-   **true**：允许。 |
|UseCoupon|Boolean|否|false|是否使用代金券。取值：

 -   **true**：使用
-   **false**：不使用

 默认值为**false**。 |
|CouponNo|String|否|123456|代金券编号，默认为字符串。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|唯一请求识别码。 |
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|任务编号。 |

## 示例

请求示例

```
http://domain.aliyuncs.com/?Action=SaveSingleTaskForCreatingOrderActivate
&RegistrantProfileId=123
&DomainName=test.com
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SaveSingleTaskForCreatingOrderActivateResponse>
      <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
      <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
</SaveSingleTaskForCreatingOrderActivateResponse>
```

`JSON` 格式

```
{    
  "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
  "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

