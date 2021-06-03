# Domain name validity

This topic describes the requirements for validity of domain names.

A valid domain name is subject to the following conditions:

-   Domain names are case-insensitive and are not sensitive to simplified or traditional Chinese characters.
-   A valid domain name must be 1 to 63 characters in length \(excluding the suffix\).
-   A valid English domain name can contain letters \(a-z\), digits \(0-9\), and hyphens \(-\). However, a valid English domain name cannot start or end with a hyphen, and cannot contain a hyphen in the third and fourth character positions at the same time.
-   A valid Chinese domain name must contain at least one Chinese character \(simplified or traditional\) in addition to the valid characters that are allowed in an English domain name. The length of a Chinese domain name is measured in Punycode after conversion.
-   Request parameters \(Punycode\) that start with "xn-" are not supported. Use a Chinese domain name as a request parameter.

