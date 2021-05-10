# API概览

支持域名购买、续费以及管理操作（包括信息修改、DNS修改、创建DNS、信息模板的管理等），以及域名列表和域名信息的查询。

## 域名管理接口

|API|描述|
|:--|:-|
|[QueryDomainList](/cn.zh-CN/API 参考/域名管理接口/QueryDomainList.md)|查询自己账号下域名列表|
|[QueryDomainByInstanceId](/cn.zh-CN/API 参考/域名管理接口/QueryDomainByInstanceId.md)|查询自己账号下域名信息|
|[QueryContactInfo](/cn.zh-CN/API 参考/域名管理接口/QueryContactInfo.md)|查询域名联系人信息|
|[QueryChangeLogList](/cn.zh-CN/API 参考/域名管理接口/QueryChangeLogList.md)|查询操作日志|
|[DeleteEmailVerification](/cn.zh-CN/API 参考/域名管理接口/DeleteEmailVerification.md)|删除已验证通过的邮箱|
|[VerifyEmail](/cn.zh-CN/API 参考/域名管理接口/VerifyEmail.md)|验证邮箱|
|[ListEmailVerification](/cn.zh-CN/API 参考/域名管理接口/ListEmailVerification.md)|查询邮箱验证列表|
|[ResendEmailVerification](/cn.zh-CN/API 参考/域名管理接口/ResendEmailVerification.md)|重新发送验证邮件|
|[SubmitEmailVerification](/cn.zh-CN/API 参考/域名管理接口/SubmitEmailVerification.md)|发送邮箱验证列表|
|[QueryEmailVerification](/cn.zh-CN/API 参考/域名管理接口/QueryEmailVerification.md)|查询邮箱验证结果|
|[SaveSingleTaskForCreatingOrderActivate](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCreatingOrderActivate.md)|提交域名注册任务|
|[SaveSingleTaskForCreatingOrderRenew](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCreatingOrderRenew.md)|提交域名续费任务|
|[SaveBatchTaskForModifyingDomainDns](/cn.zh-CN/API 参考/域名管理接口/SaveBatchTaskForModifyingDomainDns.md)|提交批量修改域名Dns任务|
|[SaveBatchTaskForUpdatingContactInfoByNewContact](/cn.zh-CN/API 参考/域名管理接口/SaveBatchTaskForUpdatingContactInfoByNewContact.md)|提交通过新联系人信息域名信息修改任务|
|[SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId](/cn.zh-CN/API 参考/域名管理接口/SaveBatchTaskForUpdatingContactInfoByRegistrantProfileId.md)|提交批量通过模板域名信息修改任务|
|[SaveBatchTaskForCreatingOrderActivate](/cn.zh-CN/API 参考/域名管理接口/SaveBatchTaskForCreatingOrderActivate.md)|提交批量域名注册任务|
|[SaveBatchTaskForCreatingOrderRenew](/cn.zh-CN/API 参考/域名管理接口/SaveBatchTaskForCreatingOrderRenew.md)|提交批量域名续费任务|
|[SaveBatchTaskForUpdateProhibitionLock](/cn.zh-CN/API 参考/域名管理接口/SaveBatchTaskForUpdateProhibitionLock.md)|提交批量禁止更新锁任务|
|[SaveBatchTaskForTransferProhibitionLock](/cn.zh-CN/API 参考/域名管理接口/SaveBatchTaskForTransferProhibitionLock.md)|提交批量禁止转移锁任务|
|[QueryTaskList](/cn.zh-CN/API 参考/域名管理接口/QueryTaskList.md)|查询域名任务列表|
|[QueryTaskInfoHistory](/cn.zh-CN/API 参考/域名管理接口/QueryTaskInfoHistory.md)|查询域名任务历史列表|
|[QueryTaskDetailList](/cn.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md)|查询域名任务的详情列表|
|[QueryTaskDetailHistory](/cn.zh-CN/API 参考/域名管理接口/QueryTaskDetailHistory.md)|查询域名任务的详情历史列表|
|[SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileID](/cn.zh-CN/API 参考/域名管理接口/SaveTaskForSubmittingDomainRealNameVerificationByRegistrantProfileID.md)|通过信息模板ID提交域名实名认证任务|
|[SaveTaskForSubmittingDomainRealNameVerificationByIdentityCredential](/cn.zh-CN/API 参考/域名管理接口/SaveTaskForSubmittingDomainRealNameVerificationByIdentityCredential.md)|提交域名实名认证任务|
|[SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID](/cn.zh-CN/API 参考/域名管理接口/SaveTaskForUpdatingRegistrantInfoByRegistrantProfileID.md)|提交通过信息模板ID修改注册联系人信息任务|
|[SaveTaskForUpdatingRegistrantInfoByIdentityCredential](/cn.zh-CN/API 参考/域名管理接口/SaveTaskForUpdatingRegistrantInfoByIdentityCredential.md)|提交批量通过联系人信息和资料修改注册联系人信息任务|
|[QueryFailReasonForDomainRealNameVerification](/cn.zh-CN/API 参考/域名管理接口/QueryFailReasonForDomainRealNameVerification.md)|查询域名实名认证失败原因|
|[CheckDomain](/cn.zh-CN/API 参考/域名管理接口/CheckDomain.md)|检查域名是否可以注册接口|
|[FuzzyMatchDomainSensitiveWord](/cn.zh-CN/API 参考/域名管理接口/FuzzyMatchDomainSensitiveWord.md)|检查是否包含敏感词|
|[BatchFuzzyMatchDomainSensitiveWord](/cn.zh-CN/API 参考/域名管理接口/BatchFuzzyMatchDomainSensitiveWord.md)|批量检查是否包含敏感词|
|[CheckDomainSunriseClaim](/cn.zh-CN/API 参考/域名管理接口/CheckDomainSunriseClaim.md)|查询商标词key|
|[LookupTmchNotice](/cn.zh-CN/API 参考/域名管理接口/LookupTmchNotice.md)|查询tmch信息|
|[AcknowledgeTaskResult](/cn.zh-CN/API 参考/域名管理接口/AcknowledgeTaskResult.md)|确认任务详情结果|
|[CheckTransferInFeasibility](/cn.zh-CN/API 参考/域名管理接口/CheckTransferInFeasibility.md)|校验域名是否可以转入|
|[PollTaskResult](/cn.zh-CN/API 参考/域名管理接口/PollTaskResult.md)|获取已经执行完成的任务详情列表|
|[QueryDomainGroupList](/cn.zh-CN/API 参考/域名管理接口/QueryDomainGroupList.md)|查询域名分组列表|
|[QueryTransferInByInstanceId](/cn.zh-CN/API 参考/域名管理接口/QueryTransferInByInstanceId.md)|根据实例编号查询域名转入信息|
|[QueryTransferInList](/cn.zh-CN/API 参考/域名管理接口/QueryTransferInList.md)|查询域名转入列表|
|[QueryTransferOutInfo](/cn.zh-CN/API 参考/域名管理接口/QueryTransferOutInfo.md)|查询域名转出信息|
|[QueryDomainAdminDivision](/cn.zh-CN/API 参考/域名管理接口/QueryDomainAdminDivision.md)|查询中国行政区划|
|[SaveBatchTaskForCreatingOrderTransfer](/cn.zh-CN/API 参考/域名管理接口/SaveBatchTaskForCreatingOrderTransfer.md)|提交批量域名转入任务|
|[SaveSingleTaskForCreatingOrderTransfer](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCreatingOrderTransfer.md)|提交域名转入任务|
|[SaveSingleTaskForCancelingTransferIn](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCancelingTransferIn.md)|提交取消域名转入任务|
|[SaveSingleTaskForCancelingTransferOut](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCancelingTransferOut.md)|提交取消域名转出任务|
|[SaveSingleTaskForQueryingTransferAuthorizationCode](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForQueryingTransferAuthorizationCode.md)|提交获取域名转移密码任务|
|[TransferInCheckMailToken](/cn.zh-CN/API 参考/域名管理接口/TransferInCheckMailToken.md)|域名转入验证邮件|
|[TransferInReenterTransferAuthorizationCode](/cn.zh-CN/API 参考/域名管理接口/TransferInReenterTransferAuthorizationCode.md)|域名转入重新输入转移密码|
|[TransferInRefetchWhoisEmail](/cn.zh-CN/API 参考/域名管理接口/TransferInRefetchWhoisEmail.md)|域名转入重新抓取whois邮箱|
|[TransferInResendMailToken](/cn.zh-CN/API 参考/域名管理接口/TransferInResendMailToken.md)|域名转入重新发送验证邮件|
|[VerifyContactField](/cn.zh-CN/API 参考/域名管理接口/VerifyContactField.md)|校验联系人信息|
|[SaveSingleTaskForCreatingOrderRedeem](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCreatingOrderRedeem.md)|提交域名赎回任务|
|[SaveBatchTaskForCreatingOrderRedeem](/cn.zh-CN/API 参考/域名管理接口/SaveBatchTaskForCreatingOrderRedeem.md)|提交批量域名赎回任务|
|[SaveSingleTaskForCreatingDnsHost](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCreatingDnsHost.md)|提交创建DnsHost任务|
|[SaveSingleTaskForModifyingDnsHost](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForModifyingDnsHost.md)|提交修改DnsHost任务|
|[SaveSingleTaskForSynchronizingDnsHost](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForSynchronizingDnsHost.md)|提交同步DnsHost任务|
|[SaveSingleTaskForTransferProhibitionLock](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForTransferProhibitionLock.md)|提交禁止转移锁任务|
|[SaveSingleTaskForUpdateProhibitionLock](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForUpdateProhibitionLock.md)|提交禁止更新锁任务|
|[SaveSingleTaskForUpdatingContactInfo](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForUpdatingContactInfo.md)|提交域名信息修改任务|
|[QueryDnsHost](/cn.zh-CN/API 参考/域名管理接口/QueryDnsHost.md)|查询域名DnsHost|
|[DeleteDomainGroup](/cn.zh-CN/API 参考/域名管理接口/DeleteDomainGroup.md)|删除域名分组|
|[SaveDomainGroup](/cn.zh-CN/API 参考/域名管理接口/SaveDomainGroup.md)|保存域名分组|
|[UpdateDomainToDomainGroup](/cn.zh-CN/API 参考/域名管理接口/UpdateDomainToDomainGroup.md)|向分组中设置域名|
|[SaveBatchDomainRemark](/cn.zh-CN/API 参考/域名管理接口/SaveBatchDomainRemark.md)|批量保存域名备注信息|
|[QueryDomainSuffix](/cn.zh-CN/API 参考/域名管理接口/QueryDomainSuffix.md)|高级搜索自己账号下后缀列表|
|[QueryAdvancedDomainList](/cn.zh-CN/API 参考/域名管理接口/QueryAdvancedDomainList.md)|高级搜索自己账号下域名列表|
|[SaveSingleTaskForAddingDSRecord](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForAddingDSRecord.md)|提交创建DS记录任务|
|[SaveSingleTaskForModifyingDSRecord](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForModifyingDSRecord.md)|提交修改DS记录任务|
|[SaveSingleTaskForDeletingDSRecord](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForDeletingDSRecord.md)|提交删除DS记录任务|
|[SaveSingleTaskForSynchronizingDSRecord](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForSynchronizingDSRecord.md)|提交同步DS记录任务|
|[SaveSingleTaskForAssociatingEns](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForAssociatingEns.md)|提交绑定Ens地址任务|
|[QueryEnsAssociation](/cn.zh-CN/API 参考/域名管理接口/QueryEnsAssociation.md)|查询Ens系统中绑定的地址|
|[QueryDSRecord](/cn.zh-CN/API 参考/域名管理接口/QueryDSRecord.md)|查询域名DS记录|
|[ScrollDomainList](/cn.zh-CN/API 参考/域名管理接口/ScrollDomainList.md)|翻页遍历域名列表|
|[QueryDomainByDomainName](/cn.zh-CN/API 参考/域名管理接口/QueryDomainByDomainName.md)|按域名查询域名信息|
|[SaveSingleTaskForDisassociatingEns](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForDisassociatingEns.md)|提交解绑Ens地址任务|
|[QueryLocalEnsAssociation](/cn.zh-CN/API 参考/域名管理接口/QueryLocalEnsAssociation.md)|查询阿里云系统中记录的ens绑定地址|
|[SaveSingleTaskForSaveArtExtension](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForSaveArtExtension.md)|提交创建Art扩展信息任务|
|[QueryArtExtension](/cn.zh-CN/API 参考/域名管理接口/QueryArtExtension.md)|查询Art扩展信息|
|[CancelDomainVerification](/cn.zh-CN/API 参考/域名管理接口/CancelDomainVerification.md)|取消域名实名认证审核|
|[CancelTask](/cn.zh-CN/API 参考/域名管理接口/CancelTask.md)|取消进行中的任务|
|[SaveSingleTaskForDeletingDnsHost](/cn.zh-CN/API 参考/域名管理接口/SaveSingleTaskForDeletingDnsHost.md)|提交删除DnsHost任务|
|[QueryDomainRealNameVerificationInfo](/cn.zh-CN/API 参考/域名管理接口/QueryDomainRealNameVerificationInfo.md)|查询域名实名认证资料|
|[SubmitOperationAuditInfo]()|提交自助业务审核信息|
|[SubmitOperationCredentials](/cn.zh-CN/API 参考/域名管理接口/SubmitOperationCredentials.md)|提交自助业务待审核的证件资料|
|[GetOperationOssUploadPolicy](/cn.zh-CN/API 参考/域名管理接口/GetOperationOssUploadPolicy.md)|获取审核资料的存储信息|
|[QueryOperationAuditInfoList](/cn.zh-CN/API 参考/域名管理接口/QueryOperationAuditInfoList.md)|查询自助业务的审核记录列表|
|[QueryOperationAuditInfoDetail](/cn.zh-CN/API 参考/域名管理接口/QueryOperationAuditInfoDetail.md)|查询自助业务的审核记录详情|
|[CancelOperationAudit](/cn.zh-CN/API 参考/域名管理接口/CancelOperationAudit.md)|取消自助业务审核|

