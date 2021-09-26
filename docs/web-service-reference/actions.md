---
title: 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: Actions 元素表示满足条件时对邮件可采取的一组操作。
ms.openlocfilehash: 7f6608af5b8a9eb2772228a638fc42b9558f1e42
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546859"
---
# <a name="actions"></a>操作

**Actions** 元素表示满足条件时对邮件可采取的一组操作。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AssignCategories](assigncategories.md) <br/> |表示在电子邮件上标记的类别。  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |标识电子邮件项目将复制到的文件夹的 ID。  <br/> |
|[删除](delete.md) <br/> |指示是否将邮件移动到"已删除邮件"文件夹。  <br/> |
|[ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) <br/> |指示作为附件转发邮件的电子邮件地址。  <br/> |
|[ForwardToRecipients](forwardtorecipients.md) <br/> |指示邮件要转发到的电子邮件地址。  <br/> |
|[MarkImportance](markimportance.md) <br/> |指定在邮件上标记的重要性。  <br/> |
|[MarkAsRead](markasread.md) <br/> |指示邮件是否标记为已读。  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |标识电子邮件项目将移动到的文件夹的 ID。  <br/> |
|[PermanentDelete](permanentdelete.md) <br/> |指示是否永久删除邮件，而不是保存到"已删除邮件"文件夹。  <br/> |
|[RedirectToRecipients](redirecttorecipients.md) <br/> |指示邮件重定向到的电子邮件地址。  <br/> |
|[SendSMSAlertToRecipients](sendsmsalerttorecipients.md) <br/> |指示短信服务向其中发送短信 (短信) 发送通知的移动电话号码。  <br/> |
|[ServerReplyWithMessage](serverreplywithmessage.md) <br/> |指示。 要作为传入邮件回复发送的模板邮件的 ID。  <br/> |
|[StopProcessingRules](stopprocessingrules.md) <br/> |指示是否评估后续规则。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[规则 (RuleType)](rule-ruletype.md) <br/> |表示用户邮箱中的单个规则。  <br/> |
   
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

- [条件](conditions.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

