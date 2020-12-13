# SaveBatchDomainRemark

调用SaveBatchDomainRemark批量保存域名备注。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveBatchDomainRemark&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveBatchDomainRemark|系统规定参数。取值：**SaveBatchDomainRemark**。 |
|InstanceIds|String|否|S12344567|实例编号列表，建议**10**条一组，每组最多**50**条，以逗号（，）隔开。 |
|Remark|String|否|MyRemarkInfo|备注信息。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**，此参数为必填项。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|4189E320-961E-4786-8E15-0000|唯一请求识别码。 |

## 示例

请求示例

```
http://domain.aliyuncs.com/?Action=SaveBatchDomainRemark
&InstanceId.1=S20182000000000
&InstanceId.2=S20182000000001
&Remark=MyRemarkInfo
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SaveBatchDomainRemarkResponse>
      <RequestId>4189E320-961E-4786-8E15-0000</RequestId>
</SaveBatchDomainRemarkResponse>
```

`JSON` 格式

```
{
  "requestId": "F7C66E24-0134-4E53-9A31-0000"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

