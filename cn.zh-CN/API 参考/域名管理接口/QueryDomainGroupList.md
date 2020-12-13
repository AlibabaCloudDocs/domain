# QueryDomainGroupList

调用QueryDomainGroupList查询域名分组列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryDomainGroupList&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryDomainGroupList|系统规定参数。取值：**QueryDomainGroupList**。 |
|ShowDeletingGroup|Boolean|否|false|是否展示正在删除中的域名分组，取值如下：

 -   **false**：否。
-   **true**：是。

 默认为**false**。 |
|DomainGroupName|String|否|默认分组|用户自定义的域名分组名称。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Data|Array of DomainGroup| |域名分组列表。 |
|DomainGroup| | | |
|BeingDeleted|Boolean|false|是否正在删除中。超过1000个域名的分组删除为异步过程，需要系统处理一段时间，在此期间内该字段为**true**。 |
|CreationDate|String|2018-04-02 15:59:06|域名分组创建时间。 |
|DomainGroupId|String|-1|域名分组编号。 |
|DomainGroupName|String|未分组|域名分组名称。 |
|DomainGroupStatus|String|COMPLETE|域名分组状态。取值：

 -   **PROCESSING**：处理中；
-   **COMPLETE**：已完成。

 **说明：** 通过文件设置分组、替换超过1000个域名的分组等情况下为异步过程，需要等待系统处理，此状态下该字段为**PROCESSING**。 |
|ModificationDate|String|2018-04-02 15:59:06|域名分组修改时间。 |
|TotalNumber|Integer|20|域名数量。 |
|RequestId|String|80011ABC-F573-4795-B0E8-377BFBBA3422|唯一请求标识码。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=QueryDomainGroupList
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<QueryDomainGroupListResponse>
    <Data>
        <DomainGroup>
            <DomainGroupId>-1</DomainGroupId>
            <BeingDeleted>false</BeingDeleted>
            <DomainGroupName>未分组</DomainGroupName>
            <CreationDate>2018-04-27 14:49:10</CreationDate>
            <TotalNumber>346</TotalNumber>
            <DomainGroupStatus>COMPLETE</DomainGroupStatus>
       </DomainGroup>
    </Data>
    <RequestId>AA897378-08E9-4C34-98F9-8689F4EDC98E</RequestId>
</QueryDomainGroupListResponse>
```

`JSON` 格式

```
{
    "Data":{
        "DomainGroup":[{
            "BeingDeleted":false,
            "CreationDate":"2018-04-27 14:48:02",
            "DomainGroupId":-1,
            "DomainGroupName":"未分组",
            "DomainGroupStatus":"COMPLETE",
            "TotalNumber":346
        }]
    },
    "RequestId":"49F5586F-4D94-4909-8C6F-7DD5072ED08D"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

