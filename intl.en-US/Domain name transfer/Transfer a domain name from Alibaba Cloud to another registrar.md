# Transfer a domain name from Alibaba Cloud to another registrar

You can transfer domain names that are registered at Alibaba Cloud to another registrar. This topic describes how to transfer a domain name from Alibaba Cloud to another registrar.

## Background information

You can transfer a domain name from Alibaba Cloud to another registrar. The transfer process is usually completed within five to seven days. After you transfer a domain name from Alibaba Cloud to another registrar, you cannot use the services provided by Alibaba Cloud Domains for the domain name.

## Rules on transferring a domain name from Alibaba Cloud

A domain name can be transferred to another registrar regardless of the real-name verification status of the domain name, such as verified, not verified, or failed. However, you must comply with the rules listed in the following table when you transfer a domain name from Alibaba Cloud to another registrar.

**Note:** If your domain name uses Alibaba Cloud Domain Name System \(DNS\) servers, you must change the DNS servers to those of the new registrar before the transfer. Otherwise, your domain name cannot be correctly resolved.

|Rule|Description|
|----|-----------|
|The current domain name registrar is Alibaba Cloud.|N/A|
|The domain name has been registered at least 60 days.|N/A|
|The domain name does not expire within 15 days.|We recommend that you transfer your domain name at least 30 days before it expires in case your domain name expires during the transfer process.|
|It has been more than 60 days since the domain name was transferred to Alibaba Cloud.|N/A|
|The status of the domain name is normal at the time of transfer.|-   The domain name is not in the Transfer Prohibited state.
-   The domain name does not have any overdue payments and is not under any arbitration or legal proceedings.
-   The domain name registrant has a clear identity and is not involved in any dispute. |
|It has been more than 45 days since the domain name was renewed or redeemed upon expiration.|You can transfer a domain name to another registrar 45 days after the last renewal. After the domain name is transferred to another registrar, the validity period of the domain name is extended by one year.|

## Procedure

1.  Submit a transfer-out request to obtain the transfer key.

    1.  Log on to the [Alibaba Cloud Domains console](https://dc.console.aliyun.com).

    2.  On the **Domain Name List** page, find the domain name that you want to transfer to another registrar and click **Manage** in the **Action** column. The **Basic Information** page appears.

    3.  In the left-side navigation pane, click **Domain Transfer-Out**.

    4.  Check the email address specified for **Registrant Email** and click **Next**.

        **Note:** The email address of the registrant must be valid because the transfer key for the domain name is sent to this email address. If the email address of the registrant is invalid, click **Change Email** next to **Registrant Email** to change the email address.

    5.  Obtain a verification code, enter the code in the **Email Verification Code** field, and then click **Next**.

        **Note:** In consideration of system stability and security, Alibaba Cloud takes about 1 minute to send the transfer key to the email address of the registrant. Obtain the transfer key in the email sent by Alibaba Cloud.

        -   If no transfer key is received, click **Resend Transfer Code**.
        -   If the email address is invalid, click **Registrant Email** to change the email address.
2.  Submit a transfer-in request in the system of the new registrar.

    1.  Submit a transfer-in request and provide the transfer key as required by the new registrar.

    2.  Complete the transfer process based on the rules of the new registrar.

    3.  Check whether your email address receives the confirmation email from the new registrar.

3.  When Alibaba Cloud receives a transfer request from the new registrar, Alibaba Cloud automatically sends a confirmation email to the email address of the domain name registrant.

    -   No further step is required for the transfer. The domain name is automatically transferred to the new registrar after five to seven days.
    -   For more information about how to cancel the transfer, see the following section.

## Cancel a transfer-out request

After you submit a transfer-out request in the Alibaba Cloud Domains console, you can cancel the transfer-out request before the transfer-out request is approved. To cancel a transfer-out request, perform the following steps:

1.  Log on to the [Alibaba Cloud Domains console](https://dc.console.aliyun.com). Click the domain name for which you want to cancel the transfer-out request to go to the **Basic Information** page.

2.  In the left-side navigation pane, choose **Domain Transfer-Out** \> **Cancel Transfer-Out**.

    **Note:** If the **Cancel Transfer-Out** button is unavailable on the **Domain Transfer-Out** page, the domain name has been transferred to the new registrar. You can wait 60 days and then transfer the domain name to Alibaba Cloud again. For more information, see [Transfer a domain name to Alibaba Cloud](/intl.en-US/Domain name transfer/Transfer a domain name to Alibaba Cloud.md).


## What to do next

You can query the transfer status on WHOIS lookup or at the registrar to which the domain name is transferred. To query the registrar information of a domain name on Alibaba Cloud WHOIS lookup, perform the following steps:

1.  Go to the Alibaba Cloud [WHOIS](https://www.alibabacloud.com/zh/whois) page.

2.  Enter the transferred domain name in the search box and click **Search** to view the current registrar of the domain name.


