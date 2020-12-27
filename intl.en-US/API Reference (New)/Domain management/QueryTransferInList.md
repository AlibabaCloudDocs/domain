# QueryTransferInList

Queries the domain names that are transferred to Alibaba Cloud.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer automatically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryTransferInList&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryTransferInList|The operation that you want to perform. Set the value to **QueryTransferInList**. |
|PageNum|Integer|Yes|1|The number of the page to return. |
|PageSize|Integer|Yes|20|The number of entries to return on each page. |
|SimpleTransferInStatus|String|No|INIT|The transfer status of the domain name. Valid values:

-   **INIT**: The transfer application is submitted.
-   **AUTHORIZATION**: The transfer is being authorized through email verification.
-   **NAME\_VERIFICATION**: The naming format of the domain name is being verified.
-   **PASSWORD\_VERIFICATION**: The transfer key is being verified.
-   **PENDING**: The domain name is being transferred.
-   **SUCCESS**: The domain name is transferred.
-   **FAIL**: The domain name fails to be transferred. |
|DomainName|String|No|Aliyun.com|The domain name that you want to transfer to Alibaba Cloud. Fuzzy match by prefix is supported. |
|SubmissionStartDate|Long|No|1514428524669|The beginning of the time range to submit the domain names that you want to transfer to Alibaba Cloud. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|SubmissionEndDate|Long|No|1514428524669|The end of the time range to submit the domain names that you want to transfer to Alibaba Cloud. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|Lang|String|No|en|The language of the error message returned. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that is used to query the domain names that are transferred to Alibaba Cloud. Set the value to **127.0.0.1**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CurrentPageNum|Integer|1|The page number of the returned page. |
|Data|Array of TransferInInfo| |The information of the domain names that are transferred to Alibaba Cloud. |
|TransferInInfo| | | |
|DomainName|String|test.com|The domain name. |
|Email|String|test@test.com|The email address to which the confirmation email for domain name transfer is sent. |
|ExpirationDate|String|2018-03-28 00:41:42|The time when the domain name transfer expired. The time follows the ISO 8601 standard in the yyyy-MM-ddThh:mm:ss format. The time is displayed in UTC. |
|ExpirationDateLong|Long|1514428524669|The timestamp when the domain name transfer expired. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|InstanceId|String|S20181T0WLI85212|The instance ID of the domain name that you queried. |
|ModificationDate|String|2018-03-28 00:41:42|The time when the transfer information was updated. |
|ModificationDateLong|Long|1514428524669|The timestamp when the transfer information was updated. |
|NeedMailCheck|Boolean|true|Indicates whether email verification is performed. Valid values:

-   **true**: Email verification is performed.
-   **false**: Email verification is not performed. |
|ProgressBarType|Integer|0|The type of the transfer progress bar. Valid values:

-   **0**: Both email verification and naming format verification are required.
-   **1**: Only email verification is required.
-   **2**: Only naming format verification is required.
-   **3**: Email verification and naming format verification are not required. |
|ResultCode|String|clientCancelled|The code returned when the transfer fails. Valid values:

-   **clientCancelled**: You cancel the domain name transfer request.
-   **clientRejected**: The original registrar of the domain name rejects the domain name transfer request, or you cancel the transfer request.
-   **serverCancelled**: The domain name registry cancels the transfer.
-   **transferProhibited**: The domain name is prohibited from the transfer.
-   **transferExpired**: You do not complete the relevant transfer confirmation within the validity period.
-   **nameVerificationFailed**: The domain name fails the naming format verification.
-   **transferSubmitted**: Another user has submitted a transfer request for the domain name. |
|ResultDate|String|2018-03-28 00:41:42|The time when the transfer succeeded or failed. The time follows the ISO 8601 standard in the yyyy-MM-ddThh:mm:ssZ format. The time is displayed in UTC. |
|ResultDateLong|Long|1514428524669|The timestamp when the transfer succeeded or failed. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|ResultMsg|String|You canceled the domain name transfer request.|The description of the cause for the transfer failure. |
|SimpleTransferInStatus|String|FAIL|The transfer status of the domain name. Valid values:

-   **INIT**: The transfer application is submitted.
-   **AUTHORIZATION**: The transfer is being authorized through email verification.
-   **NAME\_VERIFICATION**: The naming format of the domain name is being verified.
-   **PASSWORD\_VERIFICATION**: The transfer key is being verified.
-   **PENDING**: The domain name is being transferred.
-   **SUCCESS**: The domain name is transferred.
-   **FAIL**: The domain name fails to be transferred. |
|Status|Integer|11|The detailed transfer status of the domain name. Valid values:

