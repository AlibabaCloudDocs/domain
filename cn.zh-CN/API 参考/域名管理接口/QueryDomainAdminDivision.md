# QueryDomainAdminDivision

调用QueryDomainAdminDivision查询中国行政区划。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryDomainAdminDivision&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryDomainAdminDivision|系统规定参数。取值：**QueryDomainAdminDivision**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|AdminDivisions|Array of AdminDivision| |一级行政区划。 |
|AdminDivision| | | |
|Children|Array of Children| |下级行政区划。 |
|Children| | | |
|ChildDivisionName|String|石家庄|下级行政区划名称。 |
|DivisionName|String|河北|行政区划名称。 |
|RequestId|String|4EA05A10-D4BC-47EA-AD9E-370A46BB4FB9|唯一请求识别码。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=QueryDomainAdminDivision
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<QueryDomainAdminDivisionResponse>
    <RequestId>CD1D8BF9-6FA1-4840-A9F0-29B7E963152F</RequestId>
    <AdminDivisions>
        <AdminDivision>
            <DivisionName>北京</DivisionName>
            <Children>
                <Children>
                    <ChildDivisionName>市辖区</ChildDivisionName>
                </Children>
            </Children>
        </AdminDivision>
        <AdminDivision>
            <DivisionName>天津</DivisionName>
            <Children>
                <Children>
                    <ChildDivisionName>市辖区</ChildDivisionName>
                </Children>
            </Children>
        </AdminDivision>
        <AdminDivision>
            <DivisionName>河北</DivisionName>
            <Children>
                <Children>
                    <ChildDivisionName>石家庄市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>唐山市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>秦皇岛市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>邯郸市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>邢台市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>保定市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>张家口市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>承德市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>沧州市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>廊坊市</ChildDivisionName>
                </Children>
                <Children>
                    <ChildDivisionName>衡水市</ChildDivisionName>
                </Children>
            </Children>
        </AdminDivision>
    </AdminDivisions>
</QueryDomainAdminDivisionResponse>
```

`JSON` 格式

```
{
	"AdminDivisions":{
		"AdminDivision":[
			{
				"Children":{
					"Children":[{
						"ChildDivisionName":"市辖区"
					}]
				},
				"DivisionName":"北京"
			},
			{
				"Children":{
					"Children":[{
						"ChildDivisionName":"市辖区"
					}]
				},
				"DivisionName":"天津"
			},
			{
				"Children":{
					"Children":[
						{
							"ChildDivisionName":"石家庄市"
						},
						{
							"ChildDivisionName":"唐山市"
						},
						{
							"ChildDivisionName":"秦皇岛市"
						},
						{
							"ChildDivisionName":"邯郸市"
						},
						{
							"ChildDivisionName":"邢台市"
						},
						{
							"ChildDivisionName":"保定市"
						},
						{
							"ChildDivisionName":"张家口市"
						},
						{
							"ChildDivisionName":"承德市"
						},
						{
							"ChildDivisionName":"沧州市"
						},
						{
							"ChildDivisionName":"廊坊市"
						},
						{
							"ChildDivisionName":"衡水市"
						}
					]
				},
				"DivisionName":"河北"
			}
		]
	},
	"RequestId":"3BFCCC38-6E6E-4E78-837D-1C65B586397C"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

