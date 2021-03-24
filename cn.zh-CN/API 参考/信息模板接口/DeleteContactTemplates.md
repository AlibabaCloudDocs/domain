# DeleteContactTemplates

调用DeleteContactTemplates接口批量删除域名联系人模板。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=DeleteContactTemplates&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteContactTemplates|系统规定参数。取值：DeleteContactTemplates。 |
|RegistrantProfileIds|String|是|1234567|待删除的信息模板的编号。

 信息模板创建成功后由系统自动生成，您可以调用[QueryRegistrantProfiles](~~67701~~)接口查询信息模板编号。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|4D73432C-7600-4779-ACBB-C3B5CA145D32|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=DeleteContactTemplates
&RegistrantProfileIds=1234567
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<DeleteContactTemplatesResponse>
  <RequestId>4D73432C-7600-4779-ACBB-C3B5CA145D32</RequestId>
</DeleteContactTemplatesResponse>
```

`JSON`格式

```
{
    "RequestId": "4D73432C-7600-4779-ACBB-C3B5CA145D32"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

