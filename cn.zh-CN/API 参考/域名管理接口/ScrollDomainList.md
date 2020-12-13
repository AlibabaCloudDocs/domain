# ScrollDomainList

调用ScrollDomainList翻页遍历域名列表。

## API描述

针对域名持有数量较大的用户，查询域名列表接口响应可能存在缓慢的情况，阿里云提供了翻页遍历域名列表的功能。该接口在第一次调用时，需要传入查询条件，但不要传入scrollId，此时接口会返回scrollId，并不返回数据。第二次查询开始，需要传入上一次请求获取的scrollId，并且后续查询中传入的查询条件将不会生效，需以第一次请求时的查询条件为准。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=ScrollDomainList&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ScrollDomainList|系统规定参数。取值：**ScrollDomainList**。 |
|PageSize|Integer|是|50|域名列表的分页大小。 |
|StartRegistrationDate|Long|否|1541520000000|查询域名注册日期范围的开始时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数。 |
|EndRegistrationDate|Long|否|1541520000000|查询域名注册日期范围的结束时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数。 |
|StartExpirationDate|Long|否|1541520000000|查询域名到期日期范围的开始时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数。 |
|EndExpirationDate|Long|否|1541520000000|查询域名到期日期范围的结束时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数。 |
|DomainStatus|Integer|否|0|域名状态。取值：

 -   **0**：全部。
-   **1**：急需续费。
-   **2**：急需赎回。
-   **3**：正常。
-   **4**：正在转出万网。
-   **5**：域名持有者信息修改中。
-   **6**：未实名认证。
-   **7**：审核失败，重新实名认证。
-   **8**：审核中。 |
|ProductDomainType|String|否|gTLD|域名类型。取值：

 -   **New gTLD**。
-   **gTLD**。
-   **ccTLD**。
-   **other**。 |
|DomainGroupId|Long|否|123456|域名分组ID，可通过[QueryDomainGroupList](~~69362~~)接口获取。 |
|StartLength|Integer|否|0|查询域名长度范围的开始长度。 |
|EndLength|Integer|否|3|查询域名长度范围的结束长度。 |
|KeyWordPrefix|Boolean|否|true|开头关键字。 |
|KeyWordSuffix|Boolean|否|false|结束关键字。 |
|ExcludedPrefix|Boolean|否|false|开头排除关键字。 |
|ExcludedSuffix|Boolean|否|true|结束排除关键字。 |
|Excluded|String|否|test|排除关键字。 |
|KeyWord|String|否|test|关键字。 |
|Form|Integer|否|1|域名组成信息。 |
|ScrollId|String|否|test|翻页遍历ID（技术参数）。 |
|TradeType|Integer|否|-1|发布状态。取值：

 -   **2**：已发布一口价。
-   **3**：已发布线上议价。
-   **4**：已发布竞价。
-   **6**：已发布带价push。
-   **-1**：未发布域名交易。 |
|Suffixs|String|否|com|查询后缀列表，以逗号（，）隔开。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Data|Array of Domain| |域名列表。 |
|Domain| | | |
|DnsList|List|\["dns15.hichina.com", "dns16.hichina.com"\]|DNS列表。 |
|DomainAuditStatus|String|NONAUDIT|域名实名认证状态。取值：

 -   **FAILED**：实名认证失败。
-   **SUCCEED**：实名认证成功。
-   **NONAUDIT**：未实名认证。
-   **AUDITING**：审核中。 |
|DomainGroupId|String|1234|域名分组编号。 |
|DomainGroupName|String|测试分组|域名分组名称。 |
|DomainName|String|test.com|域名。 |
|DomainStatus|String|3|域名状态。取值：

 -   **1**：急需续费。
-   **2**：急需赎回。
-   **3**：正常。
-   **4**：转出中。
-   **5**：域名持有者信息修改中。
-   **6**：未实名认证。
-   **7**：实名认证失败。
-   **8**：实名认证审核中。 |
|DomainType|String|gTLD|域名类型。取值：

 -   **New gTLD**。
-   **gTLD**。
-   **ccTLD**。 |
|Email|String|a@test.com|邮箱。 |
|ExpirationCurrDateDiff|Integer|10|到期日和当前日期差。 |
|ExpirationDate|String|2019-02-15 17:30:35|域名到期日。 |
|ExpirationDateLong|Long|1550223035000|域名到期日，UTC时间1970年1月1日0点距离域名到期日的毫秒数。 |
|ExpirationDateStatus|String|1|域名过期状态。取值：

 -   **1**：域名未过期。
-   **2**：域名已过期。 |
|InstanceId|String|S1234|域名实例编号。 |
|Premium|Boolean|false|是否是溢价词。 |
|ProductId|String|2a|产品ID。 |
|RegistrantOrganization|String|alibaba cloud|域名持有者。 |
|RegistrantType|String|1|域名注册类型。取值：

 -   **1**：个人。
