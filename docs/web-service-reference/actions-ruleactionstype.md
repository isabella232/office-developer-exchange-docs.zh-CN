---
title: 操作（RuleActionsType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2afba70c-65f7-458c-a4e6-a2cd9bccc0f9
description: Actions 元素包含与收件箱规则关联的操作的列表。
ms.openlocfilehash: fbef3b69b1688d7c612af018d6a19f9ec1728066
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529677"
---
# <a name="actions-ruleactionstype"></a>操作（RuleActionsType）

**Actions**元素包含与收件箱规则关联的操作的列表。 
  
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
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

