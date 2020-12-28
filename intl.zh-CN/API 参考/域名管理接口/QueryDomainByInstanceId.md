# QueryDomainByInstanceId

调用QueryDomainByInstanceId根据域名实例编号查询域名的基本信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryDomainByInstanceId&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryDomainByInstanceId|系统规定参数。取值：**QueryDomainByInstanceId**。 |
|InstanceId|String|是|S20131205001\*\*\*\*|域名实例编号。

 **说明：** 您可以通过[QueryDomainList](~~67712~~)接口查询域名实例编号。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|DnsList|List|dns1.hichina.com,dns2.hichina.com|返回域名已配置的DNS列表。 |
|DomainName|String|test.com|查询的域名。 |
|DomainNameProxyService|Boolean|false|是否已开启域名隐私保护服务。 |
|DomainNameVerificationStatus|String|NONAUDIT|域名命名审核状态。取值：

 -   **NONAUDIT**：未认证。
-   **SUCCEED**：成功。
-   **FAILED**：审核失败。
-   **AUDITING**：审核中。 |
|Email|String|test@alibaba-inc.com|域名所有者邮箱。 |
|EmailVerificationClientHold|Boolean|false|域名是否被暂停解析。取值：

 -   **false**：域名未被暂停解析。
-   **true**：域名已被暂停解析。 |
|EmailVerificationStatus|Integer|1|域名持有者邮箱是否已通过验证。取值：

 -   **0**：没有通过验证。
-   **1**：已通过验证。 |
|ExpirationDate|String|2019-12-07 17:02:13|查询的域名到期时间。 |
|ExpirationDateLong|Long|1625111915000|到期时间的时间戳。 |
|InstanceId|String|S20179H1BBI9test|域名实例编号。 |
|Premium|Boolean|false|是否是溢价词。取值：

 -   **true**：溢价词。
-   **false**：非溢价词。 |
|RealNameStatus|String|NONAUDIT|域名实名认证状态。取值：

 -   **NONAUDIT**：未实名认证。
-   **SUCCEED**：实名认证成功。
-   **FAILED**：实名认证审核失败。
-   **AUDITING**：实名认证审核中。

 **说明：** 域名实名认证状态是域名命名审核和实名审核的组合状态，只有域名命名审核和实名审核均通过才算域名实名认证成功。 |
|RegistrantName|String|Test litm|联系人名称。 |
|RegistrantOrganization|String|Test litm|域名持有者。 |
|RegistrantType|String|1|域名注册联系人类型。取值：

 -   **1**：个人。
-   **2**：企业。 |
|RegistrantUpdatingStatus|String|NORMAL|域名持有者修改状态。取值：

 -   **PENDING**：域名持有者信息修改中。
-   **NORMAL**：正常。 |
|RegistrationDate|String|2017-12-07 17:02:13|域名注册时间。 |
|RegistrationDateLong|Long|1625111915000|注册时间的时间戳。 |
|RequestId|String|23C9B3C4-9E2C-4405-A88D-BD33E459D140|请求ID。 |
|TransferOutStatus|String|NORMAL|域名转出状态。取值：

 -   **NORMAL**：正常。
-   **PENDING**：正在转出阿里云。 |
|TransferProhibitionLock|String|CLOSE|域名转移锁状态。取值：

 -   **NONE\_SETTING**：未设置。
-   **OPEN**：已开启。
-   **CLOSE**：已关闭。 |
|UpdateProhibitionLock|String|CLOSE|域名安全锁状态。取值：

 -   **NONE\_SETTING**：未设置。
-   **OPEN**：已开启。
-   **CLOSE**：已关闭。 |
|UserId|String|121000000test|阿里云用户编号（阿里云账号UID）。 |
|ZhRegistrantName|String|李四|中文联系人。

 **说明：** 该参数仅适用于中国站。 |
|ZhRegistrantOrganization|String|李四|中文域名持有者。

 **说明：** 该参数仅适用于中国站。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=QueryDomainByInstanceId
&InstanceId=S20131205001****
&<公共请求参数>
```

正常返回示例

`XML` 格式

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

`JSON` 格式

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

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

