# QueryTransferInByInstanceId

You can call this operation to query the domain name transfer-in information by instance ID.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryTransferInByInstanceId&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryTransferInByInstanceId|The operation that you want to perform. Set the value to **QueryTransferInByInstanceId**. |
|InstanceId|String|Yes|S20181T0WLI85212|The instance ID of the domain name that you want to query. |
|Lang|String|No|en|The language of the error message to return. Valid values:

-   **zh:** Chinese
-   **en:** English

Default value:**en** |
|UserClientIp|String|No|127.0.0.1|The IP address of the client used by the user to initiate the query. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|DomainName|String|test.com|The domain name returned. |
|Email|String|test@test.com|The email address to which the confirmation email for domain name transfer-in was sent. |
|ExpirationDate|String|2018-03-28 00:41:42|The time when the domain name transfer-in expired. |
|ExpirationDateLong|Long|1514428524669|The timestamp when the domain name transfer-in expired. |
|InstanceId|String|S20181T0WLI85212|The instance ID of the domain name that was queried. |
|ModificationDate|String|2018-03-28 00:41:42|The time when the transfer-in information was updated. |
|ModificationDateLong|Long|1514428524669|The timestamp when the transfer-in information was updated. |
|NeedMailCheck|Boolean|true|Indicates whether email verification is required. |
|ProgressBarType|Integer|0|The type of the transfer progress bar. Valid values:

-   **0:** Both email verification and domain name auditing are required.
-   **1:** Only email verification is required.
-   **2:** Only domain name auditing is required.
-   **3:** Neither email verification nor domain name auditing is required. |
|RequestId|String|AF7D4DCE-0776-47F2-A9B2-6FB85A87AA60|The ID of the request. |
|ResultCode|String|clientCancelled|The code returned when the transfer fails. Valid values:

-   **clientCancelled:** You canceled the domain name transfer-in request.
-   **clientRejected:** The original registrar of the domain name rejected the domain name transfer-in request, or you rejected the request through the original registrar.
-   **serverCancelled:** The domain name registry canceled the transfer-in.
-   **transferProhibited:** The domain name transfer was prohibited.
-   **transferExpired:** You did not complete the relevant transfer-in confirmation within the validity period.
-   **nameVerificationFailed:** The domain name did not pass the name audit.
-   **transferSubmitted:** Another user has submitted the domain name transfer-in request. |
|ResultDate|String|2018-03-28 00:41:42|The time when the transfer succeeded or failed. |
|ResultDateLong|Long|1514428524669|The timestamp when the transfer succeeded or failed. |
|ResultMsg|String|You canceled the domain name transfer-in request.|The description of the cause for this transfer failure. |
|SimpleTransferInStatus|String|SUCCESS|The status of the domain name transfer-in. Valid values:

-   **INIT:** Submitted
-   **AUTHORIZATION:** Authorization through email verification
-   **NAME\_VERIFICATION:** Domain name audit
-   **PASSWORD\_VERIFICATION:** Transfer code verification
-   **PENDING:** In progress
-   **SUCCESS:** Succeeded
-   **FAIL:** Failed |
|Status|Integer|11|The detailed status of the domain name transfer-in. Valid values:

-   **10:** Initial state.
-   **11:** The token link for email verification has been sent.
-   **19:** The token link verification succeeded.
-   **20:** The request for a domain name audit has been submitted.
-   **21:** Domain name auditing failed.
-   **29:** Domain name auditing succeeded.
-   **31:** The transfer code is incorrect.
-   **39:** The transfer-in request is submitted successfully.
-   **50:** The customer canceled the transfer-in request.
-   **51:** The transfer-in failed.
-   **52:** The transfer-in expired.
-   **59:** The transfer-in succeeded. |
|SubmissionDate|String|2018-03-28 00:41:42|The time when the transfer request was submitted. |
|SubmissionDateLong|Long|1514428524669|The timestamp when the transfer request was submitted. |
|TransferAuthorizationCodeSubmissionDate|String|2018-03-28 00:41:42|The time when the transfer code was submitted successfully. |
|TransferAuthorizationCodeSubmissionDateLong|Long|1514428524669|The timestamp when the transfer code was submitted successfully. |
|UserId|String|123456|The ID of the user who initiated the domain name transfer-in request. |
|WhoisMailStatus|Boolean|true|Indicates whether the email address of the domain name registrant was captured through WHOIS. When the domain name transfer-in is in the state of authorization through email verification and this field is set to **false**, the email address of the domain name registrant was not captured through WHOIS, and the capture must be manually processed. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=QueryTransferInByInstanceId
&InstanceId=S20181T0WLI85212
&<Common request parameters>

```

Sample success responses

`XML` format

```
<QueryTransferInByInstanceIdResponse>
    <InstanceId>S20182F0RED000000</InstanceId>
    <WhoisMailStatus>true</WhoisMailStatus>
    <UserId>123456</UserId>
    <ResultDate>2018-03-28 09:54:39</ResultDate>
    <ExpirationDate>2018-04-12 09:51:53</ExpirationDate>
    <NeedMailCheck>true</NeedMailCheck>
    <Status>50</Status>
    <Email></Email>
    <SimpleTransferInStatus>FAIL</SimpleTransferInStatus>
    <ResultMsg>You have canceled this domain name transfer in. </ResultMsg>
    <RequestId>0D6108ED-7BB3-4898-83D0-44883DE0D3E7</RequestId>
    <ModificationDate>2018-03-28 09:54:39</ModificationDate>
    <ResultCode>clientCancelled</ResultCode>
    <DomainName>test.com</DomainName>
    <ProgressBarType>0</ProgressBarType>
    <SubmissionDate>2018-03-28 09:51:53</SubmissionDate>
</QueryTransferInByInstanceIdResponse>
```

`JSON` format

```
{
	"InstanceId":"S20182F0RED000000",
	"WhoisMailStatus":true,
	"UserId":"123456",
	"ResultDate":"2018-03-28 09:54:39",
	"ExpirationDate":"2018-04-12 09:51:53",
	"NeedMailCheck":true,
	"Status":50,
	"Email":"",
	"ResultMsg":"You have canceled this domain name transfer in.",
	"SimpleTransferInStatus":"FAIL",
	"RequestId":"B3E437A1-4947-4E4F-B9E2-9781AB1C8134",
	"ModificationDate":"2018-03-28 09:54:39",
	"ResultCode":"clientCancelled",
	"DomainName":"test.com",
	"ProgressBarType":0,
	"SubmissionDate":"2018-03-28 09:51:53"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

