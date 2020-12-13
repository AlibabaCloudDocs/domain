# SaveBatchTaskForCreatingOrderTransfer

调用SaveBatchTaskForCreatingOrderTransfer提交批量域名转入任务。

任务执行结果请通过查询任务详情[QueryTaskDetailList](~~67710~~)接口来查询。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveBatchTaskForCreatingOrderTransfer&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveBatchTaskForCreatingOrderTransfer|系统规定参数。取值：**SaveBatchTaskForCreatingOrderTransfer**。 |
|CouponNo|String|否|123123|代金券编号。 |
|UsePromotion|Boolean|否|false|是否使用优惠券。取值：

 -   **false**：不使用。
-   **true**：使用。 |
|OrderTransferParam.N.DomainName|String|否|test.com|域名，如涉及多个域名时该项传入域名列表。 |
|OrderTransferParam.N.AuthorizationCode|String|否|testCode|域名转入密码。多个域名时使用**list**传入。 |
|OrderTransferParam.N.RegistrantProfileId|Long|否|123456|已经实名认证的域名信息模板ID，可通过[QueryRegistrantProfileRealNameVerificationInfo](~~69359~~)接口获取。 |
|OrderTransferParam.N.PermitPremiumTransfer|Boolean|否|false|是否允许溢价词域名转入，取值

 -   **false**：允许。
-   **true**：不允许。

 默认值为**false**。 |
|PromotionNo|String|否|123123|优惠券编号。 |
|UseCoupon|Boolean|否|false|是否使用代金券。取值：

 -   **false**：不使用。
-   **true**：使用。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
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
/?Action=SaveBatchTaskForCreatingOrderTransfer
&OrderTransferParam.1.AuthorizationCode=testCode
&OrderTransferParam.1.DomainName=test.com
&OrderTransferParam.1.PermitPremiumTransfer=false
&OrderTransferParam.1.RegistrantProfileId=123456
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SaveBatchTaskForCreatingOrderTransferResponse>
    <TaskNo>3bdbaa0e-faa2-4ad2-98f4-bcfeb0237054</TaskNo>
    <RequestId>EEB28AA7-6051-4E71-B2CC-DAAFB2DF6BCA</RequestId>
</SaveBatchTaskForCreatingOrderTransferResponse>
```

`JSON` 格式

```
{
    "RequestId":"492D1868-1384-4219-8F8B-7EB44534A72A",
    "TaskNo":"939b6918-be3b-4c4f-b949-93553da52dca"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

