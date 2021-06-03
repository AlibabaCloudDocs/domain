# QueryDomainList

Queries the domain names within your account by page.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryDomainList&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryDomainList|The operation that you want to perform. Set the value to **QueryDomainList**. |
|PageNum|Integer|Yes|1|The number of the page to return. |
|PageSize|Integer|Yes|10|The number of entries to return on each page. |
|StartExpirationDate|Long|No|1522080000000|The beginning of the time range to query the expiration dates of the domain names. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. Only query by day is supported. |
|EndExpirationDate|Long|No|1522080000000|The end of the time range to query the expiration dates of the domain names. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. Only query by day is supported. |
|StartRegistrationDate|Long|No|1522080000000|The beginning of the time range to query the registration dates of the domain names. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. Only query by day is supported. |
|EndRegistrationDate|Long|No|1522080000000|The end of the time range to query the registration dates of the domain names. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. Only query by day is supported. |
|QueryType|String|No|1|The category of the domain names that you want to query. Valid values:

-   **1**: the domain names that need to be renewed
-   **2**: the domain names that need to be redeemed |
|ProductDomainType|String|No|New gTLD|The type of the domain names. Valid values:

-   **New gTLD**: new generic top-level domain
-   **gTLD**: generic top-level domain
-   **ccTLD**: country code top-level domain |
|OrderByType|String|No|ASC|The order of domain name-related business, such as registration time and expiration date. Valid values:

-   **ASC**: ascending order
-   **DESC**: descending order

**Note:** If this parameter is not specified, the default value is **DESC**. |
|DomainName|String|No|test.com|The domain name that you want to search for. |
|DomainGroupId|String|No|123456|The ID of the domain name group. You can call the [QueryDomainGroupList](~~69362~~) operation to query the ID. |
|OrderKeyType|String|No|RegistrationDate|The sorting rule of the domain names. Valid values:

-   **RegistrationDate**: The domain names are sorted by registration time.
-   **ExpirationDate**: The domain names are sorted by expiration time.

**Note:** If this parameter is not specified, the domain names are sorted by the time when they were added to the database of the verification authority. |
|Lang|String|No|en|The language of the error message returned. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to query the domain names. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CurrentPageNum|Integer|0|The page number of the returned page. |
|Data|Array of Domain| |The domain names returned. |
|Domain| | | |
|DomainAuditStatus|String|FAILED|The status of the real-name verification for the domain name. Valid values:

-   **FAILED**: The real-name verification fails.
-   **SUCCEED**: The real-name verification succeeds.
-   **NONAUDIT**: The real-name verification is not performed.
-   **AUDITING**: The information about the real-name verification is being reviewed. |
|DomainGroupId|String|123456|The ID of the domain name group. |
|DomainGroupName|String|Test group|The name of the domain name group. |
|DomainName|String|test.com|The domain name that you searched. |
|DomainStatus|String|3|The status of the domain name. Valid values:

-   **1**: The domain name needs to be renewed.
-   **2**: The domain name needs to be redeemed.
-   **3**: The domain name is in a normal state. |
|DomainType|String|gTLD|The type of the domain name. Valid values:

-   **New gTLD**
-   **gTLD**
-   **cTLD** |
|ExpirationCurrDateDiff|Integer|-30|The number of days between the expiration date of the domain name and the current date. |
|ExpirationDate|String|Nov 02,2019 04:00:45|The date and time at which the domain name expires. |
|ExpirationDateLong|Long|1522080000000|The validity period of the domain name. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|ExpirationDateStatus|String|1|The expiration status of the domain name. Valid values:

-   **1**: The domain name is not expired.
-   **2**: The domain name is expired. |
|InstanceId|String|ST20151102120031118|The instance ID of the domain name that is queried. |
|Premium|Boolean|true|Indicates whether the domain name is premium. |
|ProductId|String|2a|The product ID. |
|RegistrantType|String|1|The registration type of the domain name. Valid values:

-   **1**: individual
-   **2**: enterprise |
|RegistrationDate|String|Nov 02,2017 04:00:45|The time when the domain name was registered. |
|RegistrationDateLong|Long|1522080000000|Indicates how long the domain name has been registered. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|Remark|String|Test|The remarks on the domain name that was searched. |
|NextPage|Boolean|false|Indicates whether the current page is followed by another page. |
|PageSize|Integer|5|The number of entries returned per page. |
|PrePage|Boolean|false|Indicates whether the current page follows another page. |
|RequestId|String|B7AB5469-5E38-4AA9-A920-C65B7A9C8E6E|The ID of the request. |
|TotalItemNum|Integer|1|The total number of domain names returned. |
|TotalPageNum|Integer|1|The total number of pages that display the domain names. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=QueryDomainList
&PageNum=1
&PageSize=10
&<Common request parameters>
```

Sample success responses

`XML` format

```
<?xml version='1.0' encoding='UTF-8'?>
<QueryDomainListResponse>
    <Data>
        <Domain>
            <ExpirationDate>Nov 02,2019 04:00:45</expirationDate>
            <InstanceId>ST20151102120031118</SaleId>
            <RegistrationDate>Nov 02,2017 04:00:45</registrationDate>
            <DomainName>test.com</DomainName>
            <DomainType>gTLD</domainType>
        </Domain>
    </Data>
    <TotalItemNum>1</TotalItemNum>
    <PageSize>5</PageSize>
    <CurrentPageNum>0</CurrentPageNum>
    <RequestId>B7AB5469-5E38-4AA9-A920-C65B7A9C8E6E</RequestId>
    <PrePage>false</PrePage>
    <TotalPageNum>1</TotalPageNum>
    <NextPage>false</NextPage>
</QueryDomainListResponse>
```

`JSON` format

```
{
  "Data": {
    "Domain": [
      {
        "ExpirationDate": "Nov 02,2019 04:00:45",
        "InstanceId": "ST2015110212003800001928",
        "RegistrationDate": "Nov 02,2017 04:00:45",
        "DomainName": "fds234sdf.net",
        "DomainType": "gTLD"
      }
    ]
  },
  "TotalItemNum": 1,
  "PageSize": 5,
  "CurrentPageNum": 0,
  "RequestId": "77F90DA6-89AB-4074-80F3-E595CB57DF98",
  "PrePage": false,
  "TotalPageNum": 1,
  "NextPage": false
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

