# QueryDomainList

Queries the domain names within your Alibaba Cloud account by page.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryDomainList&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryDomainList|The operation that you want to perform. Set the value to **QueryDomainList**. |
|EndExpirationDate|Long|No|1522080000000|The end of the time range to query domain names based on expiration dates. This value is a UNIX timestamp that indicates the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. Only queries by day are supported. |
|StartExpirationDate|Long|No|1522080000000|The beginning of the time range to query domain names based on expiration dates. This value is a UNIX timestamp that indicates the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. Only queries by day are supported. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to send the request. Set the value to **127.0.0.1**. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|QueryType|String|No|1|The category of the domain names that you want to query. Valid values:

 -   **1**: the domain names that need to be renewed
-   **2**: the domain names that need to be redeemed |
|StartRegistrationDate|Long|No|1522080000000|The beginning of the time range to query domain names based on registration dates. This value is a UNIX timestamp that indicates the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. Only queries by day are supported. |
|EndRegistrationDate|Long|No|1522080000000|The end of the time range to query domain names based on registration dates. This value is a UNIX timestamp that indicates the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. Only queries by day are supported. |
|DomainName|String|No|test.com|The domain name that you want to search for. |
|OrderByType|String|No|ASC|The order of the domain name-related information, such as the registration date and expiration date. Valid values:

 -   **ASC**: ascending order
-   **DESC:** descending order

**Note:** If this parameter is not specified, the default value is **DESC**. |
|OrderKeyType|String|No|RegistrationDate|The sequence number of the connection. Valid values:

 -   **RegistrationDate**: The domain names are sorted by registration date.
-   **ExpirationDate**: The domain names are sorted by expiration date.

 **Note:** If this parameter is not specified, the domain names are sorted by the time when they were added to the database of the verification authority. |
|ProductDomainType|String|No|New gTLD|The type of domain names. Valid values:

 -   **New gTLD**: new generic top-level domain names
-   **gTLD**: generic top-level domain names
-   **ccTLD**: country code top-level domain names |
|PageNum|Integer|Yes|1|The number of the page to return |
|PageSize|Integer|Yes|10|The number of entries to return on each page. |
|DomainGroupId|String|No|123456|The ID of the domain name group. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|PrePage|Boolean|false|Indicates whether the current page follows another page. |
|CurrentPageNum|Integer|0|The page number of the returned page. |
|RequestId|String|B7AB5469-5E38-4AA9-A920-C65B7A9C8E6E|The ID of the request. |
|PageSize|Integer|5|The number of entries returned per page. |
|TotalPageNum|Integer|1|The total number of pages returned. |
|Data|Array of Domain| |The domain names returned. |
|Domain| | | |
|DomainAuditStatus|String|FAILED|The status of the real-name verification for the domain name. Valid values:

 -   **FAILED**: The real-name verification fails.
-   **SUCCEED**: The real-name verification succeeds.
-   **NONAUDIT**: The real-name verification is not performed.
-   **AUDITING**: The information about the real-name verification is being reviewed. |
|DomainGroupId|String|123456|The ID of the domain name group. |
|Remark|String|Test|The remarks on the domain name. |
|DomainGroupName|String|Test group|The name of the domain name group. |
|RegistrationDate|String|Nov 02,2017 04:00:45|The time when the domain name was registered. |
|InstanceId|String|ST20151102120031118|The instance ID of the domain name. |
|DomainName|String|test.com|The domain name that you searched. |
|ExpirationDateStatus|String|1|Indicates whether the domain name expires. Valid values:

 -   **1**: The domain name is not expired.
-   **2**: The domain name is expired. |
|ExpirationDate|String|Nov 02,2019 04:00:45|The date and time when the domain name expires. |
|RegistrantType|String|1|The registration type of the domain name. Valid values:

 -   **1**: registered by an individual
-   **2**: registered by an enterprise |
|ExpirationDateLong|Long|1522080000000|The validity period of the domain name. This value is a UNIX timestamp that indicates the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. |
|ExpirationCurrDateDiff|Integer|-30|The number of days between the expiration date of the domain name and the current date. |
|Premium|Boolean|true|Indicates whether the domain name is premium. |
|RegistrationDateLong|Long|1522080000000|Indicates how long the domain name has been registered. This value is a UNIX timestamp that indicates the number of milliseconds that have elapsed since January 1, 1970, 00:00:00 UTC. |
|ProductId|String|2a|The product ID. |
|DomainStatus|String|3|The status of the domain name. Valid values:

 -   **1**: The domain name needs to be renewed.
-   **2**: The domain name needs to be redeemed.
-   **3**: The domain name is in a normal state. |
|DomainType|String|gTLD|The type of the domain name. Valid values:

 -   **New gTLD**
-   **gTLD**
-   **ccTLD** |
|TotalItemNum|Integer|1|The total number of domain names returned. |
|NextPage|Boolean|false|Indicates whether the current page is followed by another page. |

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
HTTP/1.1 200 OK
Content-Type:application/xml

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
HTTP/1.1 200 OK
Content-Type:application/json

{
  "Data" : {
    "Domain" : [ {
      "ExpirationDate" : "Nov 02,2019 04:00:45",
      "InstanceId" : "ST2015110212003800001928",
      "RegistrationDate" : "Nov 02,2017 04:00:45",
      "DomainName" : "fds234sdf.net",
      "DomainType" : "gTLD"
    } ]
  },
  "TotalItemNum" : 1,
  "PageSize" : 5,
  "CurrentPageNum" : 0,
  "RequestId" : "77F90DA6-89AB-4074-80F3-E595CB57DF98",
  "PrePage" : false,
  "TotalPageNum" : 1,
  "NextPage" : false
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

