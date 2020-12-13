# FuzzyMatchDomainSensitiveWord

调用FuzzyMatchDomainSensitiveWord检查域名是否包含敏感词。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=FuzzyMatchDomainSensitiveWord&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|FuzzyMatchDomainSensitiveWord|系统规定参数。取值：**FuzzyMatchDomainSensitiveWord**。 |
|Keyword|String|是|xxx\*\*.cn|域名关键字（除域名后缀外包含的词语），多个域名关键字之间使用英文逗号（,）分隔。 |
|Lang|String|否|en|接口返回错误信息的语言。取值范围：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Exist|Boolean|true|域名是否包含敏感词。取值：

 -   **true**：含敏感词。
-   **false**：不含敏感词。 |
|Keyword|String|xxx\*\*.cn|传入的域名关键字。 |
|MatchedSentiveWords|Array of MatchedSensitiveWord| |匹配到域名中包含敏感词的结果详情。当**Exist**参数的取值为**false**时，匹配结果为空。 |
|MatchedSensitiveWord| | | |
|Word|String|xxx|匹配到域名中包含的敏感词。 |
|RequestId|String|D15F91FD-0B34-4E48-8CBF-EFA5D2A31586|请求ID。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=FuzzyMatchDomainSensitiveWord
&Keyword=xxx**.cn
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<FuzzyMatchDomainSensitiveWordResponse>
      <MatchedSentiveWords>
            <MatchedSensitiveWord>
                  <Word>xxx</Word>
            </MatchedSensitiveWord>
      </MatchedSentiveWords>
      <Keyword>xxx**.cn</Keyword>
      <RequestId>D15F91FD-0B34-4E48-8CBF-EFA5D2A31586</RequestId>
      <Exist>true</Exist>
</FuzzyMatchDomainSensitiveWordResponse>
```

`JSON` 格式

```
{
	"MatchedSentiveWords": {
		"MatchedSensitiveWord": [
			{
				"Word": "xxx"
			}
		]
	},
	"Keyword": "xxx**.cn",
	"RequestId": "D15F91FD-0B34-4E48-8CBF-EFA5D2A31586",
	"Exist": true
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

