# SaveBatchTaskForCreatingOrderRedeem

Submits a task for redeeming multiple domain names.

You can call the [QueryTaskDetailList](~~67710~~) operation to query the running result of the task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveBatchTaskForCreatingOrderRedeem&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveBatchTaskForCreatingOrderRedeem|The operation that you want to perform. Set the value to **SaveBatchTaskForCreatingOrderRedeem**. |
|UsePromotion|Boolean|No|false|Specifies whether to use coupons. Valid values:

 -   **false**: Coupons are not used.
-   **true**: Coupons are used. |
|PromotionNo|String|No|123213123|The ID of the coupon that you want to use. |
|OrderRedeemParam.N.DomainName|String|No|Aliyun.com|The domain name that you want to redeem. If you want to redeem multiple domain names, specify this parameter by using a domain name list. You can call the [QueryDomainList](~~69362~~) to query the domain name list. |
|OrderRedeemParam.N.CurrentExpirationDate|Long|No|000000|The time when the domain name expires. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|UseCoupon|Boolean|No|false|Specifies whether to use vouchers. Valid values:

 -   **false**: Vouchers are not used.
-   **true**: Vouchers are used. |
|CouponNo|String|No|123123|The ID of the voucher that you want to use. |
|Lang|String|No|en|The language of the error message returned. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to submit the task. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|F51977F9-2B40-462B-BCCD-CF5BB1E9DB56|The ID of the request. |
|TaskNo|String|d3babb0a-c939-4c25-8c65-c47b65f5492a|The ID of the task that was submitted. |

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

Sample success responses

`XML` format

```
<SaveBatchTaskForCreatingOrderRedeemResponse>
      <TaskNo>d3babb0a-c939-4c25-8c65-c47b65f5492a</TaskNo>
      <RequestId>F51977F9-2B40-462B-BCCD-CF5BB1E9DB56</RequestId>
</SaveBatchTaskForCreatingOrderRedeemResponse>
```

`JSON` format

```
{    
  "TaskNo": "d3babb0a-c939-4c25-8c65-c47b65f5492a",
  "RequestId": "F51977F9-2B40-462B-BCCD-CF5BB1E9DB56"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

