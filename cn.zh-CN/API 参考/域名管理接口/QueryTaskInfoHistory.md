# QueryTaskInfoHistory

调用QueryTaskInfoHistory分页查询自己账户下的域名任务历史列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=QueryTaskInfoHistory&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|QueryTaskInfoHistory|系统规定参数。取值：**QueryTaskInfoHistory**。 |
|PageSize|Integer|是|2|分页大小。 |
|TaskNoCursor|String|否|aa634d3f-927e-4d17-9d2c-test|任务光标，翻页时传入对应页游标中的任务编号（技术参数）。 |
|CreateTimeCursor|Long|否|1522080000000|创建日期的游标（技术参数）。 |
|BeginCreateTime|Long|否|1522080000000|查询创建日期范围的开始时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数，目前只支持按天查询。 |
|EndCreateTime|Long|否|1522080000000|查询创建日期范围的结束时间，UTC时间1970年1月1日0点距离现在的毫秒数，目前只支持按天查询。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPageCursor|Struct| |当前页的游标。 |
|Clientip|String|127.0.0.1|提交任务时用户IP。 |
|CreateTime|String|2017-11-01 17:22:51|任务创建时间。 |
|CreateTimeLong|Long|1509528171000|任务创建时间。 |
|TaskNo|String|aa634d3f-927e-4d17-9d2c-test|任务编号。 |
|TaskNum|Integer|1|任务包含域名数量。 |
|TaskStatus|String|COMPLETE|任务状态。取值：

 -   **WAITING\_EXECUTE**；等待执行；
-   **EXECUTING**；执行中；
-   **COMPLETE**；执行完成。 |
|TaskStatusCode|Integer|3|任务状态码。取值：

 -   **1**：等待执行；
-   **2**：执行中；
-   **3**：执行完成。 |
|TaskType|String|CHG\_DNS|任务类型。取值：

 -   **CHG\_HOLDER**：修改所有者信息；
-   **CHG\_DNS**：修改DNS；
-   **SET\_WHOIS\_PROTECT**：设置隐私保护；
-   **UPDATE\_ADMIN\_CONTACT**：修改管理者信息；
-   **UPDATE\_BILLING\_CONTACT**：修改付费者信息；
-   **UPDATE\_TECH\_CONTACT**：修改技术者信息；
-   **SET\_UPDATE\_PROHIBITED**：设置域名安全锁；
-   **SET\_TRANSFER\_PROHIBITED**：设置域名转移锁；
-   **ORDER\_ACTIVATE**：创建注册订单；
-   **ORDER\_RENEW**：创建续费订单；
-   **ORDER\_REDEEM**：创建赎回订单；
-   **CREATE\_DNSHOST**：创建DNS host；
-   **UPDATE\_DNSHOST**：更新DNS host；
-   **UPDATE\_REGISTRANT\_CONTACT**：修改注册联系人；
-   **DELETE\_DOMAIN**：删除域名；
-   **SYNC\_DNSHOST**：同步DNS host。 |
|TaskTypeDescription|String|修改DNS|任务类型描述。 |
|NextPageCursor|Struct| |下一页的游标。 |
|Clientip|String|127.0.0.1|提交任务时用户IP。 |
|CreateTime|String|2017-10-27 13:07:07|任务创建时间。 |
|CreateTimeLong|Long|1509080827000|任务创建时间。 |
|TaskNo|String|8f112aa1-98be-48c3-82f8-test|任务编号。 |
|TaskNum|Integer|15|任务包含域名数量。 |
|TaskStatus|String|COMPLETE|任务状态。取值：

 -   **WAITING\_EXECUTE**；等待执行；
-   **EXECUTING**；执行中；
-   **COMPLETE**；执行完成。 |
|TaskStatusCode|Integer|3|任务状态码。取值：

 -   **1**：等待执行；
-   **2**：执行中；
-   **3**：执行完成。 |
|TaskType|String|CHG\_DNS|任务类型。取值：

 -   **CHG\_HOLDER**：修改所有者信息；
