# Domain name transfer

This topic provides answers to some commonly asked questions about how to transfer domain names to and from Alibaba Cloud.

-   [How long does it take to transfer a domain name to Alibaba Cloud?](#section_mzj_xta_2zz)
-   [How do I transfer a domain name to Alibaba Cloud?](#section_fj8_f29_kt5)
-   [How do I enter the name and contact information of the domain name registrar when I transfer a domain name to Alibaba Cloud?](#section_k1i_71g_s0t)
-   [How long is the transfer key valid before I submit a domain name transfer request to the new registrar?](#section_b45_7uv_qvm)
-   [How do I transfer a domain name that is in use to Alibaba Cloud?](#section_aok_kkl_u8t)
-   [What do I do if the original domain name registrar does not allow me to transfer the domain name?](#section_9gu_rrk_cf7)
-   [What do I do if I receive the message "The domain name is in the transfer prohibited state and cannot be transferred."?](#section_kgf_8jz_y1s)
-   [What do I do if I receive the message "The domain name format is incorrect. Please try again."?](#section_tp2_iwv_5nf)
-   [What do I do if I receive the message "Sorry. Your domain name transfer key is incorrect."?](#section_fqw_elx_yei)

## How long does it take to transfer a domain name to Alibaba Cloud?

The transfer of a domain name to Alibaba Cloud must be confirmed by the original domain name registrar. The time required for a successful transfer depends on the confirmation time of the original domain name registrar. The transfer process usually takes five to seven days.

## How do I transfer a domain name to Alibaba Cloud?

For more information, see [Transfer a domain name to Alibaba Cloud](/intl.en-US/Domain name transfer/Transfer a domain name to Alibaba Cloud.md).

## How do I enter the name and contact information of the domain name registrar when I transfer a domain name to Alibaba Cloud?

If you want to transfer a domain name from its current registrar to Alibaba Cloud, the current registrar requires that you enter the following information about the new registrar \(Alibaba Cloud\):

Full name: Alibaba Cloud Computing Co., Ltd. \(formerly HiChina\)

Contact: 95187-1

## How long is the transfer key valid before I submit a domain name transfer request to the new registrar?

A transfer key is valid for 15 days. After you obtain a transfer key, submit a domain name transfer request to the new registrar as soon as possible. If the transfer key expires, you must obtain a new one.

## How do I transfer a domain name that is in use to Alibaba Cloud?

To transfer a domain name such as a website or an email address that is in use and is registered with another domain name registrar to Alibaba Cloud, perform the following operations:

1.  Change the DNS servers of the domain name to Alibaba Cloud DNS servers.

    For more information, see [Quick Start](https://www.alibabacloud.com/help/zh/doc-detail/106669.htm).

2.  Change the DNS servers of the domain name to ns1.alidns.com and ns2.alidns.com at the original domain name registrar.

    **Note:** Make sure that the DNS records on the new and original DNS servers are the same within 48 hours after you change the DNS servers.

3.  Submit a request to transfer a domain name.

    For more information about how to transfer a domain name to Alibaba Cloud, see [Transfer a domain name to Alibaba Cloud](/intl.en-US/Domain name transfer/Transfer a domain name to Alibaba Cloud.md).


## What do I do if the original domain name registrar does not allow me to transfer the domain name?

If the original domain name registrar does not allow you to transfer the domain name, you can file a complaint by using one of the following methods:

-   For China Internet Network Information Center \(CCNIC\) domain names, such as .cn, .中国, and .公司, send an email to supervise@cnnic.cn or dial 010-58813000 to file a complaint.
-   For international domain names, go to [Complaint regarding international domain names](http://reports.internic.net/cgi/registrars/problem-report.cgi?spm=a2c4g.11186623.2.21.VgStC5&file=problem-report.cgi) to file a complaint.

## What do I do if I receive the message "The domain name is in the transfer prohibited state and cannot be transferred."?

Cause: A transfer prohibition lock is enabled for the domain name.

Solution: Contact the original domain name registrar to disable the transfer prohibition lock for the domain name. Go to the [WHOIS](https://www.alibabacloud.com/whois) page and enter the domain name to view the status of the domain name.

## What do I do if I receive the message "The domain name format is incorrect. Please try again."?

Cause: Alibaba Cloud does not allow the transfer of domain names that contain the current suffix.

Solution: For domain names that can be transferred to Alibaba Cloud, go to the [Pricing of domain names](https://www.alibabacloud.com/zh/domain/pricing) page.

## What do I do if I receive the message "Sorry. Your domain name transfer key is incorrect."?

Cause: The transfer key of the domain name is incorrect.

Solution: Obtain a new transfer key from the original domain name registrar. For more information, see [Obtain a transfer key for transferring a domain name](/intl.en-US/Domain name transfer/Obtain a transfer key for transferring a domain name.md).

**Note:**

-   You must obtain the transfer key from the original domain name registrar. Alibaba Cloud cannot obtain it for you.
-   We recommend that you enter the transfer key. If you copy and paste the transfer key, do not copy the spaces.
-   The transfer key contains special characters, which must be entered in full accordance with the transfer key provided by the original domain name registrar.
-   The system automatically determines whether your transfer key is valid. If you enter incorrect transfer keys multiple times, contact the original domain name registrar to confirm the transfer key.

