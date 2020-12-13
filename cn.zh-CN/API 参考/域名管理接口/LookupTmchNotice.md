# LookupTmchNotice

调用LookupTmchNotice根据传入商标词key查询tmch（商标词）信息。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=LookupTmchNotice&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|LookupTmchNotice|系统规定参数。取值：**LookupTmchNotice**。 |
|ClaimKey|String|是|2017092100/8/2/1/kDfu9htHGEx\_y-LJ3XSlKMZ70000020001|域名商标词key，通过[CheckDomainSunriseClaim](~~97210~~)接口获取。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Claims|Array of Claim| |商标信息列表。 |
|Claim| | | |
|ClassDescs|Array of ClassDesc| |类型描述。 |
|ClassDesc| | | |
|ClassNum|Integer|18|类型编号。 |
|Desc|String|New Zealand|描述。 |
|Contacts|Array of Contact| |商标联系人列表。 |
|Contact| | | |
|Addr|Struct| |地址。 |
|Cc|String|NZ|国家。 |
|City|String|Auckland|市。 |
|Pc|String|1010|邮编。 |
|Sp|String|Auckland|省。 |
|Street|List|Level 5 131 Queen Street|街道。 |
|Email|String|82106\*\*\*\*@qq.com|电子邮件。 |
|Fax|String|+64.44723358|传真。 |
|Name|String|AJ Park|姓名。 |
|Org|String|AJ Park|组织。 |
|Type|String|agent|类型。 |
|Voice|String|+64.44738278|电话。 |
|GoodsAndServices|String|Class 9: Calculators; bags, coverings,containers, carriers and holders for mobile phones, personal handheld computers and notebooks; headphones; speakers; blank storage media;batteries. Class 16: Paper|商标产品及服务信息。 |
|Holders|Array of Holder| |商标持有者信息。 |
|Holder| | | |
|Addr|Struct| |地址。 |
|Cc|String|NZ|国家。 |
|City|String|Wellington|市。 |
|Pc|String|6011|邮编。 |
|Sp|String|Wellington|省。 |
|Street|List|Level 5 131 Queen Street|街道。 |
|Entitlement|String|owner|持有者名称。 |
|Org|String|Whitcoulls 2011 Limited|组织。 |
|JurDesc|Struct| |法律信息。 |
|Desc|String|New Zealand|描述。 |
|JurCC|String|NZ|所在地。 |
|MarkName|String|POTED|商标名称。 |
|Id|Long|586608000000|tmch的通知ID。 |
|Label|String|noted|商标标签。 |
|NotAfter|String|2018-10-15T00:00:00.0Z|商标通知结束时间。 |
|NotBefore|String|2018-10-13T00:00:00.0Z|商标通知开始时间。 |
|RequestId|String|01C10C8E-0468-468C-BCD9-E709BDD0AE8F|唯一请求识别码。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=LookupTmchNotice
&ClaimKey=2017092100/8/2/1/kDfu9htHGEx_y-LJ3XSlKMZ70000020001
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<tmchNotice>
      <id>f58a66080000000000205821776</id>
      <notBefore>2018-10-13T00:00:00.0Z</notBefore>
      <notAfter>2018-10-15T00:00:00.0Z</notAfter>
      <label>noted</label>
      <claims>
            <claim>
                  <markName>POTED</markName>
                  <holder entitlement="owner">
                    <org>Whitcoulls 2011 Limited</org>
                    <addr>
                          <street>Level 5 131 Queen Street </street>
                          <city>Auckland</city>
                          <pc>1010</pc>
                          <cc>NZ</cc>
                    </addr>
                  </holder>
                  <contacts>
                    <contact>
                          <name>AJ Park</name>
                          <org>AJ Park </org>
                          <addr>
                                <street>Level 22, State Insurance Tower</street>
                                <street>1 Willis St</street>
                                <street>Wellington </street>
                                <city>Wellington</city>
                                <pc>6011</pc>
                                <cc>NZ</cc>
                          </addr>
                          <voice>+64.44738278</voice>
                          <fax>+64.44723358</fax>
                          <email>dns@ajpark.com</email>
                    </contact>
                  </contacts>
                  <classDesc>Leather and imitations
                of leather, and goods made of these materials and not included in
                other classes; animal skins, hides; trunks and travelling bags;
                umbrellas and parasols; walking sticks; whips, harness and saddlery.
            </classDesc>
                  <classDesc>Advertising; business
                management; business administration; office functions.
            </classDesc>
                  <goodsAndServices>Class 9: Calculators; bags, coverings,
                containers, carriers and holders for mobile phones, personal handheld
                computers and notebooks; headphones; speakers; blank storage media;
                batteries. Class 16: Paper
            </goodsAndServices>
            </claim>
      </claims>
</tmchNotice>
```

`JSON` 格式

```
{
  "tmchNotice": {
    "id": "f58a66080000000000205821776",
    "notBefore": "2018-10-13T00:00:00.0Z",
    "notAfter": "2018-10-15T00:00:00.0Z",
    "label": "noted",
    "claims": {
      "claim": {
        "markName": "POTED",
        "holder": {
          "-entitlement": "owner",
          "org": "Whitcoulls 2011 Limited",
          "addr": {
            "street": "Level 5 131 Queen Street ",
            "city": "Auckland",
            "pc": "1010",
            "cc": "NZ"
          }
        },
        "contacts": {
          "contact": {
            "name": "AJ Park",
            "org": "AJ Park ",
            "addr": {
              "street": [
                "Level 22, State Insurance Tower",
                "1 Willis St",
                "Wellington "
              ],
              "city": "Wellington",
              "pc": "6011",
              "cc": "NZ"
            },
            "voice": "+64.44738278",
            "fax": "+64.44723358",
            "email": "dns@ajpark.com"
          }
        },
        "classDesc": [
          "Leather and imitations of leather, and goods made of these materials and not included in other classes; animal skins, hides; trunks and travelling bags; umbrellas and parasols; walking sticks; whips, harness and saddlery.",
          "Advertising; business management; business administration; office functions."
        ],
        "goodsAndServices": "Class 9: Calculators; bags, coverings, containers, carriers and holders for mobile phones, personal handheld computers and notebooks; headphones; speakers; blank storage media; batteries. Class 16: Paper"
      }
    }
  }
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

