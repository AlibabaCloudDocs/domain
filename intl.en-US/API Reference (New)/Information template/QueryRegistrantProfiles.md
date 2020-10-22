# QueryRegistrantProfiles

Queries registrant profiles under your Alibaba Cloud account.

## Description

You can use optional request parameters to specify specific query criteria to query registrant profiles as required. For example, you can use the following optional request parameters:

-   RegistrantProfileId, which indicates the ID of a registrant profile.
-   Parameters that indicate the information about a registrant profile, such as RegistrantOrganization. You can use these parameters if you do not know the ID of the profile that you want to query.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=QueryRegistrantProfiles&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Position|Type|Required|Example|Description|
|---------|--------|----|--------|-------|-----------|
|Action|Query|String|Yes|QueryRegistrantProfiles|The operation that you want to perform. Set the value to **QueryRegistrantProfiles**. |
|RegistrantProfileId|Query|Long|No|1234567|The ID of the registrant profile that you want to query. The system generates an ID after you create a registrant profile. |
|RegistrantType|Query|String|No|1|The type of the domain name registrant. Valid values:

-   **1**: individual
-   **2**: enterprise

Default value: **1**. |
|RegistrantOrganization|Query|String|No|li si|The name of the domain name registrant. |
|Email|Query|String|No|82106\*\*\*\*@qq.com|The email address of the domain name registrant. |
|RealNameStatus|Query|String|No|SUCCEED|The status of real-name verification for the domain name registrant. Valid values:

-   **FAILED**: failed
-   **SUCCEED**: successful
-   **NONAUDIT**: not verified
-   **AUDITING**: being reviewed |
|DefaultRegistrantProfile|Query|Boolean|No|false|Specifies whether to query the default profile. Valid values:

-   **true**
-   **false**

Default value: **false**. |
|PageSize|Query|Integer|No|500|The number of entries to return on each page. Default value:**0**. Maximum value:**5000**. |
|PageNum|Query|Integer|No|1|The number of the page to return. Default value: **0**. |
|RegistrantProfileType|Query|String|No|common|The type of the registrant profile. Valid values:

-   **common**: common profile
-   **cnnic**: China Internet Network Information Center \(CNNIC\) profile

**Note:** You can create and manage a CNNIC profile only on the Alibaba Cloud international site \(alibabacloud.com\). You must use a CNNIC profile to manage specific domain names, such as .cn, from the CNNIC registrar. For other domain names, you can use a common profile. |
|Lang|Query|String|No|en|The language of the error message to return. Valid values:

-   **zh**: Chinese
-   **en**: English

Default value: **en**. |
|UserClientIp|Query|String|No|127.0.0.1|The IP address of the client that you use to query registrant profiles. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CurrentPageNum|Integer|1|The page number of the returned page. |
|NextPage|Boolean|true|Indicates whether the current page is followed by another page. Valid values:

-   **true**
-   **false** |
|TotalPageNum|Integer|1|The total number of returned pages. |
|TotalItemNum|Integer|9|The total number of returned entries.

**Note:** This parameter indicates the total number of queried registrant profiles. If multiple registrant profiles are queried, the information about these profiles is returned in sequence by profile. |
|RegistrantProfiles|Array of RegistrantProfile| |The list of registrant profiles. |
|RegistrantProfile| | | |
|Address|String|zhe jiang sheng hang zhou shi shi li qu shi li zhen shi li da sha 1001 hao|The address of the domain name registrant. |
|City|String|hang zhou shi|The city where the domain name registrant is located. |
|Country|String|CN|The code of the country or region where the domain name registrant is located,such as **CN** or **US**. |
|CreateTime|String|2019-02-18 10:46:47|The time when the registrant profile was created. |
|DefaultRegistrantProfile|Boolean|false|Indicates whether the registrant profile is the default profile. Valid values:

-   **true**
-   **false**

Default value: **false**. |
|Email|String|82106\*\*\*\*@qq.com|The email address of the domain name registrant. |
|EmailVerificationStatus|Integer|1|Indicates whether the email address has been verified. Valid values:

-   **0**: not verified
-   **1**: verified |
|PostalCode|String|310024|The zip code of the region where the domain name registrant is located. |
|Province|String|zhe jiang|The province where the domain name registrant is located. |
|RealNameStatus|String|SUCCEED|The status of real-name verification for the domain name registrant. Valid values:

