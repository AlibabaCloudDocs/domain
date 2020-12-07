# QueryRegistrantProfileRealNameVerificationInfo

调用QueryRegistrantProfileRealNameVerificationInfo接口查询信息模板实名认证资料。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryRegistrantProfileRealNameVerificationInfo&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryRegistrantProfileRealNameVerificationInfo|系统规定参数，取值：**QueryRegistrantProfileRealNameVerificationInfo**。 |
|RegistrantProfileId|Long|是|1234567|待查询的信息模板的编号。

 信息模板创建成功后由系统自动生成，您可以调用[QueryRegistrantProfiles](~~67701~~)接口查询信息模板编号。 |
|FetchImage|Boolean|否|false|是否获取实名认证图片信息。取值：

 -   **true**：获取。
-   **false**：不获取。

 默认值为**false**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为127.0.0.1。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RegistrantProfileId|Long|1234567|查询到的信息模板的编号。 |
|IdentityCredentialType|String|SFZ|实名认证证件类型。取值：

 -   **SFZ**：身份证。
-   **HZ**：护照。
-   **YYZZ**：营业执照。
-   **ORG**：组织机构代码证。
-   **XYDM**：统一社会信用代码证书。
-   **TXZ**：港澳居民来往内地通行证。

 **说明：** 更多证件类型的取值请参见[支持实名认证的证件类型](~~72209~~)。 |
|IdentityCredentialNo|String|4111111111111110\*\*|实名认证证件号码。 |
|IdentityCredential|String|dGVzdA==|采用Base64编码的实名认证资料图片。 |
|IdentityCredentialUrl|String|http://test.oss-cn-hangzhou.aliyuncs.com/20170522/1219541161213057\_070445190.jpg|实名认证图片下载地址。 |
|SubmissionDate|String|2017-05-22 19:04:49|实名认证资料提交时间。 |
|ModificationDate|String|2017-05-22 19:04:49|实名认证资料更新时间。 |
|RequestId|String|4D73432C-7600-4779-ACBB-C3B5CA145D32|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=QueryRegistrantProfileRealNameVerificationInfo
&RegistrantProfileId=1234567
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<QueryRegistrantProfileRealNameVerificationInfoResponse>
	  <IdentityCredentialNo>4111111111111110**</IdentityCredentialNo>
	  <IdentityCredentialType>SFZ</IdentityCredentialType>
	  <ModificationDate>2017-05-22 19:04:49</ModificationDate>
	  <RegistrantProfileId>1234567</RegistrantProfileId>
	  <RequestId>4D73432C-7600-4779-ACBB-C3B5CA145D32</RequestId>
	  <SubmissionDate>2017-05-22 19:04:49</SubmissionDate>
</QueryRegistrantProfileRealNameVerificationInfoResponse>
```

`JSON` 格式

```
{
    "IdentityCredentialNo":"4111111111111110**",
    "IdentityCredentialType":"SFZ",
    "ModificationDate":"2017-05-22 19:04:49",
    "RegistrantProfileId":1234567,
    "RequestId":"4D73432C-7600-4779-ACBB-C3B5CA145D32",
    "SubmissionDate":"2017-05-22 19:04:49"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

