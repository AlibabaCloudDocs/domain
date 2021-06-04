# SaveSingleTaskForCreatingOrderRenew

Submits a task for renewing a domain name.

## Description

You can call the [QueryTaskDetailList](~~67710~~) operation to query the running result of the task.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForCreatingOrderRenew&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveSingleTaskForCreatingOrderRenew|The operation that you want to perform. Set the value to **SaveSingleTaskForCreatingOrderRenew**. |
|CurrentExpirationDate|Long|Yes|0000|The time when the domain name expires. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|DomainName|String|Yes|Aliyun.com|The domain name that you want to renew. |
|SubscriptionDuration|Integer|Yes|1|The renewal duration. Valid values: **1** to **10**. Unit: year. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to submit the task. Set the value to **127.0.0.1**. |
|Lang|String|No|en|The language of the error message returned. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |
|CouponNo|String|No|123123|The ID of the voucher that you want to use. |
|UseCoupon|Boolean|No|false|Specifies whether to use vouchers. Valid values:

-   **false**: Vouchers are not used.
-   **true**: Vouchers are used. |
|PromotionNo|String|No|123132|The ID of the coupon that you want to use. |
|UsePromotion|Boolean|No|false|Specifies whether to use coupons. Valid values:

-   **false**: Coupons are not used.
-   **true**: Coupons are used. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|The ID of the request. |
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|The ID of the task that was submitted. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=SaveSingleTaskForCreatingOrderRenew
&CurrentExpirationDate=0000
&DomainName=test.com
&SubscriptionDuration=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<SaveSingleTaskForCreatingOrderRenewResponse>
      <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
      <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
</SaveSingleTaskForCreatingOrderRenewResponse>
```

`JSON` format

```
{
  "requestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528",
  "taskNo": "9f7a509f-f347-4430-969b-52ed6d23e58f"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

