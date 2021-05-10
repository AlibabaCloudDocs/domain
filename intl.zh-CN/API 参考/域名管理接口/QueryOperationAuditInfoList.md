# QueryOperationAuditInfoList

调用QueryOperationAuditInfoList查询自助业务的审核记录列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryOperationAuditInfoList&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryOperationAuditInfoList|系统规定参数。取值：**QueryOperationAuditInfoList**。 |
|PageSize|Integer|是|20|每页记录数。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|DomainName|String|否|xxxx.com|需要查询的域名。 |
|AuditType|Integer|否|1|审核类型。取值：

 **1**：线下转移域名。 |
|AuditStatus|Integer|否|1|审核状态。取值：

 -   **0**：待完善资料。
-   **1**、**2**、**3**、**4**：审核中。
-   **5**：审核失败。
-   **6**：审核成功。
-   **7**：取消审核。 |
|PageNum|Integer|否|1|页码。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPageNum|Integer|2|当前页码。 |
|Data|Array| |审核数据。 |
|AuditInfo|String|\{"regType":1,"registrantName":"张三","telephone":"1390123\*\*\*\*","account":"zhangsan@alimail.com","reason":1,"remark":"账号丢失"\}|待审核信息。 |
|AuditStatus|Integer|1|审核状态。取值：

 -   **0**：待完善资料。
-   **1**、**2**、**3**、**4**：审核中。
-   **5**：审核失败。
-   **6**：审核成功。
-   **7**：取消审核。 |
|AuditType|Integer|1|审核类型。取值：

 **1**：线下转移域名。 |
|BusinessName|String|xxx.com等域名线下转移|审核业务的名称。 |
|CreateTime|Long|1581919010101|记录创建时间。 |
|DomainName|String|xxx.com,yyy.com|域名。 |
|Id|Long|1|审核记录ID。 |
|Remark|String|审核中|审核备注。 |
|UpdateTime|Long|1581919010101|记录更新时间。 |
|NextPage|Boolean|true|是否有下一页。 |
|PageSize|Integer|20|每页记录数。 |
|PrePage|Boolean|true|是否有上一页。 |
|RequestId|String|9DFCF6F8-243C-40EC-8035-4B12FEFD7D48|请求ID。 |
|TotalItemNum|Integer|199|总记录数。 |
|TotalPageNum|Integer|10|总页数。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=QueryOperationAuditInfoList
&PageSize=20
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<QueryOperationAuditInfoListResponse>
  <PrePage>true</PrePage>
  <CurrentPageNum>2</CurrentPageNum>
  <RequestId>9DFCF6F8-243C-40EC-8035-4B12FEFD7D48</RequestId>
  <PageSize>20</PageSize>
  <TotalPageNum>10</TotalPageNum>
  <Data>
        <AuditInfo>{"regType":1,"registrantName":"张三","telephone":"1390123****","account":"zhangsan@alimail.com","reason":1,"remark":"账号丢失"}</AuditInfo>
        <AuditStatus>1</AuditStatus>
        <BusinessName>xxx.com等域名线下转移</BusinessName>
        <DomainName>xxx.com,yyy.com</DomainName>
        <AuditType>1</AuditType>
        <CreateTime>1581919010101</CreateTime>
        <UpdateTime>1581919010101</UpdateTime>
        <Id>1</Id>
        <Remark>审核中</Remark>
  </Data>
  <TotalItemNum>199</TotalItemNum>
  <NextPage>true</NextPage>
</QueryOperationAuditInfoListResponse>
```

`JSON` 格式

```
{
    "PrePage": "true", 
    "CurrentPageNum": "2", 
    "RequestId": "9DFCF6F8-243C-40EC-8035-4B12FEFD7D48", 
    "PageSize": "20", 
    "TotalPageNum": "10", 
    "Data": [
        {
            "AuditInfo": "{\"regType\":1,\"registrantName\":\"张三\",\"telephone\":\"1390123****\",\"account\":\"zhangsan@alimail.com\",\"reason\":1,\"remark\":\"账号丢失\"}", 
            "AuditStatus": "1", 
            "BusinessName": "xxx.com等域名线下转移", 
            "DomainName": "xxx.com,yyy.com", 
            "AuditType": "1", 
            "CreateTime": "1581919010101", 
            "UpdateTime": "1581919010101", 
            "Id": "1", 
            "Remark": "审核中"
        }
    ], 
    "TotalItemNum": "199", 
    "NextPage": "true"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