-   **2**：企业。 |
|RegistrationDate|String|2017-02-15 00:00:00|注册时间。 |
|RegistrationDateLong|Long|1487088000000|域名注册时间，计算方式为UTC时间1970年1月1日0点距离注册时间的毫秒数。 |
|Remark|String|测试域名|域名备注。 |
|ZhRegistrantOrganization|String|阿里云|中文域名持有者。 |
|PageSize|Integer|50|分页大小。 |
|RequestId|String|722AB7F5-61F0-408C-A012-4784AFD34083|唯一请求识别码。 |
|ScrollId|String|test|翻页遍历ID。 |
|TotalItemNum|Integer|200|剩余总数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ScrollDomainList
&PageSize=50
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<ScrollDomainListResponse>
  <Data>
        <Domain>
              <DnsList>
                    <Dns>dns15.hichina.com</Dns>
                    <Dns>dns16.hichina.com</Dns>
              </DnsList>
              <DomainAuditStatus>FAILED</DomainAuditStatus>
              <DomainGroupId>-1</DomainGroupId>
              <DomainGroupName>未分组</DomainGroupName>
              <DomainName>test.com</DomainName>
              <DomainStatus>7</DomainStatus>
              <DomainType>gTLD</DomainType>
              <Email>test@a.com</Email>
              <ExpirationCurrDateDiff>85</ExpirationCurrDateDiff>
              <ExpirationDate>2019-02-15 17:30:35</ExpirationDate>
              <ExpirationDateLong>1550223035000</ExpirationDateLong>
              <ExpirationDateStatus>1</ExpirationDateStatus>
              <InstanceId>S2017000000</InstanceId>
              <Premium>false</Premium>
              <ProductId>2a</ProductId>
              <RegistrantOrganization>Test</RegistrantOrganization>
              <RegistrantType>1</RegistrantType>
              <RegistrationDate>2017-02-15 00:00:00</RegistrationDate>
              <RegistrationDateLong>1487088000000</RegistrationDateLong>
              <Remark>备注</Remark>
              <ZhRegistrantOrganization>测试</ZhRegistrantOrganization>
        </Domain>
        <Domain>
              <DnsList>
                    <Dns>dns11.hichina.com</Dns>
                    <Dns>dns12.hichina.com</Dns>
              </DnsList>
              <DomainAuditStatus>SUCCEED</DomainAuditStatus>
              <DomainGroupId>-1</DomainGroupId>
              <DomainGroupName>未分组</DomainGroupName>
              <DomainName>test1.com</DomainName>
              <DomainStatus>3</DomainStatus>
              <DomainType>gTLD</DomainType>
              <Email>test@a.com</Email>
              <ExpirationCurrDateDiff>181</ExpirationCurrDateDiff>
              <ExpirationDate>2019-05-22 16:23:19</ExpirationDate>
              <ExpirationDateLong>1558513399000</ExpirationDateLong>
              <ExpirationDateStatus>1</ExpirationDateStatus>
              <InstanceId>S2000000000000</InstanceId>
              <Premium>false</Premium>
              <ProductId>2a</ProductId>
              <RegistrantOrganization>test</RegistrantOrganization>
              <RegistrantType>1</RegistrantType>
              <RegistrationDate>2018-05-22 16:23:19</RegistrationDate>
              <RegistrationDateLong>1526977399000</RegistrationDateLong>
              <Remark>备注</Remark>
              <ZhRegistrantOrganization>测试</ZhRegistrantOrganization>
        </Domain>
  </Data>
  <PageSize>2</PageSize>
  <RequestId>9012EED7-4B99-4BC3-B04F-4BA637A90DC7</RequestId>
  <ScrollId>eJxlUk2P2yAQ</ScrollId>
  <TotalItemNum>539</TotalItemNum>
</ScrollDomainListResponse>
```

`JSON` 格式

```
{
    "Data":{
        "Domain":[
            {
                "DnsList":{
                    "Dns":[
                        "dns15.hichina.com",
                        "dns16.hichina.com"
                    ]
                },
                "DomainAuditStatus":"FAILED",
                "DomainGroupId":"-1",
                "DomainGroupName":"未分组",
                "DomainName":"test.com",
                "DomainStatus":"7",
                "DomainType":"gTLD",
                "Email":"test@a.com",
                "ExpirationCurrDateDiff":85,
                "ExpirationDate":"2019-02-15 17:30:35",
                "ExpirationDateLong":1550223035000,
                "ExpirationDateStatus":"1",
                "InstanceId":"S2017000000",
                "Premium":false,
                "ProductId":"2a",
                "RegistrantOrganization":"Test",
                "RegistrantType":"1",
                "RegistrationDate":"2017-02-15 00:00:00",
                "RegistrationDateLong":1487088000000,
                "Remark":"备注",
                "ZhRegistrantOrganization":"测试"
            },
            {
                "DnsList":{
                    "Dns":[
                        "dns11.hichina.com",
                        "dns12.hichina.com"
                    ]
                },
                "DomainAuditStatus":"SUCCEED",
                "DomainGroupId":"-1",
                "DomainGroupName":"未分组",
                "DomainName":"test1.com",
                "DomainStatus":"3",
                "DomainType":"gTLD",
                "Email":"test@a.com",
                "ExpirationCurrDateDiff":181,
                "ExpirationDate":"2019-05-22 16:23:19",
                "ExpirationDateLong":1558513399000,
                "ExpirationDateStatus":"1",
                "InstanceId":"S2000000000000",
                "Premium":false,
                "ProductId":"2a",
                "RegistrantOrganization":"test",
                "RegistrantType":"1",
                "RegistrationDate":"2018-05-22 16:23:19",
                "RegistrationDateLong":1526977399000,
                "Remark":"备注",
                "ZhRegistrantOrganization":"测试"
            }
        ]
    },
    "PageSize":2,
    "RequestId":"9012EED7-4B99-4BC3-B04F-4BA637A90DC7",
    "ScrollId":"eJxlUk2P2yAQ",
    "TotalItemNum":539
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