-   **10**: The domain name is purchased but the transfer request is not submitted.
-   **11**: The token link for email verification is sent.
-   **19**: The token link verification succeeds.
-   **20**: The request for the naming format verification is submitted.
-   **21**: The naming format verification fails.
-   **29**: The naming format verification succeeds.
-   **31**: The transfer key is invalid.
-   **39**: The transfer request is submitted.
-   **50**: The transfer request is canceled.
-   **51**: The transfer fails.
-   **52**: The transfer expires.
-   **59**: The transfer succeeds. |
|SubmissionDate|String|2018-03-28 00:41:42|The time when the transfer request was submitted. The time follows the ISO 8601 standard in the yyyy-MM-ddThh:mm:ssZ format. The time is displayed in UTC. |
|SubmissionDateLong|Long|1514428524669|The timestamp when the transfer request was submitted. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|TransferAuthorizationCodeSubmissionDate|String|2018-03-28 00:41:42|The time when the transfer key was submitted. The time follows the ISO 8601 standard in the yyyy-MM-ddThh:mm:ssZ format. The time is displayed in UTC. |
|TransferAuthorizationCodeSubmissionDateLong|Long|1514428524669|The timestamp when the transfer key was submitted. This value is a UNIX timestamp representing the number of milliseconds that have elapsed since the epoch time January 1, 1970, 00:00:00 UTC. |
|UserId|String|123456|The ID of the user who initiated the domain name transfer request. |
|WhoisMailStatus|Boolean|true|Indicates whether the email address of the domain name registrant is captured by using WHOIS. If the domain name transfer is in the AUTHORIZATION state, and this parameter is set to **false**, the email address of the domain name registrant is not captured by using WHOIS. The capture must be manually processed. |
|NextPage|Boolean|true|Indicates whether the current page is followed by another page. |
|PageSize|Integer|20|The number of entries returned per page. |
|PrePage|Boolean|false|Indicates whether the current page follows another page. |
|RequestId|String|AF7D4DCE-0776-47F2-A9B2-6FB85A87AA60|The ID of the request. |
|TotalItemNum|Integer|40|The total number of entries returned. |
|TotalPageNum|Integer|2|The total number of pages returned. |

## Examples

Sample requests

```
http(s)://[Endpoint]/?Action=QueryTransferInList
&PageNum=1
&PageSize=20
&<Common request parameters>
```

Sample success responses

`XML` format

```
<QueryTransferInListResponse>
    <Data>
        <TransferInInfo>
            <Status>31</Status>
            <Email>te****st@alibaba-inc.com</Email>
            <ResultMsg>TransferInFailureReason.null</ResultMsg>
            <SimpleTransferInStatus>PASSWORD_VERIFICATION</SimpleTransferInStatus>
            <InstanceId>S20182G180111111</InstanceId>
            <ModificationDate>2018-03-29 16:31:02</ModificationDate>
            <DomainName>test.com</DomainName>
            <WhoisMailStatus>true</WhoisMailStatus>
            <UserId>123456</UserId>
            <ProgressBarType>0</ProgressBarType>
            <ExpirationDate>2018-04-13 15:51:01</ExpirationDate>
            <NeedMailCheck>true</NeedMailCheck>
            <SubmissionDate>2018-03-29 15:51:01</SubmissionDate>
        </TransferInInfo>
        <TransferInInfo>
            <InstanceId>S20182G151111111</InstanceId>
            <WhoisMailStatus>true</WhoisMailStatus>
            <UserId>123456</UserId>
            <ResultDate>2018-03-29 15:47:37</ResultDate>
            <ExpirationDate>2018-04-13 14:57:11</ExpirationDate>
            <NeedMailCheck>true</NeedMailCheck>
            <Status>50</Status>
            <Email>b****i4@test.com</Email>
            <SimpleTransferInStatus>FAIL</SimpleTransferInStatus>
            <ResultMsg>You have canceled this domain name transfer in. </ResultMsg>
            <ModificationDate>2018-03-29 15:47:37</ModificationDate>
            <ResultCode>clientCancelled</ResultCode>
            <DomainName>btest.com</DomainName>
            <ProgressBarType>0</ProgressBarType>
            <SubmissionDate>2018-03-29 14:57:11</SubmissionDate>
        </TransferInInfo>
    </Data>
    <TotalItemNum>87</TotalItemNum>
    <PageSize>2</PageSize>
    <CurrentPageNum>1</CurrentPageNum>
    <RequestId>041FEBFE-966C-452E-A21D-38FBE520B93D</RequestId>
    <PrePage>false</PrePage>
    <TotalPageNum>44</TotalPageNum>
    <NextPage>true</NextPage>
</QueryTransferInListResponse>
```

`JSON` format

```
{
    "CurrentPageNum":1,
    "Data":{
        "TransferInInfo":[
            {
                "DomainName":"test.com",
                "Email":"te****st@alibaba-inc.com",
                "ExpirationDate":"2018-04-13 15:51:01",
                "InstanceId":"S20182G180111111",
                "ModificationDate":"2018-03-29 15:59:02",
                "NeedMailCheck":true,
                "ProgressBarType":0,
                "ResultMsg":"TransferInFailureReason.null",
                "SimpleTransferInStatus":"PASSWORD_VERIFICATION",
                "Status":31,
                "SubmissionDate":"2018-03-29 15:51:01",
                "UserId":"123456",
                "WhoisMailStatus":true
            },
            {
                "DomainName":"btest.com",
                "Email":"b****i4@test.com",
                "ExpirationDate":"2018-04-13 14:57:11",
                "InstanceId":"S20182G15000000",
                "ModificationDate":"2018-03-29 15:47:37",
                "NeedMailCheck":true,
                "ProgressBarType":0,
                "ResultCode":"clientCancelled",
                "ResultDate":"2018-03-29 15:47:37",
                "ResultMsg":"You have canceled this domain name transfer in.",
                "SimpleTransferInStatus":"FAIL",
                "Status":50,
                "SubmissionDate":"2018-03-29 14:57:11",
                "UserId":"123456",
                "WhoisMailStatus":true
            }
        ]
    },
    "NextPage":true,
    "PageSize":2,
    "PrePage":false,
    "RequestId":"CC71762B-0A20-4D3A-AD74-C225DB8DBEAE",
    "TotalItemNum":87,
    "TotalPageNum":44
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

