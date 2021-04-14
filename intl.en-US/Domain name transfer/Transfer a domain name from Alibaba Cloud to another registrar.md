# Transfer a domain name from Alibaba Cloud to another registrar

You can transfer domain names that are registered with Alibaba Cloud to another registrar. This topic describes how to transfer a domain name from Alibaba Cloud to another registrar.

## Background information

You can transfer a domain name from Alibaba Cloud to another registrar. The transfer process is usually completed within five to seven days. After you transfer a domain name from Alibaba Cloud to another registrar, you cannot use the services provided by Alibaba Cloud Domains for the domain name.

## Rules on transferring a domain name from Alibaba Cloud

A domain name can be transferred to another registrar regardless of the real-name verification status of the domain name However, the transfer process must comply with the rules described in the following table.

**Note:**

-   If your domain name uses Alibaba Cloud Domain Name System \(DNS\) servers, you must change the DNS servers to those of the new registrar before the transfer. Otherwise, your domain name cannot be resolved.
-   If your domain name was registered with or transferred to Alibaba Cloud before 2016, the contact information may be incomplete because the domain name registry used an earlier version of the registration system at that time. In this case, you must first supplement the required information by transferring the ownership of the domain name and then submit a transfer-out request to obtain the transfer key.

|Rule|Description|
|----|-----------|
|The current domain name registrar must be Alibaba Cloud.|-|
|The domain name must have been registered at least 60 days ago.|-|
|The domain name cannot be transferred out 15 days before the domain name expires.|We recommend that you transfer your domain name at least 30 days before it expires. This prevents the expiration of your domain name during the transfer process.|
|The domain name can be transferred out 60 days after it is transferred to Alibaba Cloud.|-|
|The domain name must be in a normal state at the time when it is transferred.|-   The domain name is not in the Transfer Prohibited state.
-   The domain name does not have overdue payments and is not under arbitration or legal proceedings.
-   The domain name registrant has a clear identity and is not involved in disputes. |
|The domain name can be transferred 45 days after it is renewed or redeemed after expiration.|You can transfer a domain name to another registrar 45 days after the last renewal. After the domain name is transferred to another registrar, the validity period of the domain name is extended by one year.|

## Procedure

1.  Submit a transfer-out request to obtain the transfer key.

    1.  Log on to the [Alibaba Cloud Domains console](https://dc.console.aliyun.com). The Domain Name List page appears.

    2.  On the **Domain Name List** page, find the domain name that you want to transfer to another registrar and click **Manage** in the **Action** column. The **Basic Information** page appears.

    3.  In the left-side navigation pane, click **Domain Transfer-Out**.

    4.  Check the email address specified for the **Registrant Email** parameter and click **Next**.

        **Note:** The email address of your registrant must be valid because the transfer key for the domain name is sent to this email address. If the email address specified for the **Registrant Email** parameter is invalid, click **Change Email** next to **Registrant Email** to change the email address.

    5.  Obtain and enter the verification code in the **Email Verification Code** field, and then click **Next**.

        **Note:** For system stability and security purposes, Alibaba Cloud requires about 1 minute to send the transfer key to the email address that you specified. You can obtain the transfer key in the email.

        -   If no transfer key is received, you can click **Get Verification Code** again to request the transfer key.
        -   If the email address is invalid, you can click **Change Email** to change the email address.
2.  Submit a transfer-in request in the system of the new registrar.

    1.  Submit a transfer-in request and provide the transfer key as required by the new registrar.

    2.  Complete the transfer process based on the rules of the new registrar.

    3.  Check whether your email address receives the confirmation email from the new registrar.

3.  After Alibaba Cloud receives a transfer request from the new registrar, Alibaba Cloud automatically sends a confirmation email to the email address of the domain name registrant.

    -   No further step is required for the transfer. The domain name is automatically transferred to the new registrar after five to seven days.
    -   If you want to cancel the transfer, perform the operations described in the "Cancel a transfer-out request" section.

## Cancel a transfer-out request

After you submit a transfer-out request in the Alibaba Cloud Domains console, you can cancel the transfer-out request before the transfer-out request is approved. To cancel a transfer-out request, perform the following steps:

1.  Log on to the [Alibaba Cloud Domains console](https://dc.console.aliyun.com). The Domain Name List page appears. On the Domain Name List page, find the domain name for which you want to cancel the transfer-out request and click its name to go to the **Basic Information** page.

2.  In the left-side navigation pane, choose **Domain Transfer-Out** \> **Cancel Transfer-Out**.

    **Note:** If the **Cancel Transfer-Out** button is unavailable on the **Domain Transfer-Out** page, the domain name has been transferred to the new registrar. You must wait 60 days before you can transfer the domain name to Alibaba Cloud again. For more information, see [Transfer a domain name to Alibaba Cloud](/intl.en-US/Domain name transfer/Transfer a domain name to Alibaba Cloud.md).


## What to do next

You can query the transfer status of the domain name on the WHOIS page or at the registrar to which the domain name is transferred. To query the registrar information of a domain name on the Alibaba Cloud WHOIS page, perform the following steps:

1.  Go to the [Alibaba Cloud WHOIS](https://www.alibabacloud.com/zh/whois) page.

2.  Enter the transferred domain name in the search bar and click **Search**. Then, you can view the current registrar of the domain name.


