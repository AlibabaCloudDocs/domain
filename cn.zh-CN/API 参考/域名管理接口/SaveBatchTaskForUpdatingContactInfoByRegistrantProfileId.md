# SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId

调用SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId提交批量域名信息修改任务。

## API描述

任务执行结果请通过[QueryTaskDetailList](~~67710~~)接口查询。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId|操作接口名，系统规定参数，取值：**SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId**。 |
|ContactType|String|是|registrant|需要修改的联系人类型。取值：

 -   **registrant**：域名持有者。
-   **admin**：管理者。
-   **billing**：付费者。
-   **tech**：技术者。 |
|DomainName.N|RepeatList|是|example.com|域名。如需传入多个域名，请使用**list**方式传入。 |
|RegistrantProfileId|Long|是|1|信息模板编号。

 信息模板创建成功后由系统自动生成，您可以调用[QueryRegistrantProfiles](~~67701~~)接口查询信息模板编号。 |
|TransferOutProhibited|Boolean|否|true|是否添加禁止转出限制，此参数只在**ContactType**的参数值为**registrant**的情况下有效，表示持有者修改后是否限制域名60天转出。取值：

 -   **false**：不转出。
-   **true**：转出。

 默认值为**false**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|EDC28FEC-6BE0-4583-95BC-test|唯一请求识别码。 |
|TaskNo|String|880f1579-be51-4dd3-a69d-test|任务编号。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId
&ContactType=registrant
&DomainName.1=alibabacloud.com
&RegistrantProfileId=1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SaveBatchTaskForUpdatingContactInfoByRegistrantProfileIdResponse>
      <TaskNo>880f1579-be51-4dd3-a69d-test</TaskNo>
      <RequestId>EDC28FEC-6BE0-4583-95BC-test</RequestId>
</SaveBatchTaskForUpdatingContactInfoByRegistrantProfileIdResponse>
```

`JSON` 格式

```
{
  "requestId": "EDC28FEC-6BE0-4583-95BC-test",
  "taskNo": "880f1579-be51-4dd3-a69d-test"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

