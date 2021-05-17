# SaveSingleTaskForCreatingDnsHost

调用SaveSingleTaskForCreatingDnsHost提交单个创建dnshost任务。

## API描述

任务执行结果请通过[QueryTaskDetailList](~~67710~~)接口查询。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForCreatingDnsHost&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveSingleTaskForCreatingDnsHost|系统规定参数。取值：**SaveSingleTaskForCreatingDnsHost**。 |
|InstanceId|String|是|S1234567890|域名实例编号，可通过查询域名列表接口[QueryDomainList](~~67712~~)获得。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|DnsName|String|是|dns1|DNS名称。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|0F1B3547-BE50-4206-8F78-9540FFB85BC1|唯一请求识别码。 |
|TaskNo|String|e9b8e8b4-7334-4548-9cec-c30b6891f292|任务编号。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=SaveSingleTaskForCreatingDnsHost
&DnsName=dns1
&InstanceId=S1234567890
&Ip.1=218.xx.xx.236
&<公共请求参数>
```

正常返回示例

`XML`格式

```
HTTP/1.1 200 OK
Content-Type:application/xml

<SaveSingleTaskForCreatingDnsHostResponse>
<TaskNo>e9b8e8b4-7334-4548-9cec-c30b6891f292</TaskNo>
<RequestId>0F1B3547-BE50-4206-8F78-9540FFB85BC1</RequestId>
</SaveSingleTaskForCreatingDnsHostResponse>
```

`JSON`格式

```
HTTP/1.1 200 OK
Content-Type:application/json

{
  "requestId" : "0F1B3547-BE50-4206-8F78-9540FFB85BC1",
  "taskNo" : "e9b8e8b4-7334-4548-9cec-c30b6891f292"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

