# DeleteDomainGroup

调用DeleteDomainGroup删除域名分组。删除超过1000个域名的分组为异步过程，需要等待系统处理。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=DeleteDomainGroup&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteDomainGroup|系统规定参数。取值：**DeleteDomainGroup**。 |
|DomainGroupId|Long|否|123456|域名分组编号，可通过[QueryDomainGroupList](~~69362~~)接口获取。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|唯一请求识别码。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=DeleteDomainGroup
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<DeleteDomainGroupResponse>
    <RequestId>E577B435-A84B-4899-91BC-F7A5E5FB6956</RequestId>
</DeleteDomainGroupResponse>
```

`JSON` 格式

```
{
    "RequestId":"6176C174-F409-4311-BB09-E46CDE55E720"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

