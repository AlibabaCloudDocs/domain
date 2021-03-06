# SaveSingleTaskForModifyingDSRecord

You can call this operation to submit a task for modifying the delegation signer \(DS\) record of a domain name.

You can call the [QueryTaskDetailList](~~67710~~) operation to query the execution result.

## Debugging

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=Domain&api=SaveSingleTaskForModifyingDSRecord&type=RPC&version=2018-01-29)

## Request parameters

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|SaveSingleTaskForModifyingDSRecord|The operation that you want to perform. Set the value to **SaveSingleTaskForModifyingDSRecord**. |
|Algorithm|Integer|Yes|1|The ID of the encryption algorithm in use. For more information, see [Domain Name System Security \(DNSSEC\) Algorithm Numbers](https://www.iana.org/assignments/dns-sec-alg-numbers/dns-sec-alg-numbers.xhtml). Valid values:

-   **1:** RSA/MD5
-   **2:** Diffie-Hellman
-   **3:** DSA/SHA-1
-   **5:** RSA/SHA-1
-   **6:** DSA-NSEC3-SHA1
-   **7:** RSASHA1-NSEC3-SHA1
-   **8:** RSA/SHA-256
-   **10:** RSA/SHA-512
-   **12:** GOST R 34.10-2001
-   **13:** ECDSA Curve P-256 with SHA-256
-   **14:** ECDSA Curve P-384 with SHA-384
-   **15:** Ed2551916 Ed448
-   **252:** Reserved for Indirect Keys
-   **253:** Private algorithm
-   **254:** Private algorithm OID |
|Digest|String|Yes|f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598|The value of the digest. |
|DigestType|Integer|Yes|2|The type of the digest algorithm. For more information, see [DS Resource Record \(RR\) Type Digest Algorithms](https://www.iana.org/assignments/ds-rr-types/ds-rr-types.xhtml). Valid values:

-   **1:** SHA-1
-   **2:** SHA-256
-   **3:** GOST R 34.11-94
-   **4:** SHA-384 |
|DomainName|String|Yes|test.com|The domain name for which you want to modify the DS record. |
|KeyTag|Integer|Yes|1|The key tag that is used to identify the domain name system security \(DNSSEC\) record. Valid values: 0 to 65535 |
|Lang|String|No|en|The language of the error message to return. Valid values:

-   **zh:** Chinese
-   **en:** English

Default value:**en** |
|UserClientIp|String|No|127.0.0.1|The IP address of the client used by the user to submit the task. |

## Response parameters

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|E2598CAF-DBFE-494E-95EF-B42A33C178AA|The ID of the request. |
|TaskNo|String|e893148f-6343-4ae1-9eba-6e2a4116e142|The ID of the task. |

## Examples

Sample requests

```

http(s)://[Endpoint]/? Action=SaveSingleTaskForModifyingDSRecord
&Algorithm=1
&Digest=f58fa917424383934c7b0cf1a90f61d692745680fa06f5ecdbe0924e86de9598
&DigestType=2
&DomainName=test.com
&KeyTag=1
&<Common request parameters>

```

Sample success responses

`XML` format

```
<SaveSingleTaskForModifyingDSRecordResponse>
    <TaskNo>3cbc5b9f-080d-4b5f-a04b-29f54bffdeab</TaskNo>
    <RequestId>722D0361-93BD-4289-824F-D17B218D8BF4</RequestId>
</SaveSingleTaskForModifyingDSRecordResponse>
```

`JSON` format

```
{
	"TaskNo":"e893148f-6343-4ae1-9eba-6e2a4116e142",
	"RequestId":"E2598CAF-DBFE-494E-95EF-B42A33C178AA"
}
```

## Error codes

For a list of error codes, visit the [API Error Center](https://error-center.alibabacloud.com/status/product/Domain).

