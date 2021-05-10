# QueryOperationAuditInfoDetail

调用QueryOperationAuditInfoDetail查询自助业务的审核记录详情。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryOperationAuditInfoDetail&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryOperationAuditInfoDetail|系统规定参数。取值：**QueryOperationAuditInfoDetail**。 |
|AuditRecordId|Long|是|1|审核记录ID。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AuditInfo|String|\{"regType":1,"registrantName":"张三","telephone":"1390123\*\*\*\*","account":"zhangsan@alimail.com","reason":1,"remark":"账号丢失"\}|审核信息。 |
|AuditStatus|Integer|1|审核状态。取值：

 -   **0**：待完善资料。
-   **1**、**2**、**3**、**4**：审核中。
-   **5**：审核失败。
-   **6**：审核成功。
-   **7**：取消审核。 |
|AuditType|Integer|1|审核类型。取值：

 **1**：线下转移域名。 |
|BusinessName|String|xxx.com等域名线下转移|审核业务名称。 |
|CreateTime|Long|1581919010100|记录创建时间。 |
|DomainName|String|xxx.com,yyy.com|域名。 |
|Id|String|1|审核记录ID。 |
|Remark|String|审核通过|审核备注。 |
|RequestId|String|9DFCF6F8-243C-40EC-8035-4B12FEFD7D1L|请求ID。 |
|UpdateTime|Long|1581919010101|记录更新时间。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=QueryOperationAuditInfoDetail
&AuditRecordId=1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<QueryOperationAuditInfoDetailResponse>
  <AuditInfo>{"regType":1,"registrantName":"张三","telephone":"1390123****","account":"zhangsan@alimail.com","reason":1,"remark":"账号丢失"}</AuditInfo>
  <AuditStatus>1</AuditStatus>
  <RequestId>9DFCF6F8-243C-40EC-8035-4B12FEFD7D1L</RequestId>
  <BusinessName>xxx.com等域名线下转移</BusinessName>
  <DomainName>xxx.com,yyy.com</DomainName>
  <AuditType>1</AuditType>
  <CreateTime>1581919010100</CreateTime>
  <UpdateTime>1581919010101</UpdateTime>
  <Id>1</Id>
  <Remark>审核通过</Remark>
</QueryOperationAuditInfoDetailResponse>
```

`JSON` 格式

```
{
    "AuditInfo": "{\"regType\":1,\"registrantName\":\"张三\",\"telephone\":\"1390123****\",\"account\":\"zhangsan@alimail.com\",\"reason\":1,\"remark\":\"账号丢失\"}", 
    "AuditStatus": "1", 
    "RequestId": "9DFCF6F8-243C-40EC-8035-4B12FEFD7D1L", 
    "BusinessName": "xxx.com等域名线下转移", 
    "DomainName": "xxx.com,yyy.com", 
    "AuditType": "1", 
    "CreateTime": "1581919010100", 
    "UpdateTime": "1581919010101", 
    "Id": "1", 
    "Remark": "审核通过"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

