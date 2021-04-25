# FAQ about custom DNS servers

If you want to use custom Domain Name System \(DNS\) servers to resolve your domain name, you must first create your own DNS servers. This topic provides answers to frequently asked questions about custom DNS servers.

-   [What is a custom DNS server?](#section_rbt_xsd_b2b)
-   [What are the naming rules for a DNS server?](#section_sbt_xsd_b2b)
-   [How many DNS servers can I create at most?](#section_tbt_xsd_b2b)
-   [Do custom DNS servers support IPv6 addresses?](#section_ubt_xsd_b2b)
-   [How many IP addresses can I configure for a DNS server?](#section_vbt_xsd_b2b)
-   [Can I change or delete a server name?](#section_wbt_xsd_b2b)
-   [Can I change or delete the IP addresses of a DNS server?](#section_xbt_xsd_b2b)
-   [Does a custom DNS server take effect immediately after it is created?](#section_act_xsd_b2b)
-   [Can I delete a custom DNS server after it is created?](#section_nf1_aoo_xyu)

## What is a custom DNS server?

A custom DNS server is a self-managed DNS server and provides the DNS resolution service. Professional technical skills are required to create custom DNS servers. If you do not have such skills, we recommend that you use the DNS service provided by your DNS service provider.

## What are the naming rules for a DNS server?

Take note of the following naming rules when you specify a name for a DNS server:

-   The name of a DNS server can contain only letters, digits, periods \(.\), and hyphens \(-\). The name is not case-sensitive and cannot start or end with a period \(.\) or hyphen \(-\).
-   It cannot contain spaces or the following special characters: exclamation points \(!\), dollar signs \($\), ampersands \(&\), and question marks \(?\).
-   The name of a DNS server can be up to 80 characters in length.

We recommend that you include dns or ns in your server name, such as dns1.yourdomain.com and dns2.yourdomain.com.

## How many DNS servers can I create at most?

You can create a maximum of 13 DNS servers. The actual number of DNS servers that you can create is determined by the domain name registry.

## Do custom DNS servers support IPv6 addresses?

Yes, custom DNS servers support IPv6 addresses.

## How many IP addresses can I configure for a DNS server?

You can configure 1 to 13 IP addresses for a DNS server. The actual number of IP addresses that you can configure for a DNS server is determined by the domain name registry.

## Can I change or delete a server name?

No, you cannot change or delete a server name.

## Can I change or delete the IP addresses of a DNS server?

Yes, you can change or delete the IP addresses of a DNS server. However, at least one IP address must be retained.

## Does a custom DNS server take effect immediately after it is created?

No, a custom DNS server requires several minutes to take effect after it is created.

## Can I delete a custom DNS server after it is created?

Yes, you can delete a custom DNS server after it is created. If you fail to delete a custom DNS server, seek technical support on the [Smart Online](https://drcloud.aliyun.com/home) page or by [submitting a ticket](https://selfservice.console.aliyun.com/ticket/createIndex). Alibaba Cloud technical engineers will then identify the failure cause for you.

