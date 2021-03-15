# QueryChangeLogList

Queries the operations logs of a domain name.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryChangeLogList&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryChangeLogList|The operation that you want to perform. Set the value to QueryChangeLogList. |
|PageNum|Integer|Yes|1|The number of the page to return. The minimum value is **1**. |
|PageSize|Integer|Yes|1|The number of entries to return on each page. Valid values: **1** to**100**. |
|StartDate|Long|No|1522080000000|The beginning of the time range to query the operations logs. The timestamp follows the UNIX time format. It is the number of milliseconds that have elapsed since 00:00:00 Thursday, 1 January 1970. |
|EndDate|Long|No|1522080000000|The end of the time range to query the operations logs. The timestamp follows the UNIX time format. It is the number of milliseconds that have elapsed since 00:00:00 Thursday, 1 January 1970. |
|DomainName|String|No|example.com|The domain name whose operations logs you want to query. |
|Lang|String|No|en|The language in which the system returns the error message. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to query the operations logs. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CurrentPageNum|Integer|1|The page number of the returned page. |
|Data|Array of ChangeLog| |The details of the operations logs. |
|ChangeLog| | | |
|Details|String|dns1;dns2 -\> dns3;dns4|The details of Domain Name System \(DNS\) servers. |
|DomainName|String|test1.com|The domain name of the operations logs that were queried. |
|Operation|String|DNS modification|The operation recorded in the operations log. |
|OperationIPAddress|String|127.0.0.1|The IP address of the operation recorded in the operations log. |
|Result|String|Failed|The operation result. |
|Time|String|2017-12-26 12:00:00|The time of the operation recorded in the operations log. The time must be in UTC, for example, 2017-12-25 12:00:00. The specific format is related to the Lang response parameter. |
|NextPage|Boolean|true|Indicates whether the current page is followed by another page. |
|PageSize|Integer|1|The number of entries returned per page. |
|PrePage|Boolean|false|Indicates whether the current page follows another page. |
|RequestId|String|2DEDFF32-7827-46B1-BE90-3DB8ABD91A58|The ID of the request. |
|ResultLimit|Boolean|true|Indicates whether the number of queried operations logs exceeds the upper limit. The server can process up to 1,000 entries during the query. If the value of the **ResultLimit** parameter is **true**, the number of entries exceeds 1,000. In this case, you must narrow down the time range to query. Otherwise, the value of the **ResultLimit** parameter is **false**. |
|TotalItemNum|Integer|1000|The total number of entries returned. |
|TotalPageNum|Integer|1000|The total number of pages returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/? Action=QueryChangeLogList
&PageNum=1
&PageSize=1
&<Common request parameters>
```

Sample success responses

`XML` format

```
<PrePage>false</PrePage>
<CurrentPageNum>1</CurrentPageNum>
<PageSize>1</PageSize>
<RequestId>2DEDFF32-7827-46B1-BE90-3DB8ABD91A58</RequestId>
<TotalPageNum>1000</TotalPageNum>
<Data>
    <ChangeLog>
        <OperationIPAddress>127.0.0.1</OperationIPAddress>
        <Details>dns1;dns2 -&amp;gt; dns3;dns4</Details>
        <DomainName>test1.com</DomainName>
        <Time>2017-12-26 12:00:00</Time>
        <Operation>DNS modification</Operation>
        <Result>Failed</Result>
    </ChangeLog>
</Data>
<ResultLimit>true</ResultLimit>
<TotalItemNum>1000</TotalItemNum>
<NextPage>true</NextPage>
```

`JSON` format

```
{
    "PrePage": false,
    "CurrentPageNum": 1,
    "PageSize": 1,
    "RequestId": "2DEDFF32-7827-46B1-BE90-3DB8ABD91A58",
    "TotalPageNum": 1000,
    "Data": {
        "ChangeLog": {
            "OperationIPAddress": "127.0.0.1",
            "Details": "dns1;dns2 -&gt; dns3;dns4",
            "DomainName": "test1.com",
            "Time": "2017-12-26 12:00:00",
            "Operation": "DNS modification",
            "Result": "Failed"
        }
    },
    "ResultLimit": true,
    "TotalItemNum": 1000,
    "NextPage": true
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

