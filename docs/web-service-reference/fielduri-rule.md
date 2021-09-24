---
title: FieldUri (Rule)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cecdea78-de9c-48be-ae31-03877feafeec
description: FieldURI 元素指定导致验证错误的规则字段的 URI。
ms.openlocfilehash: c1390f6643614216fa86053368ba012cd0883ff7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513729"
---
# <a name="fielduri-rule"></a>FieldUri (Rule)

FieldURI 元素指定导致验证错误的规则字段的 **URI。** 
  
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
|[Error](error.md) <br/> |表示特定规则属性值、谓词属性值或操作属性值上的单个验证错误。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值仅限于以下字符串之一：
  
- RuleId
    
- DisplayName
    
- 优先级
    
- IsNotSupported
    
- 操作
    
- 条件：类别
    
- Condition：ContainsBodyStrings
    
- Condition：ContainsHeaderStrings
    
- Condition：ContainsRecipientStrings
    
- Condition：ContainsSenderStrings
    
- Condition：ContainsSubjectOrBodyStrings
    
- Condition：ContainsSubjectStrings
    
- Condition：FlaggedForAction
    
- Condition：FromAddresses
    
- Condition：FromConnectedAccounts
    
- Condition：HasAttachments
    
- 条件：重要性
    
- Condition：IsApprovalRequest
    
- Condition：IsAutomaticForward
    
- Condition：IsAutomaticReply
    
- 条件：IsEncrypted
    
- Condition：IsMeetingRequest
    
- Condition：IsMeetingResponse
    
- 条件：IsNDR
    
- Condition：IsPermissionControlled
    
- Condition：IsReadReceipt
    
- Condition：IsSigned
    
- Condition：IsVoicemail
    
- Condition：ItemClasses
    
- Condition：MessageClassifications
    
- Condition：NotSentToMe
    
- Condition：SentCcMe
    
- Condition：SentOnlyToMe
    
- Condition：SentToAddresses
    
- Condition：SentToMe
    
- Condition：SentToOrCcMe
    
- 条件：敏感度
    
- Condition：WithinDateRange
    
- Condition：WithinSizeRange
    
- 异常：类别
    
- 异常：ContainsBodyStrings
    
- 异常：ContainsHeaderStrings
    
- 异常：ContainsRecipientStrings
    
- 异常：ContainsSenderStrings
    
- 异常：ContainsSubjectOrBodyStrings
    
- 异常：ContainsSubjectStrings
    
- 异常：FlaggedForAction
    
- 异常：FromAddresses
    
- 异常：FromConnectedAccounts
    
- 异常：HasAttachments
    
- 异常：重要性
    
- 异常：IsApprovalRequest
    
- 异常：IsAutomaticForward
    
- 异常：IsAutomaticReply
    
- 异常：IsEncrypted
    
- 异常：IsMeetingRequest
    
- 异常：IsMeetingResponse
    
- 异常：IsNDR
    
- 异常：IsPermissionControlled
    
- 异常：IsReadReceipt
    
- 异常：IsSigned
    
- 异常：IsVoicemail
    
- 异常：ItemClasses
    
- 异常：MessageClassifications
    
- 异常：NotSentToMe
    
- 异常：SentCcMe
    
- 异常：SentOnlyToMe
    
- 异常：SentToAddresses
    
- 异常：SentToMe
    
- 异常：SentToOrCcMe
    
- 异常：敏感度
    
- Exception：WithinDateRange
    
- 异常：WithinSizeRange
    
- Action：AssignCategories
    
- Action：CopyToFolder
    
- 操作：删除
    
- Action：ForwardAsAttachmentToRecipients
    
- Action：ForwardToRecipients
    
- Action：MarkImportance
    
- Action：MarkAsRead
    
- Action：MoveToFolder
    
- Action：PermanentDelete
    
- Action：RedirectToRecipients
    
- Action：SendSMSAlertToRecipients
    
- Action：ServerReplyWithMessage
    
- Action：StopProcessingRules
    
- IsEnabled
    
- IsInError
    
- 条件
    
- 例外
    
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

