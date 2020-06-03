---
title: FieldUri (规则)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: FieldURI 元素指定导致验证错误的规则字段的 URI。
ms.openlocfilehash: 3d88efdf951af580f81b5e2e7a544dcdf70ea830
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461245"
---
# <a name="fielduri-rule"></a>FieldUri (规则)

**FieldURI**元素指定导致验证错误的规则字段的 URI。 
  
```XML
<FieldURI/>
```

 **RuleFieldURIType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Error](error.md) <br/> |表示特定规则属性值、谓词属性值或 action 属性值上的单个验证错误。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值被限制为以下字符串之一：
  
- RuleId
    
- DisplayName
    
- 优先级
    
- IsNotSupported
    
- 操作
    
- 条件：类别
    
- 条件： ContainsBodyStrings
    
- 条件： ContainsHeaderStrings
    
- 条件： ContainsRecipientStrings
    
- 条件： ContainsSenderStrings
    
- 条件： ContainsSubjectOrBodyStrings
    
- 条件： ContainsSubjectStrings
    
- 条件： FlaggedForAction
    
- 条件： FromAddresses
    
- 条件： FromConnectedAccounts
    
- 条件： HasAttachments
    
- 条件：重要性
    
- 条件： IsApprovalRequest
    
- 条件： IsAutomaticForward
    
- 条件： IsAutomaticReply
    
- 条件： IsEncrypted
    
- 条件： IsMeetingRequest
    
- 条件： IsMeetingResponse
    
- 条件： IsNDR
    
- 条件： IsPermissionControlled
    
- 条件： IsReadReceipt
    
- 条件： IsSigned
    
- 条件： IsVoicemail
    
- 条件： ItemClasses
    
- 条件： MessageClassifications
    
- 条件： NotSentToMe
    
- 条件： SentCcMe
    
- 条件： SentOnlyToMe
    
- 条件： SentToAddresses
    
- 条件： SentToMe
    
- 条件： SentToOrCcMe
    
- 条件：敏感度
    
- 条件： WithinDateRange
    
- 条件： WithinSizeRange
    
- 异常：类别
    
- 异常： ContainsBodyStrings
    
- 异常： ContainsHeaderStrings
    
- 异常： ContainsRecipientStrings
    
- 异常： ContainsSenderStrings
    
- 异常： ContainsSubjectOrBodyStrings
    
- 异常： ContainsSubjectStrings
    
- 异常： FlaggedForAction
    
- 异常： FromAddresses
    
- 异常： FromConnectedAccounts
    
- 异常： HasAttachments
    
- 异常：重要性
    
- 异常： IsApprovalRequest
    
- 异常： IsAutomaticForward
    
- 异常： IsAutomaticReply
    
- 异常： IsEncrypted
    
- 异常： IsMeetingRequest
    
- 异常： IsMeetingResponse
    
- 异常： IsNDR
    
- 异常： IsPermissionControlled
    
- 异常： IsReadReceipt
    
- 异常： IsSigned
    
- 异常： IsVoicemail
    
- 异常： ItemClasses
    
- 异常： MessageClassifications
    
- 异常： NotSentToMe
    
- 异常： SentCcMe
    
- 异常： SentOnlyToMe
    
- 异常： SentToAddresses
    
- 异常： SentToMe
    
- 异常： SentToOrCcMe
    
- 异常：敏感度
    
- 异常： WithinDateRange
    
- 异常： WithinSizeRange
    
- 操作： AssignCategories
    
- 操作： CopyToFolder
    
- 操作：删除
    
- 操作： ForwardAsAttachmentToRecipients
    
- 操作： ForwardToRecipients
    
- 操作： MarkImportance
    
- 操作： MarkAsRead
    
- 操作： MoveToFolder
    
- 操作： PermanentDelete
    
- 操作： RedirectToRecipients
    
- 操作： SendSMSAlertToRecipients
    
- 操作： ServerReplyWithMessage
    
- 操作： StopProcessingRules
    
- IsEnabled
    
- IsInError
    
- 条件
    
- 异常
    
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

