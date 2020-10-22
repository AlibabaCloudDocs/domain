# QueryDomainByInstanceId

Queries the basic information about a domain name by domain name instance ID.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryDomainByInstanceId&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|QueryDomainByInstanceId|The operation that you want to perform. Set the value to**QueryDomainByInstanceId**. |
|InstanceId|String|Yes|S20131205001\*\*\*\*|The instance ID of the domain name that you want to query.

 **Note:** You can call the QueryDomainList operation to query the instance ID of a domain name. For more information, see [QueryDomainList](~~67712~~). |
|UserClientIp|String|No|127.0.0.1|The IP address of the client that you use to query the domain name. |
|Lang|String|No|en|The language of the error message to return. Valid values:

 -   **zh**: Chinese
-   **en**: English

 Default value:**en**. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|DnsList|List|dns1.hichina.com,dns2.hichina.com|The Domain Name System \(DNS\) servers of the domain name. |
|DomainName|String|test.com|The domain name that was queried. |
|DomainNameProxyService|Boolean|false|Indicates whether privacy protection is enabled for the domain name. |
|DomainNameVerificationStatus|String|NONAUDIT|The status of name auditing for the domain name. Valid values:

 -   **NONAUDIT**: not audited
-   **SUCCEED**: successful
-   **FAILED**: failed
-   **AUDITING**: being audited |
|Email|String|test@alibaba-inc.com|The email address of the domain name registrant. |
|EmailVerificationClientHold|Boolean|false|Indicates whether the domain name is in the ClientHold state, namely, domain name resolution being disabled. Valid values:

 -   **false**: Domain name resolution is not disabled.
-   **true**: Domain name resolution is disabled. |
|EmailVerificationStatus|Integer|1|Indicates whether the email address has been verified. Valid values:

 -   **0**: not verified
-   **1**: verified |
|ExpirationDate|String|2019-12-07 17:02:13|The time when the domain name expired or is about to expire. |
|ExpirationDateLong|Long|1625111915000|The timestamp when the domain name expired or is about to expire. |
|InstanceId|String|S20179H1BBI9test|The instance ID of the domain name that was queried. |
|Premium|Boolean|false|Indicates whether the domain name contains any premium words. |
|RealNameStatus|String|NONAUDIT|The status of real-name verification for the domain name. Valid values:

 -   **NONAUDIT**: not verified
-   **SUCCEED**: successful
-   **FAILED**: failed
-   **AUDITING**: being reviewed

 **Note:** A domain name is considered as verified only when both name auditing and real-name verification are successful. |
|RegistrantName|String|Test litm|The contact for the domain name. |
|RegistrantOrganization|String|Test litm|The registrant of the domain name. |
|RegistrantType|String|1|The type of the domain name registrant. Valid values:

 -   **1**: individual
-   **2**: enterprise |
|RegistrantUpdatingStatus|String|NORMAL|The status of the information about the domain name registrant. Valid values:

 -   **PENDING**: being modified
-   **NORMAL**: normal |
|RegistrationDate|String|2017-12-07 17:02:13|The time when the domain name was registered. |
|RegistrationDateLong|Long|1625111915000|The timestamp when the domain name was registered. |
|RequestId|String|23C9B3C4-9E2C-4405-A88D-BD33E459D140|The ID of the request. |
|TransferOutStatus|String|NORMAL|The status of the domain name. Valid values:

 -   **NORMAL**: normal
-   **PENDING:** being transferred out of Alibaba Cloud |
|TransferProhibitionLock|String|CLOSE|The status of the transfer lock for the domain name. Valid values:

 -   **NONE\_SETTING**: not set
-   **OPEN**: enabled
-   **CLOSE**: disabled |
|UpdateProhibitionLock|String|CLOSE|The status of the security lock for the domain name. Valid values:

 -   **NONE\_SETTING**: not set
-   **OPEN**: enabled
-   **CLOSE**: disabled |
|UserId|String|121000000test|The ID of the Alibaba Cloud account. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/? Action=QueryDomainByInstanceId
&InstanceId=S20131205001****
&<Common request parameters>
```

Sample success responses

`XML` format

```
<QueryDomainByInstanceIdResponse>
      <RegistrantInfoStatus>NORMAL</RegistrantInfoStatus>
      <TransferProhibitionLock>CLOSE</TransferProhibitionLock>
      <UpdateProhibitionLock>CLOSE</UpdateProhibitionLock>
      <InstanceId>S20179H1BBI9test</InstanceId>
      <EmailVerificationStatus>1</EmailVerificationStatus>
      <RealNameStatus>NONAUDIT</RealNameStatus>
      <DomainNameVerificationStatus>NONAUDIT</DomainNameVerificationStatus>
      <UserId>121000000test</UserId>
      <Premium>false</Premium>
      <ExpirationDate>2019-12-07 17:02:13</ExpirationDate>
      <DomainNameProxyService>false</DomainNameProxyService>
      <RegistrantType>1</RegistrantType>
      <Email>test@alibaba-inc.com</Email>
      <RegistrationDate>2017-12-07 17:02:13</RegistrationDate>
      <EmailVerificationClientHold>false</EmailVerificationClientHold>
      <DomainName>test.com</DomainName>
      <TransferOutStatus>NORMAL</TransferOutStatus>
      <RegistrantName>Test litm</RegistrantName>
      <DnsList>
            <Dns>dns1.hichina.com</Dns>
            <Dns>dns2.hichina.com</Dns>
      </DnsList>
      <RegistrantOrganization>Test litm</RegistrantOrganization>
</QueryDomainByInstanceIdResponse>
```

`JSON` format

```
{
  "dnsList": [
    "dns1.hichina.com",
    "dns2.hichina.com"
  ],
  "domainName": "test.com",
  "domainNameProxyService": false,
  "email": "test@alibaba-inc.com",
  "emailVerificationClientHold": false,
  "emailVerificationStatus": 1,
  "expirationDate": "2019-12-07 17:02:13",
  "instanceId": "S20179H1BBI9test",
  "premium": false,
  "realNameStatus": "NONAUDIT",
  "domainNameVerificationStatus": "NONAUDIT",
  "registrantInfoStatus": "NORMAL",
  "registrantName": "Test litm",
  "registrantOrganization": "Test litm",
  "registrationDate": "2017-12-07 17:02:13",
  "transferOutStatus": "NORMAL",
  "transferProhibitionLock": "CLOSE",
  "updateProhibitionLock": "CLOSE",
  "userId": "121000000test"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

