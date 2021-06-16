# SaveBatchTaskForCreatingOrderRedeem

Submits a task for redeeming multiple domain names.

You can call the [QueryTaskDetailList](~~67710~~) operation to query the task execution result.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveBatchTaskForCreatingOrderRedeem&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveBatchTaskForCreatingOrderRedeem|The operation that you want to perform. Set the value to **SaveBatchTaskForCreatingOrderRedeem**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to send the request. Set the value to **127.0.0.1**. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|CouponNo|String|No|123123|The ID of the voucher that you want to use. |
|UseCoupon|Boolean|No|false|Specifies whether to use vouchers. Valid values:

 -   **false**: Do not use vouchers.
-   **true**: Use vouchers. |
|PromotionNo|String|No|123213123|The ID of the coupon that you want to use. |
|UsePromotion|Boolean|No|false|Specifies whether to use coupons. Valid values:

 -   **false**: Do not use coupons.
-   **true**: Use coupons. |
|OrderRedeemParam.N.DomainName|String|Yes|Aliyun.com|The domain name that you want to redeem. If you want to redeem multiple domain names, specify this parameter by using a domain name list. You can call the [QueryDomainList](~~67712~~) to query the domain name list. |
|OrderRedeemParam.N.CurrentExpirationDate|Long|Yes|000000|The time when the domain name expires. This value is a UNIX timestamp that indicates the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|F51977F9-2B40-462B-BCCD-CF5BB1E9DB56|The ID of the request. |
|TaskNo|String|d3babb0a-c939-4c25-8c65-c47b65f5492a|The ID of the task. |

## Examples

Sample requests

```
http://domain.aliyuncs.com/?Action=SaveBatchTaskForCreatingOrderRedeem
&OrderRedeemParam.1.DomainName=test1.com
&OrderRedeemParam.1.CurrentExpirationDate=000000
&OrderRedeemParam.2.DomainName=test2.com
&OrderRedeemParam.2.CurrentExpirationDate=000000
&OrderRedeemParam.3.DomainName=test3.com
&OrderRedeemParam.3.CurrentExpirationDate=000000
&<Common request parameters>
```

Sample success response

`XML` format

```
HTTP/1.1 200 OK
Content-Type:application/xml

<?xml version='1.0' encoding='UTF-8'?>
<SaveBatchTaskForCreatingOrderRedeemResponse>
    <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
    <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
</SaveBatchTaskForCreatingOrderRedeemResponse>
```

`JSON` format

```
HTTP/1.1 200 OK
Content-Type:application/json

{
  "TaskNo" : "d3babb0a-c939-4c25-8c65-c47b65f5492a",
  "RequestId" : "F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

