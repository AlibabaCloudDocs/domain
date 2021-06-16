# QueryOperationAuditInfoList

Queries review records of self-service operations.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryOperationAuditInfoList&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryOperationAuditInfoList|The operation that you want to perform. Set the value to **QueryOperationAuditInfoList**. |
|PageSize|Integer|Yes|20|The number of entries to return on each page. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |
|DomainName|String|No|xxxx.com|The domain name for which you want to query review records. |
|AuditType|Integer|No|1|The type of the operation that triggers the review. Valid values:

**1**: offline transfer of domain names |
|AuditStatus|Integer|No|1|The status of the review. Valid values:

-   **0**: waiting for materials
-   **1**, **2**, **3**, and **4**: reviewing
-   **5**: failed
-   **6**: successful
-   **7**: canceled |
|PageNum|Integer|No|1|The number of the page to return. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CurrentPageNum|Integer|2|The page number of the returned page. |
|Data|Array| |The data of a review record. |
|AuditInfo|String|\{"regType":1,"registrantName":"Zhang San","telephone":"1390123\*\*\*\*","account":"zhangsan@alimail.com","reason":1,"remark":"The account is lost."\}|The reviewed information. |
|AuditStatus|Integer|1|The status of the review. Valid values:

-   **0**: waiting for materials
-   **1**, **2**, **3**, and **4**: reviewing
-   **5**: failed
-   **6**: successful
-   **7**: canceled |
|AuditType|Integer|1|The type of the operation that triggers the review. Valid values:

**1**: offline transfer of domain names |
|BusinessName|String|Offline transfer of domain names such as xxx.com|The name of the reviewed operation. |
|CreateTime|Long|1581919010101|The time when the record was created. |
|DomainName|String|xxx.com,yyy.com|The domain name for which the operation was performed. |
|Id|Long|1|The ID of the review record. |
|Remark|String|Reviewing|The remarks of the review. |
|UpdateTime|Long|1581919010101|The time when the record was updated. |
|NextPage|Boolean|true|Indicates whether the current page is followed by another page. |
|PageSize|Integer|20|The number of entries returned per page. |
|PrePage|Boolean|true|Indicates whether the current page follows another page. |
|RequestId|String|9DFCF6F8-243C-40EC-8035-4B12FEFD7D48|The ID of the request. |
|TotalItemNum|Integer|199|The total number of entries returned. |
|TotalPageNum|Integer|10|The total number of pages returned. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/?Action=QueryOperationAuditInfoList
&PageSize=20
&<Common request parameters>
```

Sample success responses

`XML` format

```
<QueryOperationAuditInfoListResponse>
  <PrePage>true</PrePage>
  <CurrentPageNum>2</CurrentPageNum>
  <RequestId>9DFCF6F8-243C-40EC-8035-4B12FEFD7D48</RequestId>
  <PageSize>20</PageSize>
  <TotalPageNum>10</TotalPageNum>
  <Data>
        <AuditInfo>{"regType":1,"registrantName":"Zhang San","telephone":"1390123****","account":"zhangsan@alimail.com","reason":1,"remark":"The account is lost."}</AuditInfo>
        <AuditStatus>1</AuditStatus>
        <BusinessName>Offline transfer of domain names such as xxx.com</BusinessName>
        <DomainName>xxx.com,yyy.com</DomainName>
        <AuditType>1</AuditType>
        <CreateTime>1581919010101</CreateTime>
        <UpdateTime>1581919010101</UpdateTime>
        <Id>1</Id>
        <Remark>Reviewing</Remark>
  </Data>
  <TotalItemNum>199</TotalItemNum>
  <NextPage>true</NextPage>
</QueryOperationAuditInfoListResponse>
```

`JSON` format

```
{
    "PrePage": "true", 
    "CurrentPageNum": "2", 
    "RequestId": "9DFCF6F8-243C-40EC-8035-4B12FEFD7D48", 
    "PageSize": "20", 
    "TotalPageNum": "10", 
    "Data": [
        {
            "AuditInfo": "{\"regType\":1,\"registrantName\":\"Zhang San\",\"telephone\":\"1390123****\",\"account\":\"zhangsan@alimail.com\",\"reason\":1,\"remark\":\"The account is lost.\"}", 
            "AuditStatus": "1", 
            "BusinessName": "Offline transfer of domain names such as xxx.com", 
            "DomainName": "xxx.com,yyy.com", 
            "AuditType": "1", 
            "CreateTime": "1581919010101", 
            "UpdateTime": "1581919010101", 
            "Id": "1", 
            "Remark": "Reviewing"
        }
    ], 
    "TotalItemNum": "199", 
    "NextPage": "true"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

