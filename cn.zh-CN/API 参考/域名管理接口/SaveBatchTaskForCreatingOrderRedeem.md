# SaveBatchTaskForCreatingOrderRedeem

调用SaveBatchTaskForCreatingOrderRedeem提交批量域名赎回任务。

任务执行结果请通过[查询任务详情列表](~~67710~~)接口来查询。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveBatchTaskForCreatingOrderRedeem&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveBatchTaskForCreatingOrderRedeem|系统规定参数。取值：**SaveBatchTaskForCreatingOrderRedeem**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。 |
|CouponNo|String|否|123123|代金券编号。 |
|UseCoupon|Boolean|否|false|是否使用代金券。取值：

 -   **false**：不使用。
-   **true**：使用。 |
|PromotionNo|String|否|123213123|优惠券编号。 |
|UsePromotion|Boolean|否|false|是否使用优惠券。取值：

 -   **false**：不使用。
-   **true**：使用。 |
|OrderRedeemParam.N.DomainName|String|是|Aliyun.com|域名，如涉及多个域名时该项传入域名列表。域名列表可通过[QueryDomainList](~~67712~~)接口获取。 |
|OrderRedeemParam.N.CurrentExpirationDate|Long|是|000000|域名当前到期日，计算方式为UTC时间1970年1月1日0点距离域名当前到期日的毫秒数。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|F51977F9-2B40-462B-BCCD-CF5BB1E9DB56|唯一请求识别码。 |
|TaskNo|String|d3babb0a-c939-4c25-8c65-c47b65f5492a|任务编号。 |

## 示例

请求示例

```
http://domain.aliyuncs.com/?Action=SaveBatchTaskForCreatingOrderRedeem
&OrderRedeemParam.1.DomainName=test1.com
&OrderRedeemParam.1.CurrentExpirationDate=000000
&OrderRedeemParam.2.DomainName=test2.com
&OrderRedeemParam.2.CurrentExpirationDate=000000
&OrderRedeemParam.3.DomainName=test3.com
&OrderRedeemParam.3.CurrentExpirationDate=000000
&<公共请求参数>
```

正常返回示例

`XML`格式

```
HTTP/1.1 200 OK
Content-Type:application/xml

<?xml version='1.0' encoding='UTF-8'?>
<SaveBatchTaskForCreatingOrderRedeemResponse>
    <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
    <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
</SaveBatchTaskForCreatingOrderRedeemResponse>
```

`JSON`格式

```
HTTP/1.1 200 OK
Content-Type:application/json

{
  "TaskNo" : "d3babb0a-c939-4c25-8c65-c47b65f5492a",
  "RequestId" : "F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

