---
title: EmailAddress (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: EmailAddress 元素定义邮箱用户的主 SMTP 地址。
ms.openlocfilehash: 8740f6f7f67269de86aaa7383a7ad8f3cdf07a4a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512994"
---
# <a name="emailaddress-nonemptystringtype"></a>EmailAddress (NonEmptyStringType)

**EmailAddress** 元素定义邮箱用户的主 SMTP 地址。 
  
```XML
<EmailAddress/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ActingAs](actingas.md) <br/> |标识呼叫者发送身份。  <br/> |
|[邮箱](mailbox.md) <br/> | 标识完全解析的电子邮件地址。  <br/><br/>下面是此元素的一些 XPath 表达式：<br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/>以下是 Mailbox 元素的其他父元素：<br/><br/>- [BccRecipients](bccrecipients.md) <br/>- [ReplyTo](replyto.md) <br/>- [发件人](sender.md) <br/>- [从](from.md) <br/>- [组织者](organizer.md) <br/>- [DistinguishedFolderId](distinguishedfolderid.md) <br/>- [解决方案](resolution.md) <br/>- [DLExpansion](dlexpansion.md) <br/>- [Attendee](attendee.md) <br/> |
|[RoomList](roomlist.md) <br/> |按电子邮件地址标识会议室列表。  <br/> |
   
## <a name="text-value"></a>文本值

需要一个代表 SMTP 地址的文本值。
  
## <a name="remarks"></a>注解

**EmailAddress** 元素可以表示 SMTP 或旧版 Exchange可分辨 (也称为 DN) 地址。 **EmailAddress** 元素是唯一必需的 [Mailbox](mailbox.md)元素。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

