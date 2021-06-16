# QueryOperationAuditInfoDetail

Queries the details of a review record.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryOperationAuditInfoDetail&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryOperationAuditInfoDetail|The operation that you want to perform. Set the value to **QueryOperationAuditInfoDetail**. |
|AuditRecordId|Long|Yes|1|The ID of the review record. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
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
|CreateTime|Long|1581919010100|The time when the record was created. |
|DomainName|String|xxx.com,yyy.com|The domain name for which the operation was performed. |
|Id|String|1|The ID of the review record. |
|Remark|String|Approved|The remarks of the review. |
|RequestId|String|9DFCF6F8-243C-40EC-8035-4B12FEFD7D1L|The ID of the request. |
|UpdateTime|Long|1581919010101|The time when the record was updated. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/?Action=QueryOperationAuditInfoDetail
&AuditRecordId=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<QueryOperationAuditInfoDetailResponse>
  <AuditInfo>{"regType":1,"registrantName":"Zhang San","telephone":"1390123****","account":"zhangsan@alimail.com","reason":1,"remark":"The account is lost."}</AuditInfo>
  <AuditStatus>1</AuditStatus>
  <RequestId>9DFCF6F8-243C-40EC-8035-4B12FEFD7D1L</RequestId>
  <BusinessName>Offline transfer of domain names such as xxx.com</BusinessName>
  <DomainName>xxx.com,yyy.com</DomainName>
  <AuditType>1</AuditType>
  <CreateTime>1581919010100</CreateTime>
  <UpdateTime>1581919010101</UpdateTime>
  <Id>1</Id>
  <Remark>Approved</Remark>
</QueryOperationAuditInfoDetailResponse>
```

`JSON` format

```
{
    "AuditInfo": "{\"regType\":1,\"registrantName\":\"Zhang San\",\"telephone\":\"1390123****\",\"account\":\"zhangsan@alimail.com\",\"reason\":1,\"remark\":\"The account is lost.\"}", 
    "AuditStatus": "1", 
    "RequestId": "9DFCF6F8-243C-40EC-8035-4B12FEFD7D1L", 
    "BusinessName": "Offline transfer of domain names such as xxx.com", 
    "DomainName": "xxx.com,yyy.com", 
    "AuditType": "1", 
    "CreateTime": "1581919010100", 
    "UpdateTime": "1581919010101", 
    "Id": "1", 
    "Remark": "Approved"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

