# SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID

调用SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID通过信息模板编号提交修改注册联系人信息任务。

## API描述

任务执行结果请通过[QueryTaskDetailList](~~67710~~)接口查询。修改后注册联系人信息和模板信息一致，如果域名是强制实名认证域名，修改成功后域名会变为实名认证成功状态。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID|系统规定参数。取值：**SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID**。 |
|DomainName.N|RepeatList|是|Aliyun.com|域名列表，多个域名时使用**list**方式传递。域名列表可通过[QueryDomainList](~~69362~~)接口获取。 |
|RegistrantProfileId|Long|是|1|信息模板编号。您可以通过[QueryRegistrantProfiles](~~67701~~)接口查询信息模板编号。 |
|TransferOutProhibited|Boolean|是|false|是否添加禁止转出限制，表示所有者修改后是否限制域名60天转出。取值：

 -   **false**：不添加。
-   **true**：添加。

 默认值为**false**。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|40F46D3D-F4F3-4CCB-AC30-2DD20E32E528|请求ID。 |
|TaskNo|String|3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8|任务编号。 |

## 示例

请求示例

```
http://domain.aliyuncs.com/?Action=SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID
&ContactTemplateId=1
&DomainName.1=test.com
&RegistrantProfileId=1
&AddTransferProhibitionLock=true
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SaveTaskForUpdatingRegistrantInfoByRegistrantProfileIDResponse>
      <TaskNo>3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8</TaskNo>
      <RequestId>40F46D3D-F4F3-4CCB-AC30-2DD20E32E528</RequestId>
</SaveTaskForUpdatingRegistrantInfoByRegistrantProfileIDResponse>
```

`JSON` 格式

```
{    
  "TaskNo": "3cb1adc3-20e8-44ae-9e76-e812fa6fc9d8",
  "RequestId": "40F46D3D-F4F3-4CCB-AC30-2DD20E32E528"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

