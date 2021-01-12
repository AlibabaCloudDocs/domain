# QueryChangeLogList

调用QueryChangeLogList分页查询您当前阿里云账号下的操作日志。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryChangeLogList&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryChangeLogList|系统规定参数。取值：QueryChangeLogList。 |
|PageNum|Integer|是|1|分页页码，最小值为**1**。 |
|PageSize|Integer|是|1|分页大小，最小值为**1**，最大值为**100**。 |
|StartDate|Long|否|1522080000000|查询操作日期的开始时间，UTC时间1970年1月1日0点距离现在的毫秒数。 |
|EndDate|Long|否|1522080000000|查询操作日期的结束时间，UTC时间1970年1月1日0点距离现在的毫秒数。 |
|DomainName|String|否|example.com|待查询操作日志的域名。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPageNum|Integer|1|当前页码。 |
|Data|Array of ChangeLog| |操作日志列表。 |
|ChangeLog| | | |
|Details|String|dns1;dns2 -\> dns3;dns4|详情。 |
|DomainName|String|test1.com|域名。 |
|Operation|String|DNS modification|操作行为。 |
|OperationIPAddress|String|127.0.0.1|操作IP。 |
|Result|String|Failed|操作结果。 |
|Time|String|2017-12-26 12:00:00|操作时间，UTC时间，如2017-12-25 12:00:00，具体格式与入参Lang有关。 |
|NextPage|Boolean|true|是否有下一页。 |
|PageSize|Integer|1|分页大小。 |
|PrePage|Boolean|false|是否有上一页。 |
|RequestId|String|2DEDFF32-7827-46B1-BE90-3DB8ABD91A58|唯一请求识别码。 |
|ResultLimit|Boolean|true|当前查询除分页限制外，服务端最多处理最近1000条记录。如结果超过1000条，**ResultLimit**为**true**，请缩小时间范围重新搜索；否则**ResultLimit**为**false**。 |
|TotalItemNum|Integer|1000|记录总数。 |
|TotalPageNum|Integer|1000|总页数。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=QueryChangeLogList
&PageNum=1
&PageSize=1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<PrePage>false</PrePage>
<CurrentPageNum>1</CurrentPageNum>
<PageSize>1</PageSize>
<RequestId>2DEDFF32-7827-46B1-BE90-3DB8ABD91A58</RequestId>
<TotalPageNum>1000</TotalPageNum>
<Data>
    <ChangeLog>
        <OperationIPAddress>127.0.0.1</OperationIPAddress>
        <Details>dns1;dns2 -&amp;gt; dns3;dns4</Details>
        <DomainName>test1.com</DomainName>
        <Time>2017-12-26 12:00:00</Time>
        <Operation>DNS modification</Operation>
        <Result>Failed</Result>
    </ChangeLog>
</Data>
<ResultLimit>true</ResultLimit>
<TotalItemNum>1000</TotalItemNum>
<NextPage>true</NextPage>
```

`JSON` 格式

```
{
    "PrePage": false,
    "CurrentPageNum": 1,
    "PageSize": 1,
    "RequestId": "2DEDFF32-7827-46B1-BE90-3DB8ABD91A58",
    "TotalPageNum": 1000,
    "Data": {
        "ChangeLog": {
            "OperationIPAddress": "127.0.0.1",
            "Details": "dns1;dns2 -&gt; dns3;dns4",
            "DomainName": "test1.com",
            "Time": "2017-12-26 12:00:00",
            "Operation": "DNS modification",
            "Result": "Failed"
        }
    },
    "ResultLimit": true,
    "TotalItemNum": 1000,
    "NextPage": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

