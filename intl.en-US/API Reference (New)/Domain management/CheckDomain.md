# CheckDomain

Queries whether a domain name can be registered.

## Description

For more information about how to determine the validity of domain names, see [Domain name validity](~~67788~~).

**Note:** The frequency of calling the CheckDomain operation is limited. The limit is 10 queries per second \(QPS\) for a single user and 100 QPS for this operation in total.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=CheckDomain&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|CheckDomain|The operation that you want to perform. Set the value to **CheckDomain**. |
|DomainName|String|Yes|test\*\*.xin|The domain name that you want to query. |
|FeeCommand|String|No|create|The operation command. Valid values:

-   **create**: Purchase a domain name.
-   **renew**: Renew a domain name.
-   **transfer**: Transfer a domain name to Alibaba Cloud.
-   **restore**: Redeem a domain. |
|FeeCurrency|String|No|USD|The type of the currency. Valid values:

-   **CNY**: Chinese Yuan
-   **USD**: United States dollar |
|FeePeriod|Integer|No|1|The subscription duration of the domain name. Unit: **Year**. Valid values: **1** to **10**. |
|Lang|String|No|en|The language of the error message returned. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Avail|String|1|Indicates whether the domain name can be registered. Valid values:

-   **1**: The domain name can be registered.
-   **3**: The domain name can be preregistered.
-   **4**: The preregistration of the domain name can be deleted.
-   **0**: The domain name cannot be registered.
-   **-1**: The domain name is abnormal.
-   **-2**: The registration of the domain name is suspended.
-   **-3**: The domain name is added to a blacklist. |
|DomainName|String|test\*\*.xin|The domain name that is queried. |
|DynamicCheck|Boolean|true|Indicates whether the price of the domain name is determined by the domain name registry. Valid values:

-   **true**: The price of the domain name is determined by the domain name registry.
-   **false**: The price of the domain name is not determined by the domain name registry. |
|Premium|String|true|Indicates whether the domain name is a premium domain name. Valid values:

-   **true**: The domain name is a premium domain name.
-   **false**: The domain name is not a premium domain name. |
|Price|Long|1286|The registration price of a premium domain name. |
|Reason|String|In use|The reason returned by the domain name registry for the domain name that cannot be registered.

**Note:** The reasons vary based on domain name registries. |
|RequestId|String|BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/?Action=CheckDomain
&DomainName=test**.xin
&<Common request parameters>
```

Sample success responses

`XML` format

```
<CheckDomain>
      <RequestId>BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1</RequestId>
      <DomainName>test**.xin</DomainName>
      <Avail>1</Avail>
      <Premium>false</Premium>
      <Reason></Reason>
      <Price>1286</Price>
</CheckDomain>
```

`JSON` format

```
{
    "RequestId": "BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1",
    "DomainName": "test**.xin",
    "Avail": 1,
    "Premium": false,
    "Reason": "",
    "Price": 1286
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

