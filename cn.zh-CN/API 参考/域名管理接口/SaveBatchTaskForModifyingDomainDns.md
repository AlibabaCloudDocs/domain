# SaveBatchTaskForModifyingDomainDns

调用SaveBatchTaskForModifyingDomainDns提交批量修改域名DNS任务。

任务执行结果请通过[QueryTaskDetailList](~~67710~~)接口查询。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveBatchTaskForModifyingDomainDns&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveBatchTaskForModifyingDomainDns|系统规定参数。取值：**SaveBatchTaskForModifyingDomainDns**。 |
|AliyunDns|Boolean|是|false|是否修改为阿里云DNS。取值：

 -   **true**：是。
-   **false**：否。 |
|DomainName.N|RepeatList|是|test1.com|域名。 |
|DomainNameServer.N|RepeatList|否|ns1.test.com|DNS列表，**AliyunDns**值为**false**时此项必填。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|6A862A8A-E7AB-4C4E-8946-A74122D9CC4B|唯一请求识别码。 |
|TaskNo|String|35fb2fb7-d4d6-4478-9408-22cb63696b86|任务编号。 |

## 示例

请求示例

```
http://domain.aliyuncs.com/?Action=SaveBatchTaskForModifyingDomainDns
&AliyunDns=false
&DomainName.1=test1.com
&DomainName.2=test2.com
&DomainNameServer.1=ns1.test.com
&DomainNameServer.2=ns2.test.com
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SaveBatchTaskForModifyingDomainDnsResponse>
  <TaskNo>35fb2fb7-d4d6-4478-9408-22cb63696b86</TaskNo>
  <RequestId>6A862A8A-E7AB-4C4E-8946-A74122D9CC4B</RequestId></SaveBatchTaskForModifyingDomainDnsResponse>
```

`JSON` 格式

```
{
  "requestId": "689C17B3-6AE0-45FB-8E41-4491A02C9999",
  "taskNo": "fce12087-6c9f-4dcd-92df-d3829b7f19bc"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

