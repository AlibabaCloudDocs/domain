# UpdateDomainToDomainGroup

调用UpdateDomainToDomainGroup向分组中设置域名。如果您使用文件上传的方式，替换拥有超过1000个域名的分组，则该操作属于异步操作，您需要等待系统处理后，才能看到结果。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=UpdateDomainToDomainGroup&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|UpdateDomainToDomainGroup|系统规定参数。取值：**UpdateDomainToDomainGroup**。 |
|DataSource|Integer|是|1|域名数据来源。取值：

 -   **1**：自定义输入域名；
-   **2**：文件上传。 |
|DomainGroupId|Long|是|1234|分组编号，可通过[QueryDomainGroupList](~~69362~~) 接口查询。 |
|Replace|Boolean|是|false|是否替换当前分组中域名。取值：

 -   **false**：向分组中新增域名；
-   **true**：替换分组中原有域名。 |
|DomainName.N|RepeatList|否|test.com|自定义输入的域名，域名来源为自定义输入时，该字段为必须。 |
|FileToUpload|String|否|dGVzdA==|base64编码的**xls**、**xlsx**文件，域名来源为文件时该字段为必须。文件中每行一个域名，单次上传最大支持文件大小为**2M**。 |
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
http(s)://[Endpoint]/?Action=UpdateDomainToDomainGroup
&DataSource=1
&DomainGroupId=1234
&Replace=false
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<UpdateDomainToDomainGroupResponse>
    <RequestId>B00B4D8C-2AF3-4EA1-8F39-579CE195C5D6</RequestId>
</UpdateDomainToDomainGroupResponse>
```

`JSON` 格式

```
{
    "RequestId":"C7EE737A-5C01-4B82-A9BF-61DA846D57D2"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

