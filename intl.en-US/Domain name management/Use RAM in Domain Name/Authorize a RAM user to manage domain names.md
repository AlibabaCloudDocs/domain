# Authorize a RAM user to manage domain names

To implement fine-grained access control and improve account security, you can use Resource Access Management \(RAM\) to grant management permissions on domain names to RAM users. Then, the authorized RAM users can manage domain names. This topic describes how to authorize a RAM user to manage domain names.

A RAM user is created. For more information, see [Create a RAM user](/intl.en-US/RAM User Management/Create a RAM user.md).

RAM is a resource access control service provided by Alibaba Cloud. You can use RAM to authorize a RAM user to manage your domain names. System policies and custom policies are supported by default. The **AliyunDomainFullAccess** system policy is provided for Alibaba Cloud Domains. You can create a custom policy to provide finer-grained access control if the default system policies cannot meet your requirements.

**Note:** This topic describes two custom policies, which are used to grant a RAM user the read-only permissions on all domain names and the management permissions on a single domain name. For more information about how to create other custom policies, see [Create a custom policy](/intl.en-US/Policy Management/Custom policies/Create a custom policy.md).

## Grant the read and write permissions to a RAM user

You can use RAM to attach the **AliyunDomainFullAccess** system policy to a RAM user to authorize the user to manage domain names. This is the highest-level permission. The authorized RAM user can manage all domain names within the Alibaba Cloud account.

**Note:** You are not allowed to use a RAM user to register or renew a domain name in the Alibaba Cloud Domains console or by calling Domains API operations. If you want to register or renew a domain name, use your Alibaba Cloud account.

1.  Log on to the [RAM console](https://ram.console.aliyun.com) by using your Alibaba Cloud account.

2.  [Create a RAM user](/intl.en-US/RAM User Management/Create a RAM user.md).

3.  In the left-side navigation pane, choose **Identities** \> **Users**.

4.  On the Users page, find the RAM user that you want to authorize in the **User Logon Name/Display Name** column.

5.  Click **Add Permissions** in the Actions column. In the Add Permissions panel, information is automatically entered in the Principal field.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9448017951/p71551.png)

6.  Configure the permission policies.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/9448017951/p71553.png)

    1.  Set Authorization to **Alibaba Cloud account all resources**.

    2.  Set Select Policy to **System Policy**.

    3.  Enter domain in the search box. System policies for the domain name are displayed.

    4.  Click **AliyunDomainFullAccess** to add the policy to the **Selected** section.

7.  Click **OK**.

8.  Click **Complete**.


## Grant the read-only permissions to a RAM user

You can use RAM to create a custom policy to grant the read-only permissions on domain names to a RAM user. The authorized RAM user can view domain names within the Alibaba Cloud account but cannot manage these domain names. Add the following script to the custom policy:

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

For more information, see [Create a custom policy](/intl.en-US/Policy Management/Custom policies/Create a custom policy.md).

## Authorize a RAM user to manage a single domain name

You can use RAM to create a custom policy to authorize a RAM user to manage a single domain name. The authorized RAM user can manage a domain name such as example.com. Add the following script to the custom policy:

**Note:**

-   Only the operations listed in the following script can be authorized. For more information about the authorization rules of each operation, see [Authentication rules for the Domains API](/intl.en-US/Domain name management/Use RAM in Domain Name/Authentication rules for the Domains API.md).
-   After you attach the custom policy to a RAM user, the RAM user can log on to the [Alibaba Cloud Domains console](https://dc.console.aliyun.com) to view all the domain names within the Alibaba Cloud account. However, the RAM user can manage only the domain name specified in the custom policy.

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

For more information, see [Create a custom policy](/intl.en-US/Policy Management/Custom policies/Create a custom policy.md).

Log on to the RAM console as the authorized RAM user. For more information, see [Log on to the console as a RAM user](/intl.en-US/RAM User Management/Log on to the console as a RAM user.md).

