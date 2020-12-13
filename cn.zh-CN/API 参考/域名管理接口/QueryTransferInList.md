# QueryTransferInList

调用QueryTransferInList查询域名转入列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryTransferInList&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryTransferInList|系统规定参数。取值：**QueryTransferInList**。 |
|PageNum|Integer|是|1|域名列表的页码。 |
|PageSize|Integer|是|20|域名列表分页的大小。 |
|SimpleTransferInStatus|String|否|INIT|转移状态。取值：

 -   **INIT**：提交转入。
-   **AUTHORIZATION**：授权转入（邮箱验证）。
-   **NAME\_VERIFICATION**：命名审核。
-   **PASSWORD\_VERIFICATION**：转移密码验证。
-   **PENDING**：转入处理中。
-   **SUCCESS**：转入成功。
-   **FAIL**：转入失败。 |
|DomainName|String|否|Aliyun.com|域名，前缀匹配（模糊查询）。 |
|SubmissionStartDate|Long|否|1514428524669|提交域名列表转入的结束时间。 |
|SubmissionEndDate|Long|否|1514428524669|提交域名列表转入的开始时间。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPageNum|Integer|1|当前域名列表的页码。 |
|Data|Array of TransferInInfo| |域名转入信息列表。 |
|TransferInInfo| | | |
|DomainName|String|test.com|域名。 |
|Email|String|test@test.com|域名转入确认邮件发送邮箱。 |
|ExpirationDate|String|2018-03-28 00:41:42|域名转入的过期时间。 |
|ExpirationDateLong|Long|1514428524669|域名转入过期的时间戳。 |
|InstanceId|String|S20181T0WLI85212|实例编号。 |
|ModificationDate|String|2018-03-28 00:41:42|域名转入信息的更新时间。 |
|ModificationDateLong|Long|1514428524669|域名转入信息更新的时间戳。 |
|NeedMailCheck|Boolean|true|是否需要邮件验证。取值：

 -   **true**：需要。
-   **false**：不需要。 |
|ProgressBarType|Integer|0|域名转移过程进度条类型。取值：

 -   **0**：同时需要邮箱验证和命名审核。
-   **1**：需要邮箱验证不需要命名审核。
-   **2**：需要命名审核不需要邮箱验证。
-   **3**：不需要邮箱验证不需要命名审核。 |
|ResultCode|String|clientCancelled|域名转移失败时的失败原因code。取值：

 -   **clientCancelled**：您取消了此次域名转入。
-   **clientRejected**：域名原注册商拒绝了本次域名转入（或您通过原注册商进行了拒绝操作）。
-   **serverCancelled**：注册局取消转入。
-   **transferProhibited**：域名为禁止转移状态。
-   **transferExpired**：您未在有效期内完成相关转入确认。
-   **nameVerificationFailed**：域名命名审核未通过。
-   **transferSubmitted**：其他用户已经提交域名转入。 |
|ResultDate|String|2018-03-28 00:41:42|域名转移成功或失败的时间。 |
|ResultDateLong|Long|1514428524669|域名转移成功或失败的时间戳。 |
|ResultMsg|String|您取消了此次域名转入|域名转移失败时的失败原因描述。 |
|SimpleTransferInStatus|String|FAIL|域名转移状态。取值：

 -   **INIT**：提交转入。
-   **AUTHORIZATION**：授权转入（邮箱验证）。
-   **NAME\_VERIFICATION**：命名审核。
-   **PASSWORD\_VERIFICATION**：转移密码验证。
-   **PENDING**：转入处理中。
-   **SUCCESS**：转入成功。
-   **FAIL**：转入失败。 |
|Status|Integer|11|详细域名转入状态。取值：

 -   **10**：初始状态。
-   **11**：已发送邮件验证token链接。
-   **19**：token连接已验证成功。
-   **20**：已提交命名审核。
-   **21**：命名审核失败。
-   **29**：命名审核成功。
-   **31**：转移密码错误。
-   **39**：转入提交成功。
-   **50**：客户取消转入。
-   **51**：转入失败。
-   **52**：转入过期。
-   **59**：转入成功。 |
|SubmissionDate|String|2018-03-28 00:41:42|域名转移请求的提交时间。 |
|SubmissionDateLong|Long|1514428524669|域名转移请求提交的时间戳。 |
|TransferAuthorizationCodeSubmissionDate|String|2018-03-28 00:41:42|域名转移密码提交成功的时间。 |
|TransferAuthorizationCodeSubmissionDateLong|Long|1514428524669|域名转移密码提交成功的时间戳。 |
|UserId|String|123456|用户编号。 |
|WhoisMailStatus|Boolean|true|是否通过whois抓取到域名持有者邮箱。当域名转入处于授权转入（邮箱验证）并且该字段为**false**时，表示未通过whois抓取到域名持有者邮箱，需要等待人工处理。 |
|NextPage|Boolean|true|是否有下一页。 |
|PageSize|Integer|20|域名列表的分页大小。 |
|PrePage|Boolean|false|是否有上一页。 |
|RequestId|String|AF7D4DCE-0776-47F2-A9B2-6FB85A87AA60|唯一请求识别码。 |
|TotalItemNum|Integer|40|总条数。 |
|TotalPageNum|Integer|2|总页数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=QueryTransferInList
&PageNum=1
&PageSize=20
&<公共请求参数>
```

正常返回示例

`XML` 格式

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
            <ResultMsg>You have canceled this domain name transfer in.</ResultMsg>
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

`JSON` 格式

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

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

