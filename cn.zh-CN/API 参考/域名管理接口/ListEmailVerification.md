# ListEmailVerification

调用ListEmailVerification接口查询邮箱验证列表。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=ListEmailVerification&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListEmailVerification|系统规定参数。取值：ListEmailVerification。 |
|Email|String|否|82106\*\*\*\*@qq.com|待查询的邮箱地址，每次仅可上传一个邮箱。 |
|VerificationStatus|Integer|否|1|邮箱验证状态。取值：

 -   **0**：等待验证。
-   **1**：验证成功。 |
|BeginCreateTime|Long|否|1522080000000|查询创建邮箱验证的开始时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数。 |
|EndCreateTime|Long|否|1522080000000|查询创建邮箱验证的结束时间，计算方式为UTC时间1970年1月1日0点距离现在的毫秒数。 |
|PageSize|Integer|否|500|域名列表分页的大小，默认值为**0**，最大值为**5000**，可根据自身需求设置。 |
|PageNum|Integer|否|1|域名列表分页的页码，默认值为**0**，可根据自身需求进行设置。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文。
-   **en**：英文。

 默认值为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|CurrentPageNum|Integer|1|当前页码。 |
|Data|Array of EmailVerification| |邮箱验证列表。 |
|ConfirmIp|String|127.0.0.1|完成邮箱验证的电脑IP地址。 |
|Email|String|test1@aliyun.com|进行验证的邮箱地址。 |
|EmailVerificationNo|String|00000a21fd374da99d9c95b48500000|邮箱验证编号（默认为系统自动生成的流水号）。 |
|GmtCreate|String|Dec 25,2017 03:38:46|数据库记录的创建时间。 |
|GmtModified|String|Dec 25,2017 03:41:11|数据库记录的更新时间。 |
|SendIp|String|127.0.0.1|用户发起邮件验证的IP地址。 |
|TokenSendTime|String|Dec 25,2017 03:38:46|邮箱验证Token的发送时间。 |
|UserId|String|0000|用户ID。 |
|VerificationStatus|Integer|1|邮箱验证状态，取值：

 -   **0**：等待验证。
-   **1**：验证成功。 |
|VerificationTime|String|Dec 25,2017 03:41:11|完成邮箱验证的具体时间。 |
|NextPage|Boolean|false|是否有下一页。 |
|PageSize|Integer|500|分页的大小。 |
|PrePage|Boolean|false|是否有上一页。 |
|TotalPageNum|Integer|1|总页数。 |
|TotalItemNum|Integer|2|域名总记录数。 |
|RequestId|String|78C60CC3-FF0A-44E2-989A-DDE0597791C3|唯一请求识别码。 |

## 示例

请求示例

```
http(s)://domain.aliyuncs.com/?Action=ListEmailVerification
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<ListEmailVerificationResponse>
      <Data>
            <EmailVerification>
                  <ConfirmIp>127.0.0.1</ConfirmIp>
                  <TokenSendTime>Dec 25,2017 03:38:46</TokenSendTime>
                  <Email>test1@aliyun.com</Email>
                  <VerificationStatus>1</VerificationStatus>
                  <SendIp>127.0.0.1</SendIp>
                  <VerificationTime>Dec 25,2017 03:41:11</VerificationTime>
                  <EmailVerificationNo>00000a21fd374da99d9c95b48500000</EmailVerificationNo>
                  <UserId>0000</UserId>
                  <GmtCreate>Dec 25,2017 03:38:46</GmtCreate>
                  <GmtModified>Dec 25,2017 03:41:11</GmtModified>
            </EmailVerification>
            <EmailVerification>
                  <ConfirmIp>127.0.0.1</ConfirmIp>
                  <TokenSendTime>Dec 25,2017 03:35:22</TokenSendTime>
                  <Email>test2@aliyun.com</Email>
                  <VerificationStatus>1</VerificationStatus>
                  <SendIp>127.0.0.1</SendIp>
                  <VerificationTime>Dec 25,2017 03:36:57</VerificationTime>
                  <EmailVerificationNo>0000021fd374da99d9c95b48500000</EmailVerificationNo>
                  <UserId>0000</UserId>
                  <GmtCreate>Dec 25,2017 03:32:40</GmtCreate>
                  <GmtModified>Dec 25,2017 03:36:57</GmtModified>
            </EmailVerification>
      </Data>
      <TotalItemNum>2</TotalItemNum>
      <PageSize>500</PageSize>
      <CurrentPageNum>1</CurrentPageNum>
      <RequestId>4BF41EC0-C147-4F88-8B3D-D569AF5C3E8B</RequestId>
      <PrePage>false</PrePage>
      <TotalPageNum>1</TotalPageNum>
      <NextPage>false</NextPage>
</ListEmailVerificationResponse>
```

`JSON` 格式

```
{
	"PrePage": false,
	"CurrentPageNum": 1,
	"PageSize": 500,
	"RequestId": "78C60CC3-FF0A-44E2-989A-DDE0597791C3",
	"TotalPageNum": 1,
	"Data": [
		{
			"VerificationStatus": 0,
			"GmtCreate": "2020-08-07 15:34:18",
			"Email": "821067279@qq.com",
			"EmailVerificationNo": "c8b3ede2e65742478eb8216ebf94b62a",
			"UserId": "1406926474064770",
			"GmtModified": "2020-08-07 15:54:09",
			"SendIp": "127.0.0.1",
			"TokenSendTime": "2020-08-07 15:54:09"
		}
	],
	"TotalItemNum": 1,
	"NextPage": false
}
```

## 错误码

访问[错误中心](https://error-center.aliyun.com/status/product/Domain)查看更多错误码。

