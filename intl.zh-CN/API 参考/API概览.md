# API概览

支持域名购买、续费以及管理操作（包括信息修改、DNS修改、创建DNS、信息模板的管理等），以及域名列表和域名信息的查询。

## 域名管理接口

|API|描述|
|:--|:-|
|[QueryDomainList](/intl.zh-CN/API 参考/域名管理接口/QueryDomainList.md)|查询自己账号下域名列表|
|[QueryDomainByInstanceId](/intl.zh-CN/API 参考/域名管理接口/QueryDomainByInstanceId.md)|查询自己账号下域名信息|
|[QueryContactInfo](/intl.zh-CN/API 参考/域名管理接口/QueryContactInfo.md)|查询域名联系人信息|
|[QueryChangeLogList](/intl.zh-CN/API 参考/域名管理接口/QueryChangeLogList.md)|查询操作日志|
|[DeleteEmailVerification](/intl.zh-CN/API 参考/域名管理接口/DeleteEmailVerification.md)|删除已验证通过的邮箱|
|[VerifyEmail](/intl.zh-CN/API 参考/域名管理接口/VerifyEmail.md)|验证邮箱|
|[ListEmailVerification](/intl.zh-CN/API 参考/域名管理接口/ListEmailVerification.md)|查询邮箱验证列表|
|[ResendEmailVerification](/intl.zh-CN/API 参考/域名管理接口/ResendEmailVerification.md)|重新发送验证邮件|
|[SubmitEmailVerification](/intl.zh-CN/API 参考/域名管理接口/SubmitEmailVerification.md)|发送邮箱验证列表|
|[QueryEmailVerification](/intl.zh-CN/API 参考/域名管理接口/QueryEmailVerification.md)|查询邮箱验证结果|
|[SaveSingleTaskForCreatingOrderActivate](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCreatingOrderActivate.md)|提交域名注册任务|
|[SaveSingleTaskForCreatingOrderRenew](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCreatingOrderRenew.md)|提交域名续费任务|
|[SaveBatchTaskForModifyingDomainDns](/intl.zh-CN/API 参考/域名管理接口/SaveBatchTaskForModifyingDomainDns.md)|提交批量修改域名Dns任务|
|[SaveBatchTaskForUpdatingContactInfoByNewContact](/intl.zh-CN/API 参考/域名管理接口/SaveBatchTaskForUpdatingContactInfoByNewContact.md)|提交通过新联系人信息域名信息修改任务|
|[SaveBatchTaskForCreatingOrderActivate](/intl.zh-CN/API 参考/域名管理接口/SaveBatchTaskForCreatingOrderActivate.md)|提交批量域名注册任务|
|[SaveBatchTaskForCreatingOrderRenew](/intl.zh-CN/API 参考/域名管理接口/SaveBatchTaskForCreatingOrderRenew.md)|提交批量域名续费任务|
|[SaveBatchTaskForUpdateProhibitionLock](/intl.zh-CN/API 参考/域名管理接口/SaveBatchTaskForUpdateProhibitionLock.md)|提交批量禁止更新锁任务|
|[SaveBatchTaskForTransferProhibitionLock](/intl.zh-CN/API 参考/域名管理接口/SaveBatchTaskForTransferProhibitionLock.md)|提交批量禁止转移锁任务|
|[QueryTaskList](/intl.zh-CN/API 参考/域名管理接口/QueryTaskList.md)|查询域名任务列表|
|[QueryTaskInfoHistory](/intl.zh-CN/API 参考/域名管理接口/QueryTaskInfoHistory.md)|查询域名任务历史列表|
|[QueryTaskDetailList](/intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailList.md)|查询域名任务的详情列表|
|[QueryTaskDetailHistory](/intl.zh-CN/API 参考/域名管理接口/QueryTaskDetailHistory.md)|查询域名任务的详情历史列表|
|[CheckDomain](/intl.zh-CN/API 参考/域名管理接口/CheckDomain.md)|检查域名是否可以注册接口|
|[AcknowledgeTaskResult](/intl.zh-CN/API 参考/域名管理接口/AcknowledgeTaskResult.md)|确认任务详情结果|
|[CheckTransferInFeasibility](/intl.zh-CN/API 参考/域名管理接口/CheckTransferInFeasibility.md)|校验域名是否可以转入|
|[PollTaskResult](/intl.zh-CN/API 参考/域名管理接口/PollTaskResult.md)|获取已经执行完成的任务详情列表|
|[QueryTransferInByInstanceId](/intl.zh-CN/API 参考/域名管理接口/QueryTransferInByInstanceId.md)|根据实例编号查询域名转入信息|
|[QueryTransferInList](/intl.zh-CN/API 参考/域名管理接口/QueryTransferInList.md)|查询域名转入列表|
|[QueryTransferOutInfo](/intl.zh-CN/API 参考/域名管理接口/QueryTransferOutInfo.md)|查询域名转出信息|
|[SaveSingleTaskForCancelingTransferIn](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCancelingTransferIn.md)|提交取消域名转入任务|
|[SaveSingleTaskForCancelingTransferOut](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCancelingTransferOut.md)|提交取消域名转出任务|
|[SaveSingleTaskForQueryingTransferAuthorizationCode](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForQueryingTransferAuthorizationCode.md)|提交获取域名转移密码任务|
|[TransferInCheckMailToken](/intl.zh-CN/API 参考/域名管理接口/TransferInCheckMailToken.md)|域名转入验证邮件|
|[TransferInReenterTransferAuthorizationCode](/intl.zh-CN/API 参考/域名管理接口/TransferInReenterTransferAuthorizationCode.md)|域名转入重新输入转移密码|
|[TransferInRefetchWhoisEmail](/intl.zh-CN/API 参考/域名管理接口/TransferInRefetchWhoisEmail.md)|域名转入重新抓取whois邮箱|
|[TransferInResendMailToken](/intl.zh-CN/API 参考/域名管理接口/TransferInResendMailToken.md)|域名转入重新发送验证邮件|
|[VerifyContactField](/intl.zh-CN/API 参考/域名管理接口/VerifyContactField.md)|校验联系人信息|
|[SaveSingleTaskForCreatingOrderRedeem](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCreatingOrderRedeem.md)|提交域名赎回任务|
|[SaveBatchTaskForCreatingOrderRedeem](/intl.zh-CN/API 参考/域名管理接口/SaveBatchTaskForCreatingOrderRedeem.md)|提交批量域名赎回任务|
|[SaveSingleTaskForCreatingDnsHost](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForCreatingDnsHost.md)|提交创建DnsHost任务|
|[SaveSingleTaskForModifyingDnsHost](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForModifyingDnsHost.md)|提交修改DnsHost任务|
|[SaveSingleTaskForSynchronizingDnsHost](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForSynchronizingDnsHost.md)|提交同步DnsHost任务|
|[SaveSingleTaskForTransferProhibitionLock](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForTransferProhibitionLock.md)|提交禁止转移锁任务|
|[SaveSingleTaskForUpdateProhibitionLock](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForUpdateProhibitionLock.md)|提交禁止更新锁任务|
|[SaveSingleTaskForUpdatingContactInfo](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForUpdatingContactInfo.md)|提交域名信息修改任务|
|[QueryDnsHost](/intl.zh-CN/API 参考/域名管理接口/QueryDnsHost.md)|查询域名DnsHost|
|[SaveSingleTaskForAddingDSRecord](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForAddingDSRecord.md)|提交创建DS记录任务|
|[SaveSingleTaskForModifyingDSRecord](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForModifyingDSRecord.md)|提交修改DS记录任务|
|[SaveSingleTaskForDeletingDSRecord](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForDeletingDSRecord.md)|提交删除DS记录任务|
|[SaveSingleTaskForSynchronizingDSRecord](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForSynchronizingDSRecord.md)|提交同步DS记录任务|
|[SaveSingleTaskForAssociatingEns](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForAssociatingEns.md)|提交绑定Ens地址任务|
|[QueryEnsAssociation](/intl.zh-CN/API 参考/域名管理接口/QueryEnsAssociation.md)|查询Ens系统中绑定的地址|
|[QueryDSRecord](/intl.zh-CN/API 参考/域名管理接口/QueryDSRecord.md)|查询域名DS记录|
|[QueryDomainByDomainName](/intl.zh-CN/API 参考/域名管理接口/QueryDomainByDomainName.md)|按域名查询域名信息|
|[SaveSingleTaskForDisassociatingEns](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForDisassociatingEns.md)|提交解绑Ens地址任务|
|[QueryLocalEnsAssociation](/intl.zh-CN/API 参考/域名管理接口/QueryLocalEnsAssociation.md)|查询阿里云系统中记录的ens绑定地址|
|[SaveSingleTaskForSaveArtExtension](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForSaveArtExtension.md)|提交创建Art扩展信息任务|
|[QueryArtExtension](/intl.zh-CN/API 参考/域名管理接口/QueryArtExtension.md)|查询Art扩展信息|
|[CancelTask](/intl.zh-CN/API 参考/域名管理接口/CancelTask.md)|取消进行中的任务|
|[SaveSingleTaskForDeletingDnsHost](/intl.zh-CN/API 参考/域名管理接口/SaveSingleTaskForDeletingDnsHost.md)|提交删除DnsHost任务|

## 信息模板接口

|API|描述|
|:--|:-|
|[SaveRegistrantProfile](/intl.zh-CN/API 参考/信息模板接口/SaveRegistrantProfile.md)|创建或者保存域名信息模板|
|[QueryRegistrantProfiles](/intl.zh-CN/API 参考/信息模板接口/QueryRegistrantProfiles.md)|查询自己账号下的域名信息模板|
|[DeleteRegistrantProfile](/intl.zh-CN/API 参考/信息模板接口/DeleteRegistrantProfile.md)|删除指定的域名信息模板|
|[SetDefaultRegistrantProfile](/intl.zh-CN/API 参考/信息模板接口/SetDefaultRegistrantProfile.md)|设置域名联系人默认模板|
|[DeleteContactTemplates](/intl.zh-CN/API 参考/信息模板接口/DeleteContactTemplates.md)|批量删除域名联系人模板|

