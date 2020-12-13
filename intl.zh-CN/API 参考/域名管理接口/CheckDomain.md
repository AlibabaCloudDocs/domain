# CheckDomain

调用CheckDomain检查域名是否可以注册。

## API描述

有关域名的合法性要求，请参见[域名合法性](~~67788~~)。

**说明：** 调用CheckDomain接口时有频率限制，单用户限制为10QPS，接口总量限制为100QPS。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=CheckDomain&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CheckDomain|系统规定参数。取值：**CheckDomain**。 |
|DomainName|String|是|test\*\*.xin|域名名称。 |
|FeeCommand|String|否|create|操作命令。取值：

 -   **create**：新购。
-   **renew**：续费。
-   **transfer**：转入。
-   **restore**：赎回。 |
|FeeCurrency|String|否|USD|货币类型。取值：

 -   **CNY**：人民币。
-   **USD**：美元。 |
|FeePeriod|Integer|否|1|购买周期年限，单位为**年**。范围为**1**~**10**年。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Avail|String|1|域名是否可以注册。取值：

 -   **1**：可注册。
-   **3**：预登记。
-   **4**：可删除预订。
-   **0**：不可注册。
-   **-1**：异常。
-   **-2**：暂停注册。
-   **-3**：黑名单。 |
|DomainName|String|test\*\*.xin|查询的域名名称。 |
|DynamicCheck|Boolean|true|是否动态询价。取值：

 -   **true**：是。
-   **false**：否。 |
|Premium|String|true|是否是溢价词。取值：

 -   **true**：是。
-   **false**：否。 |
|Price|Long|1286|溢价词注册价格。 |
|Reason|String|In use|由注册局返回的不可注册原因。

 **说明：** 根据注册局的不同，返回的不可注册原因不一致。 |
|RequestId|String|BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1|唯一请求识别码。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=CheckDomain
&DomainName=test**.xin
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CheckDomain>
      <RequestId>BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1</RequestId>
      <DomainName>test**.xin</DomainName>
      <Avail>1</Avail>
      <Premium>false</Premium>
      <Reason></Reason>
      <Price>1286</Price>
</CheckDomain>
```

`JSON` 格式

```
{
    "RequestId": "BA7A4FD4-EB9A-4A20-BB0C-9AEB15634DC1",
    "DomainName": "test**.xin",
    "Avail": 1,
    "Premium": false,
    "Reason": "",
    "Price": 1286
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

