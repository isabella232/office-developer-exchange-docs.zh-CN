---
title: EmailAddress (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: EmailAddress 元素定义邮箱用户的主 SMTP 地址。
ms.openlocfilehash: fcc3e650d5fc32344022ed6f015d4096a4461f63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463130"
---
# <a name="emailaddress-nonemptystringtype"></a>EmailAddress (NonEmptyStringType)

**EmailAddress**元素定义邮箱用户的主 SMTP 地址。 
  
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
|[ActingAs](actingas.md) <br/> |标识呼叫者发送的人。  <br/> |
|[邮箱](mailbox.md) <br/> | 标识完全解析的电子邮件地址。  <br/><br/>以下是此元素的一些 XPath 表达式：<br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/>以下是邮箱元素的其他父元素：<br/><br/>- [BccRecipients](bccrecipients.md) <br/>- [ReplyTo](replyto.md) <br/>- [给](sender.md) <br/>- [从](from.md) <br/>- [组织者](organizer.md) <br/>- [DistinguishedFolderId](distinguishedfolderid.md) <br/>- [办法](resolution.md) <br/>- [DLExpansion](dlexpansion.md) <br/>- [与会](attendee.md) <br/> |
|[RoomList](roomlist.md) <br/> |通过电子邮件地址标识会议室列表。  <br/> |
   
## <a name="text-value"></a>文本值

需要一个代表 SMTP 地址的文本值。
  
## <a name="remarks"></a>备注

**EmailAddress**元素可以表示 SMTP 或旧版 Exchange 可分辨名称（也称为 DN）地址。 **EmailAddress**元素是唯一一个必需的[邮箱](mailbox.md)元素。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

