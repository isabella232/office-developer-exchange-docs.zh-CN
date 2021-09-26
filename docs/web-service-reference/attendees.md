---
title: 与会者
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 837bb372-39eb-48ae-9c09-0d2552511f93
description: Attendees 元素指定会议邀请的收件人。
ms.openlocfilehash: 2ac547ee56e5a001e08957265053265d69ded42e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545706"
---
# <a name="attendees"></a>与会者

**Attendees** 元素指定会议邀请的收件人。 
  
```XML
<Attendees>
    <EmailUser></EmailUser>
</Attendees>
```

 **ArrayOfEmailUsersType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[EmailUser](emailuser.md) <br/> |指定电子邮件收件人或 Active Directory 联系人。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MeetingSuggestion](meetingsuggestion.md) <br/> |指定建议的会议。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

