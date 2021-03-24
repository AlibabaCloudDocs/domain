# API overview

The following tables list API operations available for use in Alibaba Cloud Domains. You can call these operations to purchase, renew, and manage domain names, and query domain names and domain name information. You can also update domain name information, change Domain Name System \(DNS\) servers, add DNS servers, and manage registrant profiles.

## Manage domain names

|Operation|Description|
|:--------|:----------|
|[QueryDomainList](/intl.en-US/API Reference (New)/Domain management/QueryDomainList.md)|Queries the domain names under your account.|
|[QueryDomainByInstanceId](/intl.en-US/API Reference (New)/Domain management/QueryDomainByInstanceId.md)|Queries the basic information of a domain name by instance ID.|
|[QueryContactInfo](/intl.en-US/API Reference (New)/Domain management/QueryContactInfo.md)|Queries the contact information of a domain name.|
|[QueryChangeLogList](/intl.en-US/API Reference (New)/Domain management/QueryChangeLogList.md)|Queries the operation logs of a domain name.|
|[DeleteEmailVerification](/intl.en-US/API Reference (New)/Domain management/DeleteEmailVerification.md)|Deletes verified email addresses.|
|[VerifyEmail](/intl.en-US/API Reference (New)/Domain management/VerifyEmail.md)|Verifies email addresses.|
|[ListEmailVerification](/intl.en-US/API Reference (New)/Domain management/ListEmailVerification.md)|Queries the verified email addresses.|
|[ResendEmailVerification](/intl.en-US/API Reference (New)/Domain management/ResendEmailVerification.md)|Resends a verification email.|
|[SubmitEmailVerification](/intl.en-US/API Reference (New)/Domain management/SubmitEmailVerification.md)|Submits an email verification task.|
|[QueryEmailVerification](/intl.en-US/API Reference (New)/Domain management/QueryEmailVerification.md)|Queries whether an email address is verified.|
|[SaveSingleTaskForCreatingOrderActivate](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderActivate.md)|Submits a task for registering a domain name.|
|[SaveSingleTaskForCreatingOrderRenew](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderRenew.md)|Submits a task for renewing a domain name.|
|[SaveBatchTaskForModifyingDomainDns](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForModifyingDomainDns.md)|Submits a task for changing the DNS servers of multiple domain names.|
|[SaveBatchTaskForUpdatingContactInfoByNewContact](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForUpdatingContactInfoByNewContact.md)|Submits a task for updating the domain name information of multiple domain names based on the information of the new registrant.|
|[SaveBatchTaskForCreatingOrderActivate](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderActivate.md)|Submits a task for registering multiple domain names.|
|[SaveBatchTaskForCreatingOrderRenew](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderRenew.md)|Submits a task for renewing multiple domain names.|
|[SaveBatchTaskForUpdateProhibitionLock](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForUpdateProhibitionLock.md)|Submits a task for enabling the update prohibition lock for multiple domain names.|
|[SaveBatchTaskForTransferProhibitionLock](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForTransferProhibitionLock.md)|Submits a task for enabling the transfer prohibition lock for multiple domain names.|
|[QueryTaskList](/intl.en-US/API Reference (New)/Domain management/QueryTaskList.md)|Queries domain name-related tasks.|
|[QueryTaskInfoHistory](/intl.en-US/API Reference (New)/Domain management/QueryTaskInfoHistory.md)|Queries historical domain name-related tasks.|
|[QueryTaskDetailList](/intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md)|Queries details about domain name-related tasks.|
|[QueryTaskDetailHistory](/intl.en-US/API Reference (New)/Domain management/QueryTaskDetailHistory.md)|Queries details about historical domain name-related tasks.|
|[CheckDomain](/intl.en-US/API Reference (New)/Domain management/CheckDomain.md)|Checks whether a domain name can be registered.|
|[AcknowledgeTaskResult](/intl.en-US/API Reference (New)/Domain management/AcknowledgeTaskResult.md)|Acknowledges task details.|
|[CheckTransferInFeasibility](/intl.en-US/API Reference (New)/Domain management/CheckTransferInFeasibility.md)|Checks whether a domain name can be transferred to Alibaba Cloud.|
|[PollTaskResult](/intl.en-US/API Reference (New)/Domain management/PollTaskResult.md)|Queries details about executed tasks.|
|[QueryTransferInByInstanceId](/intl.en-US/API Reference (New)/Domain management/QueryTransferInByInstanceId.md)|Queries domain name transfer-in information by instance ID.|
|[QueryTransferInList](/intl.en-US/API Reference (New)/Domain management/QueryTransferInList.md)|Queries domain name transfer-in information.|
|[QueryTransferOutInfo](/intl.en-US/API Reference (New)/Domain management/QueryTransferOutInfo.md)|Queries domain name transfer-out information.|
|[SaveSingleTaskForCancelingTransferIn](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferIn.md)|Submits a task for canceling the transfer-in request of a domain name.|
|[SaveSingleTaskForCancelingTransferOut](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferOut.md)|Submits a task for canceling the transfer-out request of a domain name.|
|[SaveSingleTaskForQueryingTransferAuthorizationCode](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForQueryingTransferAuthorizationCode.md)|Submits a task for querying the domain name transfer key.|
|[TransferInCheckMailToken](/intl.en-US/API Reference (New)/Domain management/TransferInCheckMailToken.md)|Verifies the token sent to the email address of the domain name registrant.|
|[TransferInReenterTransferAuthorizationCode](/intl.en-US/API Reference (New)/Domain management/TransferInReenterTransferAuthorizationCode.md)|Re-enters the transfer key to transfer a domain name to Alibaba Cloud.|
|[TransferInRefetchWhoisEmail](/intl.en-US/API Reference (New)/Domain management/TransferInRefetchWhoisEmail.md)|Captures the email address of the registrant of a domain name from WHOIS to transfer the domain name to Alibaba Cloud.|
|[TransferInResendMailToken](/intl.en-US/API Reference (New)/Domain management/TransferInResendMailToken.md)|Resends a verification email to transfer a domain name to Alibaba Cloud.|
|[VerifyContactField](/intl.en-US/API Reference (New)/Domain management/VerifyContactField.md)|Verifies the contact information of a domain name.|
|[SaveSingleTaskForCreatingOrderRedeem](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderRedeem.md)|Submits a task for redeeming a domain name.|
|[SaveBatchTaskForCreatingOrderRedeem](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderRedeem.md)|Submits a task for redeeming multiple domain names.|
|[SaveSingleTaskForCreatingDnsHost](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingDnsHost.md)|Submits a task for creating a DNS host.|
|[SaveSingleTaskForModifyingDnsHost](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForModifyingDnsHost.md)|Submits a task for changing a DNS host.|
|[SaveSingleTaskForSynchronizingDnsHost](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForSynchronizingDnsHost.md)|Submits a task for synchronizing DNS host information.|
|[SaveSingleTaskForTransferProhibitionLock](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForTransferProhibitionLock.md)|Submits a task for enabling the transfer prohibition lock for a domain name.|
|[SaveSingleTaskForUpdateProhibitionLock](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdateProhibitionLock.md)|Submits a task for enabling the update prohibition lock for a domain name.|
|[SaveSingleTaskForUpdatingContactInfo](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdatingContactInfo.md)|Submits a task for updating the domain name information.|
|[QueryDnsHost](/intl.en-US/API Reference (New)/Domain management/QueryDnsHost.md)|Queries the DNS host of a domain name.|
|[SaveSingleTaskForAddingDSRecord](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForAddingDSRecord.md)|Submits a task for creating the delegation signer \(DS\) record of a domain name.|
|[SaveSingleTaskForModifyingDSRecord](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForModifyingDSRecord.md)|Submits a task for modifying the DS record of a domain name.|
|[SaveSingleTaskForDeletingDSRecord](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForDeletingDSRecord.md)|Submits a task for deleting the DS record of a domain name.|
|[SaveSingleTaskForSynchronizingDSRecord](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForSynchronizingDSRecord.md)|Submits a task for synchronizing the DS record of a domain name.|
|[SaveSingleTaskForAssociatingEns](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForAssociatingEns.md)|Submits a task for associating an Ethereum Name Service \(ENS\) address with a domain name.|
|[QueryEnsAssociation](/intl.en-US/API Reference (New)/Domain management/QueryEnsAssociation.md)|Queries the wallet addresses associated with an ENS domain name.|
|[QueryDSRecord](/intl.en-US/API Reference (New)/Domain management/QueryDSRecord.md)|Queries the DS records of a domain name.|
|[QueryDomainByDomainName](/intl.en-US/API Reference (New)/Domain management/QueryDomainByDomainName.md)|Queries information of a specific domain name.|
|[SaveSingleTaskForDisassociatingEns](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForDisassociatingEns.md)|Submits a task for disassociating an Ethereum wallet address from a domain name.|
|[QueryLocalEnsAssociation](/intl.en-US/API Reference (New)/Domain management/QueryLocalEnsAssociation.md)|Queries the Ethereum wallet addresses associated with domain names in Alibaba Cloud.|
|[SaveSingleTaskForSaveArtExtension](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForSaveArtExtension.md)|Submits a task for configuring the extension information of a .art domain name.|
|[QueryArtExtension](/intl.en-US/API Reference (New)/Domain management/QueryArtExtension.md)|Queries the extension information of a .art domain name.|
|[CancelTask](/intl.en-US/API Reference (New)/Domain management/CancelTask.md)|Cancels a running task.|
|[SaveSingleTaskForDeletingDnsHost](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForDeletingDnsHost.md)|Submits a task for deleting a DNS host.|

## Manage registrant profiles

|Operation|Description|
|:--------|:----------|
|[SaveRegistrantProfile](/intl.en-US/API Reference (New)/Information template/SaveRegistrantProfile.md)|Creates or saves a registrant profile.|
|[QueryRegistrantProfiles](/intl.en-US/API Reference (New)/Information template/QueryRegistrantProfiles.md)|Queries the registrant profiles under your account.|
|[DeleteRegistrantProfile](/intl.en-US/API Reference (New)/Information template/DeleteRegistrantProfile.md)|Deletes a specified registrant profile.|

