---
title: Actions (RuleActionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2afba70c-65f7-458c-a4e6-a2cd9bccc0f9
description: Actions 元素包含与收件箱规则关联的操作列表。
ms.openlocfilehash: d91a76889778b363ea931afb98ae9817e3b7c3c1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520176"
---
# <a name="actions-ruleactionstype"></a>Actions (RuleActionsType)

Actions 元素包含与收件箱规则关联的操作列表。 
  
```XML
<Actions>
   <AssignCategories/>
   <CopyToFolder/>
   <Delete/>
   <ForwardAsAttachmentToRecipients/>
   <ForwardToRecipients/>
   <MarkImportance/>
   <MarkAsRead/>
   <MoveToFolder/>
   <PermanentDelete/>
   <RedirectToRecipients/>
   <SendSMSAlertToRecipients/>
   <ServerReplyWithMessage/>
   <StopProcessingRules/>
</Actions>
```

 **RuleActionsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[AssignCategories](assigncategories.md)  | [CopyToFolder](copytofolder.md)  | [删除](delete.md)  | [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md)  | [ForwardToRecipients](forwardtorecipients.md)  | [MarkImportance](markimportance.md)  | [MarkAsRead](markasread.md)  | [MoveToFolder](movetofolder.md)  | [PermanentDelete](permanentdelete.md)  | [RedirectToRecipients](redirecttorecipients.md)  | [SendSMSAlertToRecipients](sendsmsalerttorecipients.md)  | [ServerReplyWithMessage](serverreplywithmessage.md)  | [StopProcessingRules](stopprocessingrules.md)
  
### <a name="parent-elements"></a>父元素

[规则 (RuleType)](rule-ruletype.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