-   **FAILED**: failed
-   **SUCCEED**: successful
-   **NONAUDIT**: not verified
-   **AUDITING**: being reviewed |
|RegistrantName|String|li si|The name of the contact for the domain name. |
|RegistrantOrganization|String|li si|The name of the domain name registrant. |
|RegistrantProfileId|Long|1000001|The ID of the registrant profile. |
|RegistrantProfileType|String|common|The type of the registrant profile. Valid values:

-   **common**: common profile
-   **cnnic**: CNNIC profile

**Note:** You can create and manage a CNNIC profile only on the Alibaba Cloud international site \(alibabacloud.com\). You must use a CNNIC profile to manage specific domain names, such as .cn, from the CNNIC registrar. For other domain names, you can use a common profile. |
|RegistrantType|String|1|The type of the domain name registrant. Valid values:

-   **1**: individual
-   **2**: enterprise

Default value: **1**. |
|TelArea|String|86|The calling code of the country or region where the domain name registrant is located. For example, the calling code for China is **86**. |
|TelExt|String|1234|The extension number of the registrant's phone number. |
|Telephone|String|1829756\*\*\*\*|The phone number of the domain name registrant. |
|UpdateTime|String|2019-03-15 15:32:45|The time when the registrant profile was updated. |
|PrePage|Boolean|false|Indicates whether the current page follows another page. Valid values:

-   **true**
-   **false** |
|PageSize|Integer|2|The number of entries returned per page. Default value:**0**. Maximum value:**5000**. |
|RequestId|String|94053D79-7455-4F71-BF06-20EB2DEDE6BD|The ID of the request. |

## Examples

Sample requests

```
http(s)://domain.aliyuncs.com/? Action=QueryRegistrantProfiles
&<Common request parameters>
```

Sample success responses

`XML` format

```
<QueryRegistrantProfilesResponse>
    <TotalItemNum>9</TotalItemNum>
    <PageSize>500</PageSize>
    <CurrentPageNum>1</CurrentPageNum>
    <RequestId>94053D79-7455-4F71-BF06-20EB2DEDE6BD</RequestId>
    <PrePage>false</PrePage>
    <RegistrantProfiles>
        <RegistrantProfile>
             
             
            <Telephone>1829756****</Telephone>
             
            <DefaultRegistrantProfile>false</DefaultRegistrantProfile>
            <EmailVerificationStatus>1</EmailVerificationStatus>
            <UpdateTime>2019-03-15 15:32:45</UpdateTime>
            <RealNameStatus>SUCCEED</RealNameStatus>
            <Country>CN</Country>
            <Province>zhe jiang</Province>
             
            <City>hang zhou shi</City>
            <TelArea>86</TelArea>
            <RegistrantProfileId>1000001</RegistrantProfileId>
            <PostalCode>310024</PostalCode>
            <RegistrantType>1</RegistrantType>
            <Email>82106****@qq.com</Email>
            <CreateTime>2019-02-18 10:46:47</CreateTime>
            <Address>zhe jiang sheng hang zhou shi shi li qu shi li zhen shi li da sha 1001 hao</Address>
            <RegistrantName>li si</RegistrantName>
            <RegistrantOrganization>li si</RegistrantOrganization>
            <RegistrantProfileType>common</RegistrantProfileType>
             
        </RegistrantProfile>
    </RegistrantProfiles>
    <TotalPageNum>1</TotalPageNum>
    <NextPage>false</NextPage>
</QueryRegistrantProfilesResponse>
```

`JSON` format

```
{
    "TotalItemNum": 9,
    "PageSize": 500,
    "CurrentPageNum": 1,
    "RequestId": "94053D79-7455-4F71-BF06-20EB2DEDE6BD",
    "PrePage": false,
    "RegistrantProfiles": {
        "RegistrantProfile": [
            {
                 
                 
                "Telephone": "1829756****",
                 
                "DefaultRegistrantProfile": false,
                "EmailVerificationStatus": 1,
                "UpdateTime": "2019-03-15 15:32:45",
                "RealNameStatus": "SUCCEED",
                "Country": "CN",
                "Province": "zhe jiang",
                 
                "City": "hang zhou shi",
                "TelArea": "86",
                "RegistrantProfileId":1000001,
                "PostalCode": "310024",
                "RegistrantType": "1",
                "Email": "82106****@qq.com",
                "CreateTime": "2019-02-18 10:46:47",
                "Address": "zhe jiang sheng hang zhou shi shi li qu shi li zhen shi li da sha 1001 hao",
                "RegistrantName": "li si",
                "RegistrantOrganization": "li si",
                "RegistrantProfileType": "common",
                 
            }
        ]
    },
    "TotalPageNum": 1,
    "NextPage": false
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