-   **CHG\_DNS**：修改DNS；
-   **SET\_WHOIS\_PROTECT**：设置隐私保护；
-   **UPDATE\_ADMIN\_CONTACT**：修改管理者信息；
-   **UPDATE\_BILLING\_CONTACT**：修改付费者信息；
-   **UPDATE\_TECH\_CONTACT**：修改技术者信息；
-   **SET\_UPDATE\_PROHIBITED**：设置域名安全锁；
-   **SET\_TRANSFER\_PROHIBITED**：设置域名转移锁；
-   **ORDER\_ACTIVATE**：创建注册订单；
-   **ORDER\_RENEW**：创建续费订单；
-   **ORDER\_REDEEM**：创建赎回订单；
-   **CREATE\_DNSHOST**：创建DNS host；
-   **UPDATE\_DNSHOST**：更新DNS host；
-   **UPDATE\_REGISTRANT\_CONTACT**：修改注册联系人；
-   **DELETE\_DOMAIN**：删除域名；
-   **SYNC\_DNSHOST**：同步DNS host。 |
|TaskTypeDescription|String|修改DNS|任务类型描述。 |
|Objects|Array of TaskInfoHistory| |任务信息。 |
|Clientip|String|127.0.0.1|提交任务时用户IP。 |
|CreateTime|String|2017-11-01 17:22:51|任务创建时间。 |
|CreateTimeLong|Long|1509528171000|任务创建时间。 |
|TaskNo|String|aa634d3f-927e-4d17-9d2c-test|任务编号。 |
|TaskNum|Integer|1|任务包含域名数量。 |
|TaskStatus|String|COMPLETE|任务状态。取值：

 -   **WAITING\_EXECUTE**；等待执行；
-   **EXECUTING**；执行中；
-   **COMPLETE**；执行完成。 |
|TaskStatusCode|Integer|3|任务状态码。取值：

 -   **1**：等待执行；
-   **2**：执行中；
-   **3**：执行完成。 |
|TaskType|String|CHG\_DNS|任务类型。取值：

 -   **CHG\_HOLDER**：修改所有者信息；
-   **CHG\_DNS**：修改DNS；
-   **SET\_WHOIS\_PROTECT**：设置隐私保护；
-   **UPDATE\_ADMIN\_CONTACT**：修改管理者信息；
-   **UPDATE\_BILLING\_CONTACT**：修改付费者信息；
-   **UPDATE\_TECH\_CONTACT**：修改技术者信息；
-   **SET\_UPDATE\_PROHIBITED**：设置域名安全锁；
-   **SET\_TRANSFER\_PROHIBITED**：设置域名转移锁；
-   **ORDER\_ACTIVATE**：创建注册订单；
-   **ORDER\_RENEW**：创建续费订单；
-   **ORDER\_REDEEM**：创建赎回订单；
-   **CREATE\_DNSHOST**：创建DNS host；
-   **UPDATE\_DNSHOST**：更新DNS host；
-   **UPDATE\_REGISTRANT\_CONTACT**：修改注册联系人；
-   **DELETE\_DOMAIN**：删除域名；
-   **SYNC\_DNSHOST**：同步DNS host。 |
|TaskTypeDescription|String|修改DNS|任务类型描述。 |
|PageSize|Integer|2|分页大小。 |
|PrePageCursor|Struct| |上一页游标。 |
|Clientip|String|127.0.0.1|提交任务时用户IP。 |
|CreateTime|String|2017-11-01 17:19:47|任务创建时间。 |
|CreateTimeLong|Long|1509527987000|任务创建时间。 |
|TaskNo|String|f9baa3d5-33b9-4c81-8847-test|任务编号。 |
|TaskNum|Integer|15|任务包含域名数量。 |
|TaskStatus|String|COMPLETE|任务状态。取值：

 -   **WAITING\_EXECUTE**；等待执行；
-   **EXECUTING**；执行中；
-   **COMPLETE**；执行完成。 |
|TaskStatusCode|Integer|3|任务状态码。取值：

 -   **1**：等待执行；
-   **2**：执行中；
-   **3**：执行完成。 |
|TaskType|String|CHG\_DNS|任务类型。取值：

 -   **CHG\_HOLDER**：修改所有者信息；
