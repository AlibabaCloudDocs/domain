# QueryFailReasonForRegistrantProfileRealNameVerification

调用QueryFailReasonForRegistrantProfileRealNameVerification接口查询信息模板实名认证审核失败的原因。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryFailReasonForRegistrantProfileRealNameVerification&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryFailReasonForRegistrantProfileRealNameVerification|系统规定参数，取值：**QueryFailReasonForRegistrantProfileRealNameVerification**。 |
|RegistrantProfileID|Long|是|1234567|实名认证失败的信息模板编号。您可以调用[QueryRegistrantProfiles](~~67701~~)接口查询信息模板编号。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为127.0.0.1。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Data|Array| |实名认证审核失败原因列表。 |
|Date|String|2017-03-17 11:08:02|审核日期。 |
|FailReason|String|证件电子信息核验不合格|实名认证审核失败的原因。

 实名认证审核失败后的处理方法，请参见[实名认证失败原因及解决方案](~~35885~~)。 |
|RequestId|String|548C407F-AEA2-4B5D-90DF-EC11EBB1D76F|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=QueryFailReasonForRegistrantProfileRealNameVerification
&RegistrantProfileID=1234567
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<QueryFailReasonForRegistrantProfileRealNameVerificationResponse>
  <RequestId>548C407F-AEA2-4B5D-90DF-EC11EBB1D76F</RequestId>
  <Data>
        <FailReason>证件电子信息核验不合格</FailReason>
        <Date>2020-06-23 09:52:31</Date>
  </Data>
</QueryFailReasonForRegistrantProfileRealNameVerificationResponse>
```

`JSON` 格式

```
{
	"RequestId": "548C407F-AEA2-4B5D-90DF-EC11EBB1D76F",
	"Data": [
		{
			"FailReason": "证件电子信息核验不合格",
			"Date": "2020-06-23 09:52:31"
		}
	]
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

