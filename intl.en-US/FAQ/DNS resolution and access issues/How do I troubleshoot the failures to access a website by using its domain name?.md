# How do I troubleshoot the failures to access a website by using its domain name?

This topic describes the common causes for failures to access a website by using its domain name and shows you how to resolve these issues.

-   [Failed to access a website because the domain name has expired](#section_ulx_wmd_b2b)
-   [Failed to access a website because the domain name has expired and requires renewal](#section_r4w_hnd_b2b)

## Failed to access a website because the domain name has expired

-   Cause: The domain name has expired, and the Domain Name System \(DNS\) records of the domain name are disabled. As a result, the website to which the domain name points cannot be accessed.
-   Solution: Check the validity period of the domain name on the [WHOIS](https://whois.aliyun.com/) page. If the domain name has expired, renew it. For more information, see [Renew a domain name](/intl.en-US/Domain name management/Renew domain names/Renew a domain name.md). After the domain name is renewed, the resolution service will be resumed for the domain name within 24 to 48 hours.

## Failed to access a website because the domain name has expired and requires renewal

-   Cause 1: The domain name has expired and has not been renewed.

    Solution: Log on to the Alibaba Cloud Domains console by using the Alibaba Cloud account to which the domain name belongs, and renew the domain name. For more information, see [Renew a domain name](/intl.en-US/Domain name management/Renew domain names/Renew a domain name.md).

-   Cause 2: The domain name has been renewed after it expired, but the on-premises DNS cache has not been refreshed. As a result, the domain name resolution is not working.

    Solution: Clear the browser cache or use another browser.


