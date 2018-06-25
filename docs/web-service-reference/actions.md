---
title: 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: Actions 元素表示一的组操作可用于满足条件时要采取的上一条消息。
ms.openlocfilehash: 093d2f28135c6077b6cea488591573af0182934b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753098"
---
# <a name="actions"></a>操作

**Actions**元素表示一的组操作可用于满足条件时要采取的上一条消息。 
  
[规则 (RuleType)](rule-ruletype.md)
  
```XML
<Actions>
    <AssignCategories>
    <CopyToFolder>
    <Delete>
    <ForwardAsAttachmentToRecipients>
    <ForwardToRecipients>
    <MarkImportance>
    <MarkAsRead>
    <MoveToFolder>
    <PermanentDelete>
    <RedirectToRecipients>
    <SendSMSAlertToRecipients>
    <ServerReplyWithMessage>
    <StopProcessingRules>
</Actions>
```

 **RuleActionsType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AssignCategories](assigncategories.md) <br/> |代表在电子邮件标记的类别。  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |标识的文件夹的电子邮件项目将被复制到的 ID。  <br/> |
|[删除](delete.md) <br/> |指示邮件是否被移动到已删除邮件文件夹。  <br/> |
|[ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) <br/> |指示邮件是作为附件转发的电子邮件地址。  <br/> |
|[ForwardToRecipients](forwardtorecipients.md) <br/> |指示邮件将被转接到的电子邮件地址。  <br/> |
|[MarkImportance](markimportance.md) <br/> |指定要在邮件上标记的重要性。  <br/> |
|[MarkAsRead](markasread.md) <br/> |指示是否要标记为已读消息。  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |标识的文件夹的电子邮件项目将移动到的 ID。  <br/> |
|[PermanentDelete](permanentdelete.md) <br/> |指示邮件是否被永久删除和不保存到已删除邮件文件夹。  <br/> |
|[RedirectToRecipients](redirecttorecipients.md) <br/> |指示邮件将被重定向到的电子邮件地址。  <br/> |
|[SendSMSAlertToRecipients](sendsmsalerttorecipients.md) <br/> |指示短信服务 (SMS) 通知将发送到移动电话号码。  <br/> |
|[ServerReplyWithMessage](serverreplywithmessage.md) <br/> |指示。 是作为对传入邮件的回复发送的模板邮件 ID。  <br/> |
|[StopProcessingRules](stopprocessingrules.md) <br/> |指示是否要进行求值后续规则。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[规则 (RuleType)](rule-ruletype.md) <br/> |代表用户的邮箱中的单个规则。  <br/> |
   
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

- [条件](conditions.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

