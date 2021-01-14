# Transfer domains to another Alibaba Cloud account

This topic describes how to transfer a domain name from one Alibaba Cloud account to another Alibaba Cloud account. For example, you had another person purchase a domain name for you, and now you need to transfer the domain name to your own Alibaba Cloud account, or you need to transfer a domain name from your Alibaba Cloud account to another Alibaba Cloud account.

The domain name is within its validity period.

You can query the registration and expiration dates of a domain name on [Alibaba Cloud WHOIS](https://www.alibabacloud.com/zh/whois). If your domain name has already expired, you must renew the domain name first. For more information, see [Renew a domain name](/intl.en-US/Domain name management/Renew domain names/Renew a domain name.md).

The following example demonstrates how to transfer domain names from account A to account B.

1.  The domain names are under account A. Use account A to log on to the [Domains console](https://signin-intl.aliyun.com/doc.onaliyun.com/login.htm).

2.  Use either of the following methods to go to the **ID Transfer** tab.

    -   Method 1:
        1.  On the **Domain Names** page, find the target domain name.
        2.  Click **Manage** in the **Actions** column, and then click **Transfer between ID**.
    -   Method 2:
        -   Transfer multiple common domains: In the left-side navigation pane, choose **Bulk Operations** \> **Common Bulk Operation** \> **ID Transfer**.
        -   Transfer multiple .cn domains: In the left-side navigation pane, choose **Bulk Operations** \> **CNNIC Bulk Operation** \> **ID Transfer**.
3.  On the ID Transfer page, set the following parameters to transfer the domain names to another Alibaba Cloud account.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/0431564751/p68472.png)

    |Parameter|Description|
    |---------|-----------|
    |**Bulk Operation**|Select a method to transfer one or more domain names. The following methods are supported:     -   **Enter Domain Names**: In the **Domain Names** field, enter the domain names that you want to transfer.

**Note:** Enter one domain name in each row. You can enter up to 1,000 domain names.

    -   **Upload File**: If the domain names that you want to transfer are saved in a local file, upload the file.

**Note:** Supported file formats are XLS and XLSX. Enter one domain name in each row. The maximum file size is 2 MB. |
    |**Transfer to**|Enter the account to which you want to transfer the domain names. In this example, enter account B.|
    |**Security Verification**|Click Get Verification Code to obtain a verification code.|
    |**Email Verification Code**|Enter the verification code that the verified email address receives.|

4.  Click **Submit** to transfer the domain names to the specified account.


Use account B to log on to the Domains console, and verify that the domain names are under account B.

