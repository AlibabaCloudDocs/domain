# Common parameters

Common parameters include common request parameters and common response parameters.

## Common request parameters

Common request parameters must be included in all Domains API requests.

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|Format|String|No|The type of the returned value. Valid values: JSON and XML. Default value: XML.|
|Version|String|Yes|The version number of the API. The value is in the `YYYY-MM-DD` format. Set the value to `2018-01-29`.|
|AccessKeyId|String|Yes|The AccessKey ID provided by Alibaba Cloud for you to access services.|
|Signature|String|Yes|The signature string of the current request. For more information about how signatures are calculated, see [Sign signatures](/intl.en-US/API Reference (New)/Calling method/Signature method.md).|
|SignatureMethod|String|Yes|The encryption method of the signature string. Set the value to HMAC-SHA1.|
|Timestamp|String|Yes|The timestamp of the request. Specify the time in the ISO 8601 standard in the `YYYY-MM-DDThh:mm:ssZ` format. The time must be in UTC. For example, `2018-01-29T12:00:00Z` indicates January 29, 2018 00:00:00 UTC.|
|SignatureVersion|String|Yes|The version of the signature encryption algorithm. Set the value to 1.0.|
|SignatureNonce|String|Yes|A unique, random number used to prevent replay attacks. You must use different numbers for different requests.|

**Examples**

```
https://domain-intl.aliyuncs.com /
? Format=xml
&Version=2017-12-18    
&Signature=Pc5WB8gokVn0xfeu%2FZV%2BiNM1dgI%3D     
&SignatureMethod=HMAC-SHA1    
&SignatureNonce=15215528852396   
&SignatureVersion=1.0   
&AccessKeyId=key-test   
&Timestamp=2017-12-25T12:00:00Z   
…
```

## Common response parameters

Every response returns a unique RequestID regardless of whether the call is successful.

**Examples**

XML format

```
<? xml version="1.0" encoding="UTF-8"? > 
<!-Result Root Node-->
<Interface Name+Response>
    <!-Return Request Tag-->
    <RequestId>4C467B38-3910-447D-87BC-AC049166F216</RequestId>
    <!-Return Result Data-->
</Interface Name+Response>
```

JSON format

```
{
    "RequestId": "4C467B38-3910-447D-87BC-AC049166F216"
    /* Return Result Data */
}
```