## 信息模板接口

|API|描述|
|:--|:-|
|[SaveRegistrantProfile](/cn.zh-CN/API 参考/信息模板接口/SaveRegistrantProfile.md)|创建或者保存域名信息模板|
|[QueryRegistrantProfiles](/cn.zh-CN/API 参考/信息模板接口/QueryRegistrantProfiles.md)|查询自己账号下的域名信息模板|
|[DeleteRegistrantProfile](/cn.zh-CN/API 参考/信息模板接口/DeleteRegistrantProfile.md)|删除指定的域名信息模板|
|[RegistrantProfileRealNameVerification](/cn.zh-CN/API 参考/信息模板接口/RegistrantProfileRealNameVerification.md)|提交信息模板实名认证|
|[QueryFailReasonForRegistrantProfileRealNameVerification](/cn.zh-CN/API 参考/信息模板接口/QueryFailReasonForRegistrantProfileRealNameVerification.md)|查询模板实名认证失败原因|
|[QueryRegistrantProfileRealNameVerificationInfo](/cn.zh-CN/API 参考/信息模板接口/QueryRegistrantProfileRealNameVerificationInfo.md)|查询域名信息模板实名认证资料|
|[SetDefaultRegistrantProfile](/cn.zh-CN/API 参考/信息模板接口/SetDefaultRegistrantProfile.md)|设置域名联系人默认模板|
|[DeleteContactTemplates](/cn.zh-CN/API 参考/信息模板接口/DeleteContactTemplates.md)|批量删除域名联系人模板|

