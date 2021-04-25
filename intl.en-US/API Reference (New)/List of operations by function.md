# List of operations by function

The following tables list the API operations available for use in Alibaba Cloud Domains. You can call these operations to purchase, renew, and manage domain names, and query domain names and domain name information. You can also update domain name information, change Domain Name System \(DNS\) servers, create DNS servers, and manage registrant profiles.

## Manage domain names

|Operation|Description|
|:--------|:----------|
|[QueryDomainList](/intl.en-US/API Reference (New)/Domain management/QueryDomainList.md)|Queries the domain names within your account by page.|
|[QueryDomainByInstanceId](/intl.en-US/API Reference (New)/Domain management/QueryDomainByInstanceId.md)|Queries the basic information about a domain name based on the instance ID of the domain name.|
|[QueryContactInfo](/intl.en-US/API Reference (New)/Domain management/QueryContactInfo.md)|Queries the contact information of a domain name.|
|[QueryChangeLogList](/intl.en-US/API Reference (New)/Domain management/QueryChangeLogList.md)|Queries the operation logs of a domain name.|
|[DeleteEmailVerification](/intl.en-US/API Reference (New)/Domain management/DeleteEmailVerification.md)|Deletes one or more verified email addresses.|
|[VerifyEmail](/intl.en-US/API Reference (New)/Domain management/VerifyEmail.md)|Verifies the token that was received at the email address of a domain name.|
|[ListEmailVerification](/intl.en-US/API Reference (New)/Domain management/ListEmailVerification.md)|Queries verified and to-be-verified email addresses.|
|[ResendEmailVerification](/intl.en-US/API Reference (New)/Domain management/ResendEmailVerification.md)|Sends a new verification email to one or more email addresses.|
|[SubmitEmailVerification](/intl.en-US/API Reference (New)/Domain management/SubmitEmailVerification.md)|Sends a verification email to one or more email addresses.|
|[QueryEmailVerification](/intl.en-US/API Reference (New)/Domain management/QueryEmailVerification.md)|Queries whether an email address is verified.|
|[SaveSingleTaskForCreatingOrderActivate](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderActivate.md)|Submits a task to register a domain name.|
|[SaveSingleTaskForCreatingOrderRenew](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderRenew.md)|Submits a task to renew a domain name.|
|[SaveBatchTaskForModifyingDomainDns](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForModifyingDomainDns.md)|Submits a task to change the DNS servers of multiple domain names at a time.|
|[SaveBatchTaskForUpdatingContactInfoByNewContact](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForUpdatingContactInfoByNewContact.md)|Submits a task to update the domain name information of multiple domain names based on the information of the new registrant.|
|[SaveBatchTaskForCreatingOrderActivate](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderActivate.md)|Submits a task to register multiple domain names at a time.|
|[SaveBatchTaskForCreatingOrderRenew](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderRenew.md)|Submits a task to renew multiple domain names at a time.|
|[SaveBatchTaskForUpdateProhibitionLock](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForUpdateProhibitionLock.md)|Submits a task to enable the update prohibition lock for multiple domain names at a time.|
|[SaveBatchTaskForTransferProhibitionLock](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForTransferProhibitionLock.md)|Submits a task to enable the transfer prohibition lock for multiple domain names at a time.|
|[QueryTaskList](/intl.en-US/API Reference (New)/Domain management/QueryTaskList.md)|Queries the domain name tasks within your account by page.|
|[QueryTaskInfoHistory](/intl.en-US/API Reference (New)/Domain management/QueryTaskInfoHistory.md)|Queries the historical domain name tasks within your account by page.|
|[QueryTaskDetailList](/intl.en-US/API Reference (New)/Domain management/QueryTaskDetailList.md)|Queries the details of a specific domain name task by page.|
|[QueryTaskDetailHistory](/intl.en-US/API Reference (New)/Domain management/QueryTaskDetailHistory.md)|Queries the historical details of a domain name task by page.|
|[CheckDomain](/intl.en-US/API Reference (New)/Domain management/CheckDomain.md)|Queries whether a domain name can be registered.|
|[AcknowledgeTaskResult](/intl.en-US/API Reference (New)/Domain management/AcknowledgeTaskResult.md)|Confirms detailed task results.|
|[CheckTransferInFeasibility](/intl.en-US/API Reference (New)/Domain management/CheckTransferInFeasibility.md)|Checks whether a domain name can be transferred to Alibaba Cloud.|
|[PollTaskResult](/intl.en-US/API Reference (New)/Domain management/PollTaskResult.md)|Queries the details about completed domain name tasks.|
|[QueryTransferInByInstanceId](/intl.en-US/API Reference (New)/Domain management/QueryTransferInByInstanceId.md)|Queries domain name transfer-in information by instance ID.|
|[QueryTransferInList](/intl.en-US/API Reference (New)/Domain management/QueryTransferInList.md)|Queries the domain names that are transferred to Alibaba Cloud.|
|[QueryTransferOutInfo](/intl.en-US/API Reference (New)/Domain management/QueryTransferOutInfo.md)|Queries the transfer-out information of a domain name.|
|[SaveSingleTaskForCancelingTransferIn](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferIn.md)|Submits a task to cancel the transfer-in request of a domain name.|
|[SaveSingleTaskForCancelingTransferOut](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCancelingTransferOut.md)|Submits a task to cancel the transfer-out request of a domain name.|
|[SaveSingleTaskForQueryingTransferAuthorizationCode](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForQueryingTransferAuthorizationCode.md)|Submits a task to obtain a domain name transfer key.|
|[TransferInCheckMailToken](/intl.en-US/API Reference (New)/Domain management/TransferInCheckMailToken.md)|Verifies the token sent to the email address of the domain name registrant.|
|[TransferInReenterTransferAuthorizationCode](/intl.en-US/API Reference (New)/Domain management/TransferInReenterTransferAuthorizationCode.md)|Enters a transfer key again to transfer a domain name to Alibaba Cloud.|
|[TransferInRefetchWhoisEmail](/intl.en-US/API Reference (New)/Domain management/TransferInRefetchWhoisEmail.md)|Captures the email address of the registrant of a domain name from WHOIS to transfer the domain name to Alibaba Cloud.|
|[TransferInResendMailToken](/intl.en-US/API Reference (New)/Domain management/TransferInResendMailToken.md)|Resends a verification email to transfer a domain name to Alibaba Cloud.|
|[VerifyContactField](/intl.en-US/API Reference (New)/Domain management/VerifyContactField.md)|Verifies the information of a domain name contact.|
|[SaveSingleTaskForCreatingOrderRedeem](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingOrderRedeem.md)|Submits a task to redeem a domain name.|
|[SaveBatchTaskForCreatingOrderRedeem](/intl.en-US/API Reference (New)/Domain management/SaveBatchTaskForCreatingOrderRedeem.md)|Submits a task to redeem multiple domain names at a time.|
|[SaveSingleTaskForCreatingDnsHost](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForCreatingDnsHost.md)|Submits a task to create a DNS server.|
|[SaveSingleTaskForModifyingDnsHost](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForModifyingDnsHost.md)|Submits a task to modify a DNS server.|
|[SaveSingleTaskForSynchronizingDnsHost](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForSynchronizingDnsHost.md)|Submits a task to synchronize DNS server information.|
|[SaveSingleTaskForTransferProhibitionLock](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForTransferProhibitionLock.md)|Submits a task to enable the transfer prohibition lock for a domain name.|
|[SaveSingleTaskForUpdateProhibitionLock](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdateProhibitionLock.md)|Submits a task to enable the update prohibition lock for a domain name.|
|[SaveSingleTaskForUpdatingContactInfo](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForUpdatingContactInfo.md)|Submits a task to modify the information of a domain name.|
|[QueryDnsHost](/intl.en-US/API Reference (New)/Domain management/QueryDnsHost.md)|Queries the DNS server of a domain name.|
|[SaveSingleTaskForAddingDSRecord](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForAddingDSRecord.md)|Submits a task to create the delegation signer \(DS\) record of a domain name.|
|[SaveSingleTaskForModifyingDSRecord](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForModifyingDSRecord.md)|Submits a task to modify the DS record of a domain name.|
|[SaveSingleTaskForDeletingDSRecord](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForDeletingDSRecord.md)|Submits a task to delete the DS record of a domain name.|
|[SaveSingleTaskForSynchronizingDSRecord](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForSynchronizingDSRecord.md)|Submits a task to synchronize the DS record of a domain name.|
|[SaveSingleTaskForAssociatingEns](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForAssociatingEns.md)|Submits a task to associate an Ethereum wallet address with a domain name.|
|[QueryEnsAssociation](/intl.en-US/API Reference (New)/Domain management/QueryEnsAssociation.md)|Queries the wallet addresses associated with an Ethereum Name Service \(ENS\) domain name.|
|[QueryDSRecord](/intl.en-US/API Reference (New)/Domain management/QueryDSRecord.md)|Queries the DS records of a domain name.|
|[QueryDomainByDomainName](/intl.en-US/API Reference (New)/Domain management/QueryDomainByDomainName.md)|Queries the information of a specific domain name.|
|[SaveSingleTaskForDisassociatingEns](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForDisassociatingEns.md)|Submits a task to disassociate an Ethereum wallet address from a domain name.|
|[QueryLocalEnsAssociation](/intl.en-US/API Reference (New)/Domain management/QueryLocalEnsAssociation.md)|Queries the Ethereum wallet addresses associated with domain names in Alibaba Cloud.|
|[SaveSingleTaskForSaveArtExtension](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForSaveArtExtension.md)|Submits a task to configure the extension information of a .art domain name.|
|[QueryArtExtension](/intl.en-US/API Reference (New)/Domain management/QueryArtExtension.md)|Queries the extension information of a .art domain name.|
|[CancelTask](/intl.en-US/API Reference (New)/Domain management/CancelTask.md)|Cancels a running task.|
|[SaveSingleTaskForDeletingDnsHost](/intl.en-US/API Reference (New)/Domain management/SaveSingleTaskForDeletingDnsHost.md)|Submits a task to delete a DNS server.|

## Manage registrant profiles

|Operation|Description|
|:--------|:----------|
|[SaveRegistrantProfile](/intl.en-US/API Reference (New)/Information template/SaveRegistrantProfile.md)|Creates or updates a registrant profile.|
|[QueryRegistrantProfiles](/intl.en-US/API Reference (New)/Information template/QueryRegistrantProfiles.md)|Queries the registrant profiles within your Alibaba Cloud account.|
|[DeleteRegistrantProfile](/intl.en-US/API Reference (New)/Information template/DeleteRegistrantProfile.md)|Deletes a registrant profile.|
|[SetDefaultRegistrantProfile](/intl.en-US/API Reference (New)/Information template/SetDefaultRegistrantProfile.md)|Sets a registrant profile as the default profile.|
|[DeleteContactTemplates](/intl.en-US/API Reference (New)/Information template/DeleteContactTemplates.md)|Deletes multiple registrant profiles at a time.|

