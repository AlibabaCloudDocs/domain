# CheckDomainSunriseClaim

调用CheckDomainSunriseClaim根据传入域名查询商标词key。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=CheckDomainSunriseClaim&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CheckDomainSunriseClaim|系统规定参数。取值：**CheckDomainSunriseClaim**。 |
|DomainName|String|是|example.com|要查询的域名。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|ClaimKey|String|2017092100/8/2/1/kDfu9htHGEx\_y-LJ3XSlKMZ70000020001|TMDB库提供的商标词key。 |
|RequestId|String|BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1|唯一请求识别码。 |
|Result|Integer|1|结果。取值：

 -   **0**：不是商标词或不处于claim域名生命周期。
-   **1**：sunrise域名生命周期。
-   **2**：claim域名生命周期。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CheckDomainSunriseClaim
&DomainName=abc.xin
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CheckDomainSunriseClaim>
      <RequestId>BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1</RequestId>
      <Result>1</Result>
      <ClaimKey>2017092100/8/2/1/kDfu9htHGEx_y-LJ3XSlKMZ70000020001</ClaimKey>
</CheckDomainSunriseClaim>
```

`JSON` 格式

```
{
    "RequestId": "BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1",
    "Result": 2,
    "ClaimKey": "2017092100/8/2/1/kDfu9htHGEx_y-LJ3XSlKMZ70000020001"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

