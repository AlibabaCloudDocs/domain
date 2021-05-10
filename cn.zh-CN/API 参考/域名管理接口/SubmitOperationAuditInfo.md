# SubmitOperationAuditInfo

调用SubmitOperationAuditInfo提交自助业务审核信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SubmitOperationAuditInfo&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SubmitOperationAuditInfo|系统规定参数。取值：**SubmitOperationAuditInfo**。 |
|AuditType|Integer|是|1|业务类型。取值：

 **1**：线下转移域名，即将域名从当前的阿里云账号转移至另一个阿里云账号。 |
|DomainName|String|是|xxxx.com,yyyy.cn|域名。支持一个或多个域名，多个域名之间用英文逗号（,）分隔。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|AuditInfo|String|否|个人 \{"regType":1,"registrantName":"张三","registrantNo":"2201919190\*\*","telephone":"1390123\*\*\*\*","account":"zhangsan@alimail.com","reason":1,"remark":"账号丢失"\} 企业 \{"regType":2,"registrantName":"华大信通","operatorName":"王武","operatorNo":"2201811987101901\*\*", "operatorPhone":"1390123\*\*\*\*","account":"wangwu@alimail.com","companyNo":"91361100MA35N6\*\*\*\*","reason":2,"remark":"账号丢失"\}|待审核信息，不同的业务类型显示的信息不同。 |
|Id|Long|否|1|审核ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Id|Long|1|系统生成的记录ID。 |
|RequestId|String|9DKCF6F8-243C-40EC-8035-4B12FEFD7C22|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=SubmitOperationAuditInfo
&AuditType=1
&DomainName=xxxx.com,yyyy.cn
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SubmitOperationAuditInfoResponse>
  <RequestId>9DKCF6F8-243C-40EC-8035-4B12FEFD7C22</RequestId>
  <Id>1</Id>
</SubmitOperationAuditInfoResponse>
```

`JSON` 格式

```
{"RequestId":"9DKCF6F8-243C-40EC-8035-4B12FEFD7C22","Id":"1"}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

