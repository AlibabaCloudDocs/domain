# SaveSingleTaskForAddingDSRecord

调用SaveSingleTaskForAddingDSRecord提交创建DS记录任务。

任务执行结果请通过[QueryTaskDetailList](~~67710~~)接口查询。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForAddingDSRecord&type=RPC&version=2018-01-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|SaveSingleTaskForAddingDSRecord|系统规定参数。取值：**SaveSingleTaskForAddingDSRecord**。 |
|Algorithm|Integer|是|1|加密算法编号，详见[Domain Name System Security \(DNSSEC\) Algorithm Numbers](https://www.iana.org/assignments/dns-sec-alg-numbers/dns-sec-alg-numbers.xhtml)。取值：

 -   **1**：RSA/MD5。
-   **2**：Diffie-Hellman。
-   **3**：DSA/SHA-1。
-   **5**：RSA/SHA-1。
-   **6**：DSA-NSEC3-SHA1。
-   **7**：RSASHA1-NSEC3-SHA1。
-   **8**：RSA/SHA-256。
-   **10**：RSA/SHA-512。
-   **12**：GOST R 34.10-2001。
-   **13**：ECDSA Curve P-256 with SHA-256。
-   **14**：ECDSA Curve P-384 with SHA-384。
-   **15**：Ed2551916 Ed448。
-   **252**：Reserved for Indirect Keys。
-   **253**：private algorithm。
-   **254**：private algorithm OID。 |
|Digest|String|是|f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598|摘要。 |
|DigestType|Integer|是|2|摘要算法类型，详见[Delegation Signer \(DS\) Resource Record \(RR\) Type Digest Algorithms](https://www.iana.org/assignments/ds-rr-types/ds-rr-types.xhtml)。取值：

 -   **1**：SHA-1；
-   **2**：SHA-256；
-   **3**：GOST R 34.11-94；
-   **4**：SHA-384。 |
|DomainName|String|是|test.com|域名。 |
|KeyTag|Integer|是|1|密钥标签，用于标识DNSSEC记录，为小于65536的整数值。 |
|Lang|String|否|en|接口返回错误信息语言。取值：

 -   **zh**：中文；
-   **en**：英文。

 默认为**en**。 |
|UserClientIp|String|否|127.0.0.1|用户IP，可以设置为**127.0.0.1**。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|唯一请求识别码。 |
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|任务编号。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=SaveSingleTaskForAddingDSRecord
&Algorithm=1
&Digest=f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598
&DigestType=2
&DomainName=test.com
&KeyTag=1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<SaveSingleTaskForAddingDSRecordResponse>
    <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
    <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForAddingDSRecordResponse>
```

`JSON` 格式

```
{
    "RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA",
    "TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142"
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/Domain)查看更多错误码。