-   **CHG\_DNS**：修改DNS；
-   **SET\_WHOIS\_PROTECT**：设置隐私保护；
-   **UPDATE\_ADMIN\_CONTACT**：修改管理者信息；
-   **UPDATE\_BILLING\_CONTACT**：修改付费者信息；
-   **UPDATE\_TECH\_CONTACT**：修改技术者信息；
-   **SET\_UPDATE\_PROHIBITED**：设置域名安全锁；
-   **SET\_TRANSFER\_PROHIBITED**：设置域名转移锁；
-   **ORDER\_ACTIVATE**：创建注册订单；
-   **ORDER\_RENEW**：创建续费订单；
-   **ORDER\_REDEEM**：创建赎回订单；
-   **CREATE\_DNSHOST**：创建DNS host；
-   **UPDATE\_DNSHOST**：更新DNS host；
-   **UPDATE\_REGISTRANT\_CONTACT**：修改注册联系人；
-   **DELETE\_DOMAIN**：删除域名；
-   **SYNC\_DNSHOST**：同步DNS host。 |
|TaskTypeDescription|String|修改DNS|任务类型描述。 |
|RequestId|String|EB3FCCBA-CA1F-4D31-9F34-test|唯一请求识别码。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=QueryTaskInfoHistory
&PageSize=2
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<QueryTaskInfoHistoryResponse>
      <Objects>
            <TaskInfoHistory>
                  <Clientip>127.0.0.1</Clientip>
                  <TaskNo>aa634d3f-927e-4d17-9d2c-test</TaskNo>
                  <CreateTime>2017-11-01 17:22:51</CreateTime>
                  <TaskStatus>COMPLETE</TaskStatus>
                  <TaskNum>1</TaskNum>
                  <TaskStatusCode>3</TaskStatusCode>
                  <TaskType>CHG_DNS</TaskType>
                  <CreateTimeLong>1509528171000</CreateTimeLong>
            </TaskInfoHistory>
            <TaskInfoHistory>
                  <Clientip>127.0.0.1</Clientip>
                  <TaskNo>f9baa3d5-33b9-4c81-8847-test</TaskNo>
                  <CreateTime>2017-11-01 17:19:47</CreateTime>
                  <TaskStatus>COMPLETE</TaskStatus>
                  <TaskNum>15</TaskNum>
                  <TaskStatusCode>3</TaskStatusCode>
                  <TaskType>CHG_DNS</TaskType>
                  <CreateTimeLong>1509527987000</CreateTimeLong>
            </TaskInfoHistory>
      </Objects>
      <PageSize>2</PageSize>
      <NextPageCursor>
            <TaskNo>8f112aa1-98be-48c3-82f8-test</TaskNo>
            <CreateTime>2017-10-27 13:07:07</CreateTime>
            <CreateTimeLong>1509080827000</CreateTimeLong>
      </NextPageCursor>
      <RequestId>EB3FCCBA-CA1F-4D31-9F34-test</RequestId>
      <CurrentPageCursor>
            <Clientip>127.0.0.1</Clientip>
            <TaskNo>aa634d3f-927e-4d17-9d2c-test</TaskNo>
            <CreateTime>2017-11-01 17:22:51</CreateTime>
            <TaskStatus>COMPLETE</TaskStatus>
            <TaskNum>1</TaskNum>
            <TaskStatusCode>3</TaskStatusCode>
            <TaskType>CHG_DNS</TaskType>
            <CreateTimeLong>1509528171000</CreateTimeLong>
      </CurrentPageCursor>
</QueryTaskInfoHistoryResponse>
```

`JSON` 格式

```
{
  "currentPageCursor": {
    "clientip": "127.0.0.1",
    "createTime": "2017-11-01 17:22:51",
    "createTimeLong": 1509528171000,
    "taskNo": "aa634d3f-927e-4d17-9d2c-test",
    "taskNum": 1,
    "taskStatus": "COMPLETE",
    "taskStatusCode": 3,
    "taskType": "CHG_DNS"
  },
  "nextPageCursor": {
    "createTime": "2017-10-27 13:07:07",
    "createTimeLong": 1509080827000,
    "taskNo": "8f112aa1-98be-48c3-82f8-test"
  },
  "objects": [
    {
      "clientip": "127.0.0.1",
      "createTime": "2017-11-01 17:22:51",
      "createTimeLong": 1509528171000,
      "taskNo": "aa634d3f-927e-4d17-9d2c-test",
      "taskNum": 1,
      "taskStatus": "COMPLETE",
      "taskStatusCode": 3,
      "taskType": "CHG_DNS"
    },
    {
      "clientip": "127.0.0.1",
      "createTime": "2017-11-01 17:19:47",
      "createTimeLong": 1509527987000,
      "taskNo": "f9baa3d5-33b9-4c81-8847-test",
      "taskNum": 15,
      "taskStatus": "COMPLETE",
      "taskStatusCode": 3,
      "taskType": "CHG_DNS"
    }
  ],
  "pageSize": 2,
  "prePageCursor": {},
  "requestId": "6EB5D9B8-AD99-4423-9D02-test"
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

