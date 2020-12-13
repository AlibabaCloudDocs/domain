# SaveSingleTaskForCreatingOrderRenew

调用SaveSingleTaskForCreatingOrderRenew提交域名续费任务。

## API描述

任务执行结果请通过[QueryTaskDetailList](~~67710~~)接口查询。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForCreatingOrderRenew&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveSingleTaskForCreatingOrderRenew|系统规定参数。取值：**SaveSingleTaskForCreatingOrderRenew**。 |
|CurrentExpirationDate|Long|是|0000|域名当前的到期时间，计算方式为UTC时间1970年1月1日0点距离域名当前到期时间的毫秒数。 |
|DomainName|String|是|Aliyun.com|需要续费的域名。 |
|SubscriptionDuration|Integer|是|1|续费年限值，范围：**1**年~**10**年。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|CouponNo|String|否|123123|代金券编号。 |
|UseCoupon|Boolean|否|false|是否使用代金券。取值：

 -   **false**：不使用。
-   **true**：使用。 |
|PromotionNo|String|否|123132|优惠券编号。 |
|UsePromotion|Boolean|否|false|是否使用优惠券。取值：

 -   **false**：不使用。
-   **true**：使用。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|请求ID。 |
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|任务编号。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=SaveSingleTaskForCreatingOrderRenew
&CurrentExpirationDate=0000
&DomainName=test.com
&SubscriptionDuration=1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SaveSingleTaskForCreatingOrderRenewResponse>
      <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
      <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
</SaveSingleTaskForCreatingOrderRenewResponse>
```

`JSON` 格式

```
{
  "requestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528",
  "taskNo": "9f7a509f-f347-4430-969b-52ed6d23e58f"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

