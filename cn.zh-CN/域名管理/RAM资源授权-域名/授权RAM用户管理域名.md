# 授权RAM用户管理域名

为细分账号权限，提升账号安全性，您可以通过访问控制RAM（Resource Access Management）将域名的管理权限授权给RAM用户，使被授权的RAM用户可以管理域名。本文为您介绍如何授权RAM用户管理域名。

已成功创建RAM用户，请参见[创建RAM用户](/cn.zh-CN/用户管理/创建RAM用户.md)。

访问控制RAM是阿里云提供的资源访问控制服务，您可以通过RAM授权RAM用户管理域名。默认支持系统策略和自定义策略两种，域名的系统策略目前仅支持**AliyunDomainFullAccess**，即管理域名的权限策略。如果系统策略无法满足您的需求，您可以创建自定义策略实现精细化权限管理。

**说明：**

-   本文介绍了两种自定义策略：设置只读权限和管理某个域名的权限。如您还需创建其他自定义策略，请参见[创建自定义策略](/cn.zh-CN/权限策略管理/自定义策略/创建自定义策略.md)。
-   如需添加域名解析的权限管理，请参见[RAM鉴权](/cn.zh-CN/API文档/RAM鉴权.md)。

## 授权RAM用户读写权限

您可以通过RAM，添加**AliyunDomainFullAccess**系统策略给对应的RAM用户，授权RAM用户管理域名。该权限允许被授权的RAM用户管理主账号下的所有域名资源，属于最大权限。

1.  使用阿里云账号登录[RAM控制台](https://ram.console.aliyun.com)。

2.  [创建RAM用户](/cn.zh-CN/用户管理/创建RAM用户.md)。

3.  在左侧导航栏的**人员管理**菜单下，单击**用户**。

4.  在**用户登录名称/显示名称**列表下，找到目标RAM用户。

5.  单击**添加权限**，被授权主体会自动填入。

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3796449951/p71551.png)

6.  在**添加权限**对话框中，配置授权信息。

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/3796449951/p71553.png)

    1.  授权范围选择**云账号全部资源**。

    2.  选择权限为**系统策略**。

    3.  在搜索框中输入domain，会展现域名相关的系统策略。

    4.  单击**AliyunDomainFullAccess**，添加至**已选择**区域框中。

7.  单击**确定**。

8.  单击**完成**。


## 授权RAM用户只读权限

您可以通过RAM创建自定义策略，授权给RAM用户只读权限。该权限允许被授权的RAM用户查看主账号下的域名，但不支持对域名进行管理。自定义策略的脚本如下：

```
{
   "Version": "1",
   "Statement": [
     {
       "Action": [
         "domain:Query*"
       ],
       "Resource": "acs:domain:*:*:*",
       "Effect": "Allow"
     }
    ]
}
```

详细操作步骤请参见[创建自定义策略](/cn.zh-CN/权限策略管理/自定义策略/创建自定义策略.md)。

## 授权RAM用户管理单个域名的权限

您可以通过RAM创建自定义策略，授权RAM用户管理某个域名的权限。该权限允许被授权的RAM用户管理某一个域名的资源，例如，授权RAM用户管理“example.com”域名。自定义策略的脚本如下：

**说明：**

-   目前仅支持对以下Action授权，关于各Action的鉴权规则，具体请参见[Domain API鉴权规则](/cn.zh-CN/域名管理/RAM资源授权-域名/Domain API鉴权规则.md)。
-   RAM子账号授权成功后，您可以使用RAM子账号登录[阿里云域名控制台](https://dc.console.aliyun.com)并查看主账号下的所有域名，但只能对被授权的域名进行管理操作。

```
{
  "Version": "1",
  "Statement": [
    {
      "Action": [
      "domain:DnsModification",
      "domain:SecuritySetting",
      "domain:RealNameVerificationOperation",
      "domain:DnsHostModification",
      "domain:CreateOrderActivate",
      "domain:CreateOrderRenew",
      "domain:CreateOrderRedeem",
      "domain:CreateOrderTransfer",
      "domain:DomainTransferInOperation",
      "domain:DomainTransferOutOperation",
      "domain:QualificationAuditOperation",
      "domain:EnsSetting",
      "domain:DnsSecSetting",
      "domain:SaveArtExtension",
      "domain:CreateOrderPendingDelete"
      ],
      "Resource": "acs:domain:*:*:domain/example.com",
      "Effect": "Allow"
    },
    {
      "Action":
      "domain:Query*",
      "Resource": "acs:domain:*:*:*",
      "Effect": "Allow"
    }
  ]
}
```

详细操作步骤请参见[创建自定义策略](/cn.zh-CN/权限策略管理/自定义策略/创建自定义策略.md)。

使用被授权的RAM用户的账号登录控制台，请参见[RAM用户登录控制台](/cn.zh-CN/用户管理/RAM用户登录控制台.md)。

