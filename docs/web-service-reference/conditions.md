---
title: 条件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conditions
api_type:
- schema
ms.assetid: f049a48c-9585-43f7-8549-0b8cb19a5eea
description: Conditions 元素标识条件，履行时, 将触发规则的规则操作。
ms.openlocfilehash: f66777e82892122c4c7dac45bdef3c42f5c4a577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753476"
---
# <a name="conditions"></a>条件

**Conditions**元素标识条件，履行时, 将触发规则的规则操作。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |包含必须应用于的条件或例外应用的顺序中的传入邮件的类别。  <br/> |
|[ContainsBodyStrings](containsbodystrings.md) <br/> |指示必须显示在正文中的条件或例外应用的顺序的传入消息的字符串。  <br/> |
|[ContainsHeaderStrings](containsheaderstrings.md) <br/> |指示必须应用的条件或例外顺序中的传入消息头中显示的字符串。  <br/> |
|[ContainsRecipientStrings](containsrecipientstrings.md) <br/> |指示必须出现在**ToRecipients**或**CcRecipients**属性中的条件或例外应用的顺序的传入消息的字符串。  <br/> |
|[ContainsSenderStrings](containssenderstrings.md) <br/> |指示必须出现在**From**属性中的条件或例外应用的顺序的传入消息的字符串。  <br/> |
|[ContainsSubjectOrBodyStrings](containssubjectorbodystrings.md) <br/> |指示必须出现在正文或中的条件或例外应用的顺序的传入邮件的主题的字符串。  <br/> |
|[ContainsSubjectStrings](containssubjectstrings.md) <br/> |指示必须在主题中的条件或例外应用的顺序的传入消息中显示的字符串。  <br/> |
|[FlaggedForAction](flaggedforaction.md) <br/> |指定对传入邮件中的条件或例外的顺序应用操作值，必须在出现的标志。  <br/> |
|[FromAddresses](fromaddresses.md) <br/> |指示必须从其发送传入消息的条件或例外的顺序应用中的电子邮件地址。  <br/> |
|[FromConnectedAccounts](fromconnectedaccounts.md) <br/> |表示具有已聚合中的条件或例外的顺序应用传入消息的电子邮件帐户名。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |指示是否具有传入消息，使其具有附件中的条件或例外应用的顺序。  <br/> |
|[Importance](importance.md) <br/> |指定对传入邮件中的条件或例外应用的顺序标的重要性。  <br/> |
|[IsApprovalRequest](isapprovalrequest.md) <br/> |指示是否必须审批请求中的条件或例外的顺序应用传入消息。  <br/> |
|[IsAutomaticForward](isautomaticforward.md) <br/> |指示是否必须按条件或例外的顺序应用自动转发传入消息。  <br/> |
|[IsAutomaticReply](isautomaticreply.md) <br/> |指示是否必须按条件或例外的顺序应用的自动答复传入消息。  <br/> |
|[进行加密](isencrypted.md) <br/> |指示是否必须 S/MIME 加密的条件或例外的顺序应用传入消息。  <br/> |
|[IsMeetingRequest](ismeetingrequest.md) <br/> |指示是否必须传入消息会议请求中的条件或例外应用的顺序。  <br/> |
|[IsMeetingResponse](ismeetingresponse.md) <br/> |指示是否必须会议传入消息的条件或例外的顺序应用中的响应。  <br/> |
|[IsNDR](isndr.md) <br/> |指示的条件或例外应用的顺序中的传入邮件是否必须以未送达报告 (Ndr)。  <br/> |
|[IsPermissionControlled](ispermissioncontrolled.md) <br/> |指示传入邮件是否必须进行的条件或例外应用的顺序中控制权限 (受 RMS 保护)。  <br/> |
|[IsReadReceipt](isreadreceipt.md) <br/> |指示是否必须读取传入消息中的条件或例外应用的顺序的回执。  <br/> |
|[IsSigned](issigned.md) <br/> |指示传入邮件是否必须 S/MIME 签名中的条件或例外应用的顺序。  <br/> |
|[IsVoicemail](isvoicemail.md) <br/> |指示是否传入消息必须应用的条件或例外顺序中的语音邮件消息。  <br/> |
|[ItemClasses](itemclasses.md) <br/> |代表必须在应用的条件或例外顺序中的传入邮件标记的项类。  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |代表必须在应用的条件或例外顺序中的传入邮件标记邮件分类。  <br/> |
|[NotSentToMe](notsenttome.md) <br/> |指示是否中的条件或例外应用的顺序的传入消息的**ToRecipients**属性中不能邮箱的所有者。  <br/> |
|[SentCcMe](sentccme.md) <br/> |指示是否要应用的条件或例外顺序中的传入消息的**CcRecipients**属性中的邮箱的所有者。  <br/> |
|[SentOnlyToMe](sentonlytome.md) <br/> |指示是否邮箱所有者必须是唯一的条件或例外应用的顺序中的传入消息的**ToRecipients**属性中。  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |指示需要中的条件或例外的顺序应用发送给传入消息的电子邮件地址。  <br/> |
|[SentToMe](senttome.md) <br/> |指示是否要应用的条件或例外顺序中的传入消息的**ToRecipients**属性中的邮箱的所有者。  <br/> |
|[SentToOrCcMe](senttoorccme.md) <br/> |指示是否要应用的条件或例外顺序中的传入消息的**ToRecipients**或**CcRecipients**属性中的邮箱的所有者。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示必须在应用的条件或例外顺序中的传入邮件标记的敏感度。  <br/> |
|[WithinDateRange](withindaterange.md) <br/> |指定在其中传入消息必须已收到的条件或例外的顺序应用中的日期范围。  <br/> |
|[WithinSizeRange](withinsizerange.md) <br/> |指定的条件或例外的顺序应用必须传入消息的最小和最大大小。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[规则 (RuleType)](rule-ruletype.md) <br/> |包含单一规则并代表用户的邮箱中的规则。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[异常](exceptions.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

