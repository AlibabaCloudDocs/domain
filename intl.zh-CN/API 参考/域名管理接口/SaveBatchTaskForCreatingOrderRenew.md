# SaveBatchTaskForCreatingOrderRenew

调用SaveBatchTaskForCreatingOrderRenew提交批量域名续费任务。

## API描述

任务执行结果请通过[QueryTaskDetailList](~~67710~~)接口查询。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveBatchTaskForCreatingOrderRenew&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveBatchTaskForCreatingOrderRenew|系统规定参数。取值：**SaveBatchTaskForCreatingOrderRenew**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|CouponNo|String|否|12312412|代金券编号。 |
|UseCoupon|Boolean|否|false|是否使用代金券。取值：

 -   **false**：不使用。
-   **true**：使用。 |
|PromotionNo|String|否|123123123|优惠券编号。 |
|UsePromotion|Boolean|否|false|是否使用优惠券。取值：

 -   **false**：不使用。
-   **true**：使用。 |
|OrderRenewParam.N.SubscriptionDuration|Integer|是|1|续费年限。默认为**1**年。范围为**1**~**10**年。 |
|OrderRenewParam.N.DomainName|String|是|Aliyun.com|域名，如涉及多个域名时该项传入域名列表。域名列表可通过[QueryDomainList](~~67712~~)接口获取。 |
|OrderRenewParam.N.CurrentExpirationDate|Long|是|1522080000000|域名当前到期日，计算方式为UTC时间1970年1月1日0点距离域名当前到期日的毫秒数。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|F51977F9-2B40-462B-BCCD-CF5BB1E9DB56|请求ID。 |
|TaskNo|String|d3babb0a-c939-4c25-8c65-c47b65f5492a|任务编号。 |

## 示例

请求示例

```
http://domain.aliyuncs.com/?Action=SaveBatchTaskForCreatingOrderRenew
&OrderRenewParam.1.DomainName=test1.com
&OrderRenewParam.1.SubscriptionDuration=1
&OrderRenewParam.1.CurrentExpirationDate=0000
&OrderRenewParam.2.DomainName=test2.com
&OrderRenewParam.2.SubscriptionDuration=2
&OrderRenewParam.2.CurrentExpirationDate=0000
&<公共请求参数>
```

正常返回示例

`XML`格式

```
HTTP/1.1 200 OK
Content-Type:application/xml

<SaveBatchTaskForCreatingOrderRenewResponse>
    <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
    <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
</SaveBatchTaskForCreatingOrderRenewResponse>
```

`JSON`格式

```
HTTP/1.1 200 OK
Content-Type:application/json

{
  "requestId" : "9DFBA504-3C59-427D-907D-B6C61F2A3A27",
  "taskNo" : "2daff10d-c284-4b98-a6f4-796148116b2b"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

