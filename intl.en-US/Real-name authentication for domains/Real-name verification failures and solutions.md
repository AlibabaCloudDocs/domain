# Real-name verification failures and solutions

After you submit all the information required for the real-name verification, Alibaba Cloud immediately submits the information to the registry-accredited authority for verification. The verification authority checks the submitted information and the domain name registration details for authenticity, consistency, and completeness. If the verification fails, you can consult this topic for solutions.

-   [Invalid certificate information](#section_spz_gqk_5gb)
-   [Invalid certificate type or certificate number](#section_j6h_gqh_trg)
-   [Inconsistent registrant information or certificate information](#section_dgw_jqk_5gb)
-   [Unclear or covered photos of certificates](#section_42l_86n_adt)
-   [Newly issued certificates or certificates not found in the database of the verification authority](#section_yae_rfu_77w)
-   [Incomplete registrant certificates](#section_lab_tuk_3xq)
-   [Invalid registrant certificates](#section_gj8_r8p_ziy)
-   [Validity verification failure of the registrant identity](#section_nf9_229_i2n)
-   [Lack of registrant certificates](#section_itj_3rk_5gb)
-   [Certificate numbers not found in the database of the verification authority or the failure of registrant certificate verification](#section_aws_2sk_5gb)
-   [Invalid registrant contact information](#section_x76_bqe_bwl)
-   [Sensitive words in domain names](#section_oig_mkd_9qt)
-   [Material upload failure due to invalid image format or image size](#section_uxn_31v_tob)
-   [Material upload failure due to invalid file format](#section_be4_hu7_wae)

## Invalid certificate information

Problem description: The real-name verification failed and the message **Verification failed due to invalid certificate information** or **Verification rejected due to invalid certificate information** appears.

Solution:

1.  Check whether the name you entered in the **Registrant** field is the same as the name on your certificate.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/1778507951/p46399.png)

2.  Check whether the name you entered in the **Certification number** field is the same as the name on your certificate.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2778507951/p46412.png)

3.  Check whether the certificate type you selected for the **Real name certification type** parameter is the same as that of the certificate.

    ![Verification failed - certificate type](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2778507951/p114793.png)

4.  Check whether the certificate issue date meets the requirements of the real-name verification.

    -   Make sure that your certificate has been valid for at least 10 calendar days. If you have a newly issued certificate, we recommend that you submit a real-name verification request 10 calendar days after the certificate is issued.
    -   Make sure that your certificate is valid before you submit the certificate information for the real-name verification.

        **Note:** The real-name verification may fail if your certificate is due to expire.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2778507951/p46465.png)

5.  Check whether the uploaded materials meet the requirements of the real-name verification.
    -   You can upload a scanned color copy or an image of the original identity document. Images of the JPG and BMP formats are supported. The image can be 55 KB to 1 MB in size.
    -   You must submit a clear photo that contains the complete identity document, including the borders of the identity document without cover or smudges. Seals affixed by authorities must be in red, clear, and complete.
    -   Do not alter the identity document or modify the content of the identity document by using Photoshop. If the format of the image is not supported, **do not directly change the file name extension**. Instead, you can use an image editor to convert the image format to JPG or BMP.
6.  Check whether your household registration record is being transferred or you have changed your name.

    If your household registration record is being transferred or you have changed your name, the real-name verification may fail. In this case, submit a scanned copy of the residency certificate with seals affixed by the public security bureaus. You can also submit a real-name verification request after your household registration record is transferred. Whether you can pass the real-name verification is determined by the verification authority.

7.  Check whether the domain name registrant has a special occupation.

    Individuals with special occupations, such as military personnel, cannot use the 18-digit resident identity card number for the real-name verification. We recommend that you submit other identity documents for the verification.


## Invalid certificate type or certificate number

Problem description: The real-name verification failed because the certificate type specified by the **Real name certification type** parameter is inconsistent with the type of the uploaded certificate or because the certificate number your entered is invalid.

Solution:

-   Check whether the certification type you specified is the same as that of the uploaded certificate.

    The certificate type specified by the **Real name certification type** parameter must be the same as that of the individual identity document or organization certificate that you uploaded.

    **Note:**

    -   Organizations and enterprises in mainland China must submit a certificate that contains a valid **18-digit** Unified Social Credit Code. Organizations and enterprises outside mainland China must submit a certificate of organization issued by an agency outside mainland China.
    -   Individuals in mainland China must submit a resident identity card. Individuals outside mainland China must submit the information from a passport.
    ![Verification failed - certificate type](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2778507951/p114793.png)

-   Check whether the certificate number you entered is correct.

    The certificate number specified in the verification information must be the same as that on the uploaded certificate. Make sure that you distinguish between digit 0 and letter O, digit 1 and letter I, and digit 8 and letter B.


## Inconsistent registrant information or certificate information

Problem description: The real-name verification failed and the message **Inconsistent registrant information** or **Submitted information inconsistent with registrant information** appears.

Possible cause: The submitted image of the certificate is a mirrored image, or the certificate specified in the verification information is different from the uploaded certificate.

Solution:

-   Check whether the image of the certificate meets the requirements. Some cameras may automatically mirror images. In this case, we recommend that you use another phone or camera to take photos. Before you upload the image of your certificate, make sure that it is not a mirrored image. If you need to upload a scanned copy of a certificate, make sure that it is a scanned color copy.
-   Check whether the name of the domain name registrant specified in the domain name information is the same as that on the uploaded identity document. Pay close attention when you enter words with similar forms or pronunciations. Do not use abbreviated or shortened names.
-   The certificate type specified by the Real-name certificate type parameter must be the same as that of the uploaded certificate. For example, if the selected certificate type is business license, you must upload an image or scanned copy of your business license.
-   The certificate number specified in the verification information must be the same as that on the certificate. If the selected certificate type is identification card or business license, make sure that the certificate number specified in the verification information is the same as that on the resident identity card or business license.

    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2778507951/p46412.png)

    **Note:**

    -   If your business license has duplicates, do not enter the number of a duplicate, such as \(1-1\).
    -   Make sure that you distinguish between digit 0 and letter O, digit 1 and letter I, and digit 8 and letter B.
    -   You must enter the complete certificate number.
-   Select the correct value for the **Country/Region** parameter. If you need to submit an image of the resident identity card or business license for the real-name verification, set the **Country/Region** parameter to mainland China. You can check the value of the **Country/Region** parameter in the following ways:
    -   The real-name verification for registrant profiles: On the **Registrant Profiles** page, find the profile that you want to view and click **View** in the **Operation** column. On the page that appears, you can view the value of the **Country/Region** parameter.
    -   The real-name verification for the transfer of domain name ownership: On the **Registrant Info Modification** tab of the Info Modification page, you can view the value of the **Country/Region** parameter.

## Unclear or covered photos of certificates

Problem description: The real-name verification failed and the message **Unclear or covered photo of certificate** appears.

Solution: Upload a clear and complete image of the certificate.

-   Clear: Make sure that key information on the certificate, such as the national emblem, seals affixed by the authority, name of the domain name registrant, and certificate number, is clear and complete.
-   Complete: The image of the certificate must contain the entire identity document and its borders, without cover, smudges, or watermarks.

**Note:** Do not add watermarks to the image of the certificate.

## Newly issued certificates or certificates not found in the database of the verification authority

Problem description: The real-name verification failed and the message **Certificate cannot be found in the database** or **Newly issued certificate** appears.

Possible cause: The certificate was newly issued and the certificate information has not been synchronized to the database of the verification authority.

Solutions:

-   Solution 1

    The information about the newly issued certificate or identity document has not been synchronized to the database of the verification authority. It takes a minimum of 10 calendar days to synchronize data. Submit the verification request 10 calendar days after the certificate is issued. You can check whether the information about a newly issued certificate is synchronized to the following organizations on their websites:

    -   [China Organization Data Service](https://www.cods.org.cn/): You can query the Unified Social Credit Code of an organization registered in mainland China.
    -   [National Enterprise Credit Information Publicity System](http://www.gsxt.gov.cn): You can query business licenses.
    ![](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/en-US/2778507951/p46465.png)

-   Solution 2

    Provide proof of identity documents affixed with seals of the authority that manages your certificate. You can also contact the corresponding data management center to update your information.


## Incomplete registrant certificates

Problem description: The real-name verification failed and the message **Incomplete registrant certificate** appears.

Solution: Submit an image that contains the entire identity document including the borders. If you choose to use the business license, scan all information on the license including the national emblem or the seals affixed by the authority that manages the business license.

**Note:** Do not add watermarks to the image of the certificate.

-   If you choose to use a resident identity card, take a photo of the side that contains the identity information.
-   If you need to submit an image of a household register, take a photo of the page that contains the household registration record of the domain name registrant.
-   If you need to submit an image of a foreign permanent resident ID card, take photos of both the front and back sides of the card.
-   If you need to submit a photo of a residence permit for Hong Kong \(China\), Macau \(China\), and Taiwan \(China\) residents, take photos of both the front and back sides of the permit.
-   If the certificate contains multiple pages, take a photo of the page that contains the organization name, certificate number, and seals affixed by the registration authority.

## Invalid registrant certificates

Problem description: The real-name verification failed and the message **Invalid registrant certificate** appears.

Possible cause: The image of the certificate you submitted is unclear or incomplete.

Solution:

-   Submit valid verification information. Submit a clear **scanned color copy or image** that contains the entire certificate. The certificate information, including the borders of the certificate and national emblem, must be clear and complete.

    **Note:** Printed copies or copies in black and white are not supported.

-   The certificate must be affixed with seals of the registration authority.
    -   mainland China
        -   Organizations: Submit an image of the business license or organization code certificate that contains a valid **18-digit** Unified Social Credit Code.
        -   Individuals: Submit an image or a scanned copy of the resident identity card or residence certificate issued in mainland China.
    -   outside mainland China
        -   Organizations: Submit an image of the required certificate of organization issued by an agency outside mainland China.
        -   Individuals: Submit an image of a valid identity document such as a passport.

## Validity verification failure of the registrant identity

Problem description: The real-name verification failed and the message **Failed to authenticate the registrant identity** appears.

Possible causes:

-   Specific information that you submitted is invalid or not authentic.
-   The verification authority failed to receive the latest information that you uploaded.

Solutions:

-   If specific information that you submitted is invalid or not authentic, verify the information or use another valid identity document and submit a real-name verification request again.
-   If you confirm that the submitted information is valid and authentic, wait one to three weekdays and submit a real-name verification request again.

## Lack of registrant certificates

Problem description: The real-name verification failed and the message **Lack of registrant certificate** appears.

Solution:

-   Individual domain name registrants must submit an image of the resident identity card or passport issued in mainland China. For more information, see [Examples of real-name verification information for individual registrants](/intl.en-US/Real-name authentication for domains/Real-name authentication examples/Examples of real-name verification information for individual registrants.md).
-   Organization domain name registrants must submit a business license, organization code certificate, or required certificate of organization issued by an agency outside mainland China. For more information, see [Examples of real-name verification information for organization registrants](/intl.en-US/Real-name authentication for domains/Real-name authentication examples/Examples of real-name verification information for organization registrants.md).

## Certificate numbers not found in the database of the verification authority or the failure of registrant certificate verification

Problem description: The real-name verification failed and the message **Certificate number cannot be found** or **Registrant certificate verification failed** appears.

Solution:

-   Check whether the name of the domain name registrant and 18-digit resident identity card number specified in the verification information are correct.

    **Note:** Individuals with special occupations, such as military personnel, cannot use the 18-digit resident identity card number for the real-name verification. We recommend that you submit other identity documents for the verification.

-   If the verification of the certificate fails, submit an image of the certificate and a screenshot of the web page that shows that the certificate is valid and has been provided by a qualified authority.

## Invalid registrant contact information

Problem description: The real-name verification failed and the message **Registrant contact information invalid** appears.

Possible cause: The name of the domain name registrant is different from the name on the individual identity document or organization certificate that you uploaded.

Solution: Check the information of the domain name registrant. Make sure that the name of the domain name registrant is the same as that on the uploaded certificate. If they are different, you must transfer the domain name to the actual registrant and complete the real-name verification by uploading the required materials during the transfer. For more information, see [Transfer domain name ownership](/intl.en-US/Domain name management/Change domain information/Transfer domain name ownership.md).

## Sensitive words in domain names

Problem description: The real-name verification failed because the verification system detected sensitive words in a domain name. The following messages appear:

-   **Registration denied due to the violation of Internet Domain Name Regulations article 27 circumstance 2: Jeopardizing national security, leaking state secrets, intending to overturn the government, or disrupting state integrity.**
-   **Registration denied due to the violation of Internet Domain Name Regulations article 27 circumstance 8: Infringing other people's legal rights and interests.**
-   **Registration denied due to the violation of Internet Domain Name Regulations article 27 circumstance 9: Other contents prohibited by laws and administrative regulations.**
-   **The domain name harms national honor and interests.**
-   **Sensitive words.**

Solution: If the real-name verification of a .cn domain name fails because its naming is invalid, the system will automatically issue a refund and CNNIC will delete the domain name. We recommend that you register another domain name and complete the real-name verification. For more information about the naming rules for domain names, see [Naming rules for domain names](/intl.en-US/Quick Start/Naming and Registration Suggestions for Domain Names/Naming rules for domain names.md).

## Material upload failure due to invalid image format or image size

Problem description: During the real-name verification, materials fail to be uploaded in the **Upload File** step, and a message that indicates that **the image format must be JPG or BMP and the image size must be in the range of 55 KB to 1 MB** appears.

![Image format not supported](../images/p175256.png)

Possible cause: The size or format of the image to be uploaded does not meet the requirements. The image must be of the JPG or BMP format.

Solution: Check whether the size of the uploaded image is 55 KB to 1 MB and whether the image format is JPG or BMP. If the uploaded image does not meet the requirements, use a third-party drawing tool \(such as the drawing software that comes with the operating system\) to convert the image format or resize the image. Do not directly modify the image suffix. Otherwise, the upload fails because the system cannot recognize the modified image.

## Material upload failure due to invalid file format

Problem description: During the real-name verification, materials fail to be uploaded in the **Upload File** page, and a message that indicates that **the file format is invalid** appears.

![File format not supported](../images/p175255.png)

Possible cause: The image format is not supported. Only the JPG and BMP formats are supported. The image suffix may be directly modified.

Solution: Check whether your image is in the JPG or BMP format. If not, do not directly modify the image suffix. Otherwise, the system fails to recognize the modified image. You can use a third-party drawing tool \(such as the drawing software that comes with the operating system\) to open the original image, save the image as a JPG or BMP image, and load the image again.

