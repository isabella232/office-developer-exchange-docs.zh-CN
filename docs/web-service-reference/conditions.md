---
title: 条件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Conditions
api_type:
- schema
ms.assetid: f049a48c-9585-43f7-8549-0b8cb19a5eea
description: Conditions 元素标识满足时将触发规则的规则操作的条件。
ms.openlocfilehash: 55e569c2aa393c79eb4e712711fb2e7b4107023b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515976"
---
# <a name="conditions"></a>条件

**Conditions** 元素标识满足时将触发规则的规则操作的条件。 
  
```XML
<Conditions>
   <Categories/>
   <ContainsBodyStrings/>
   <ContainsHeaderStrings/>
   <ContainsRecipientStrings/>
   <ContainsSenderStrings/>
   <ContainsSubjectOrBodyStrings/>
   <ContainsSubjectStrings/>
   <FlaggedForAction/>
   <FromAddresses/>
   <FromConnectedAccounts/>
   <HasAttachments/>
   <Importance/>
   <IsApprovalRequest/>
   <IsAutomaticForward/>
   <IsAutomaticReply/>
   <IsEncrypted/>
   <IsMeetingRequest/>
   <IsMeetingResponse/>
   <IsNDR/>
   <IsPermissionControlled/>
   <IsReadReceipt/>
   <IsSigned/>
   <IsVoicemail/>
   <ItemClasses/>
   <MessageClassifications/>
   <NotSentToMe/>
   <SentCcMe/>
   <SentOnlyToMe/>
   <SentToAddresses/>
   <SentToMe/>
   <SentToOrCcMe/>
   <Sensitivity/>
   <WithinDateRange/>
   <WithinSizeRange/>
</Conditions>
```

 **RulePredicatesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |包含必须应用于传入邮件的类别，以便条件或例外情况适用。  <br/> |
|[ContainsBodyStrings](containsbodystrings.md) <br/> |指示必须出现在传入邮件正文中的字符串，以便条件或例外情况适用。  <br/> |
|[ContainsHeaderStrings](containsheaderstrings.md) <br/> |指示必须出现在传入邮件头中的字符串，以便条件或例外情况适用。  <br/> |
|[ContainsRecipientStrings](containsrecipientstrings.md) <br/> |指示必须出现在传入邮件的 **ToRecipients** 或 **CcRecipients** 属性中的字符串，以便条件或例外情况适用。  <br/> |
|[ContainsSenderStrings](containssenderstrings.md) <br/> |指示必须出现在传入邮件的 **From** 属性中的字符串，以便条件或例外情况适用。  <br/> |
|[ContainsSubjectOrBodyStrings](containssubjectorbodystrings.md) <br/> |指示必须出现在传入邮件正文或主题中的字符串，以便条件或例外情况适用。  <br/> |
|[ContainsSubjectStrings](containssubjectstrings.md) <br/> |指示必须出现在传入邮件主题中的字符串，以便条件或例外情况适用。  <br/> |
|[FlaggedForAction](flaggedforaction.md) <br/> |指定操作值的标志，操作值必须出现在传入邮件上，以便条件或例外适用。  <br/> |
|[FromAddresses](fromaddresses.md) <br/> |指示必须发送传入邮件的电子邮件地址，以便条件或例外情况适用。  <br/> |
|[FromConnectedAccounts](fromconnectedaccounts.md) <br/> |表示必须聚合传入邮件才能应用条件或例外的电子邮件帐户名称。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |指示传入邮件是否必须包含附件，以便条件或例外情况适用。  <br/> |
|[Importance](importance.md) <br/> |指定在传入邮件上标记的重要性，以便条件或例外适用。  <br/> |
|[IsApprovalRequest](isapprovalrequest.md) <br/> |指示传入的邮件是否必须是审批请求，以便条件或例外情况适用。  <br/> |
|[IsAutomaticForward](isautomaticforward.md) <br/> |指示传入的邮件是否必须自动转发，以便条件或例外情况适用。  <br/> |
|[IsAutomaticReply](isautomaticreply.md) <br/> |指示传入的邮件是否必须为自动答复，以便条件或例外情况适用。  <br/> |
|[IsEncrypted](isencrypted.md) <br/> |指示传入的邮件是否必须经过 S/MIME 加密才能应用条件或例外。  <br/> |
|[IsMeetingRequest](ismeetingrequest.md) <br/> |指示传入的邮件是否必须为会议请求，以便条件或例外情况适用。  <br/> |
|[IsMeetingResponse](ismeetingresponse.md) <br/> |指示传入的邮件是否必须为会议响应，以便条件或例外情况适用。  <br/> |
|[IsNDR](isndr.md) <br/> |指示传入的邮件是否必须为未送达 (，) 报告，以便条件或例外情况适用。  <br/> |
|[IsPermissionControlled](ispermissioncontrolled.md) <br/> |指示传入邮件是否必须受受 RMS (控制) ，以便条件或例外情况适用。  <br/> |
|[IsReadReceipt](isreadreceipt.md) <br/> |指示传入的邮件是否必须已读回执，以便条件或例外情况适用。  <br/> |
|[IsSigned](issigned.md) <br/> |指示传入的邮件是否必须进行 S/MIME 签名，以便条件或例外情况适用。  <br/> |
|[IsVoicemail](isvoicemail.md) <br/> |指示传入的邮件是否必须为语音邮件，以便条件或例外情况适用。  <br/> |
|[ItemClasses](itemclasses.md) <br/> |表示必须标记在传入邮件上才能应用条件或例外的项目类。  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |表示必须在传入邮件上标记的邮件分类，以便条件或例外情况适用。  <br/> |
|[NotSentToMe](notsenttome.md) <br/> |指示邮箱所有者是否不得在传入邮件的 **ToRecipients** 属性中，以便条件或例外情况适用。  <br/> |
|[SentCcMe](sentccme.md) <br/> |指示邮箱所有者是否必须拥有传入邮件的 **CcRecipients** 属性才能应用条件或例外。  <br/> |
|[SentOnlyToMe](sentonlytome.md) <br/> |指示邮箱所有者是否必须是唯一一个传入邮件的 **ToRecipients** 属性中的唯一所有者，以便条件或例外情况适用。  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |指示传入邮件必须发送到的电子邮件地址，以便条件或例外情况适用。  <br/> |
|[SentToMe](senttome.md) <br/> |指示邮箱所有者是否必须拥有传入邮件的 **ToRecipients** 属性，以便条件或例外情况适用。  <br/> |
|[SentToOrCcMe](senttoorccme.md) <br/> |指示邮箱所有者是否必须拥有传入邮件的 **ToRecipients** 或 **CcRecipients** 属性，以便条件或例外情况适用。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示必须在传入邮件上标记的敏感度，以便条件或例外情况适用。  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |指定必须接收传入邮件的日期范围，以便条件或例外情况适用。  <br/> |
|[WithinSizeRange](withinsizerange.md) <br/> |指定传入邮件必须达到的最小和最大大小，以便条件或例外适用。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[规则 (RuleType)](rule-ruletype.md) <br/> |包含单个规则，表示用户邮箱中的规则。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[异常](exceptions.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

