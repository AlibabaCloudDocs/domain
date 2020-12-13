# QueryDomainList

调用QueryDomainList分页查询自己账户下的域名列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryDomainList&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryDomainList|系统规定参数。取值：**QueryDomainList**。 |
|PageNum|Integer|是|1|域名列表的分页页码。 |
|PageSize|Integer|是|10|域名列表的分页大小。 |
|StartExpirationDate|Long|否|1522080000000|查询域名到期日期的开始时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数，目前仅支持按天查询。 |
|EndExpirationDate|Long|否|1522080000000|查询域名到期日期的结束时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数，目前仅支持按天查询。 |
|StartRegistrationDate|Long|否|1522080000000|查询域名注册日期的开始时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数，目前仅支持按天查询。 |
|EndRegistrationDate|Long|否|1522080000000|查询域名注册日期的结束时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数，目前仅支持按天查询。 |
|QueryType|String|否|1|列表查询类型。取值：

 -   **1**：急需续费列表。
-   **2**：急需赎回列表。 |
|ProductDomainType|String|否|New gTLD|域名类型。取值：

 -   **New gTLD**：新顶级域。
-   **gTLD**：通用顶级域。
-   **ccTLD**：国别域。 |
|OrderByType|String|否|ASC|业务内容（如注册时间、过期时间）的排序顺序。取值：

 -   **ASC**：升序。
-   **DESC**：倒序。

**说明：** 不传此参数默认为**DESC**。 |
|DomainName|String|否|test.com|域名搜索，可在域名列表中搜索该域名。 |
|DomainGroupId|String|否|123456|域名分组ID，可使用查询域名分组的[QueryDomainGroupList](~~69362~~)接口获取。 |
|OrderKeyType|String|否|RegistrationDate|排序字段。取值：

 -   **RegistrationDate**：根据注册时间排序。
-   **ExpirationDate**：根据到期时间排序。

 **说明：** 不传此参数时，默认以入库时间排序。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认值为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPageNum|Integer|0|当前域名列表的分页页码。 |
|Data|Array of Domain| |域名列表。 |
|Domain| | | |
|DomainAuditStatus|String|FAILED|域名实名认证状态。取值：

 -   **FAILED**：实名认证失败。
-   **SUCCEED**：实名认证成功。
-   **NONAUDIT**：未实名认证。
-   **AUDITING**：审核中。 |
|DomainGroupId|String|123456|域名分组编号。 |
|DomainGroupName|String|测试分组|域名分组名称 |
|DomainName|String|test.com|域名。 |
|DomainStatus|String|3|域名状态。取值：

 -   **1**：急需续费。
-   **2**：急需赎回。
-   **3**：正常。 |
|DomainType|String|gTLD|域名类型。取值：

 -   **New gTLD**。
-   **gTLD**。
-   **ccTLD**。 |
|ExpirationCurrDateDiff|Integer|-30|域名到期日和当前的时间的天数差值。 |
|ExpirationDate|String|Nov 02,2019 04:00:45|域名到期日期。 |
|ExpirationDateLong|Long|1522080000000|域名到期时长，UTC时间1970年1月1日0点距离域名到期日的毫秒数。 |
|ExpirationDateStatus|String|1|域名过期状态。取值：

 -   **1**：域名未过期。
-   **2**：域名已过期。 |
|InstanceId|String|ST20151102120031118|实例编号。 |
|Premium|Boolean|true|是否是溢价域名。 |
|ProductId|String|2a|产品ID。 |
|RegistrantType|String|1|域名注册类型。取值：

 -   **1**：个人。
-   **2**：企业。 |
|RegistrationDate|String|Nov 02,2017 04:00:45|注册时间。 |
|RegistrationDateLong|Long|1522080000000|注册时长，UTC时间1970年1月1日0点距离注册时间的毫秒数。 |
|Remark|String|测试备注|域名备注。 |
|NextPage|Boolean|false|是否有下一页。 |
|PageSize|Integer|5|域名分页列表的大小。 |
|PrePage|Boolean|false|是否有上一页。 |
|RequestId|String|B7AB5469-5E38-4AA9-A920-C65B7A9C8E6E|唯一请求识别码。 |
|TotalItemNum|Integer|1|域名总数。 |
|TotalPageNum|Integer|1|域名列表的总页数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=QueryDomainList
&PageNum=1
&PageSize=10
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<?xml version='1.0' encoding='UTF-8'?>
<QueryDomainListResponse>
    <Data>
        <Domain>
            <ExpirationDate>Nov 02,2019 04:00:45</expirationDate>
            <InstanceId>ST20151102120031118</SaleId>
            <RegistrationDate>Nov 02,2017 04:00:45</registrationDate>
            <DomainName>test.com</DomainName>
            <DomainType>gTLD</domainType>
        </Domain>
    </Data>
    <TotalItemNum>1</TotalItemNum>
    <PageSize>5</PageSize>
    <CurrentPageNum>0</CurrentPageNum>
    <RequestId>B7AB5469-5E38-4AA9-A920-C65B7A9C8E6E</RequestId>
    <PrePage>false</PrePage>
    <TotalPageNum>1</TotalPageNum>
    <NextPage>false</NextPage>
</QueryDomainListResponse>
```

`JSON` 格式

```
{
  "Data": {
    "Domain": [
      {
        "ExpirationDate": "Nov 02,2019 04:00:45",
        "InstanceId": "ST2015110212003800001928",
        "RegistrationDate": "Nov 02,2017 04:00:45",
        "DomainName": "fds234sdf.net",
        "DomainType": "gTLD"
      }
    ]
  },
  "TotalItemNum": 1,
  "PageSize": 5,
  "CurrentPageNum": 0,
  "RequestId": "77F90DA6-89AB-4074-80F3-E595CB57DF98",
  "PrePage": false,
  "TotalPageNum": 1,
  "NextPage": false
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

