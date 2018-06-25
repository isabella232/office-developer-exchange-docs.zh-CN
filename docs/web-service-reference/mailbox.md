---
title: Mailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: befc70fd-51cb-4258-884c-80c9050f0e82
description: Mailbox 元素标识启用了邮件的 Active Directory 对象。
ms.openlocfilehash: e9fa21f3678249a9ac13d567b88beaf0177f989f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826258"
---
# <a name="mailbox"></a>Mailbox

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Mailbox** 元素标识启用了邮件的 Active Directory 对象。 
  
```XML
<Mailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Mailbox>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[名称 (EmailAddressType)](name-emailaddresstype.md) <br/> |定义邮箱用户的名称。此元素是可选的。  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。  <br/> |
|[RoutingType （电子邮件地址）](routingtype-emailaddress.md) <br/> |定义用于邮箱路由。默认值为 SMTP。此元素是可选的。  <br/> |
|[MailboxType](mailboxtype.md) <br/> |定义邮箱用户的邮箱类型。此元素是可选的。  <br/> |
|[ItemId](itemid.md) <br/> |定义用户联系人文件夹收件人的联系人或私人通讯组列表的项标识符。此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExpandDL](expanddl.md) <br/> |定义展开通讯组列表的请求。 <br/> <br/> 下面是此元素的 XPath 表达式： ` /ExpandDL ` <br/> |
|[ToRecipients](torecipients.md) <br/> |包含项目的收件人数组。  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |表示将收到邮件副本的收件人集合。  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。  <br/> |
|[回复](replyto.md) <br/> |标识副本应发送到的电子邮件地址数组。  <br/> |
|[发件人](sender.md) <br/> |标识项目的发件人。  <br/> |
|[发件人](from.md) <br/> |表示邮件发件人的地址。  <br/> |
|[Organizer](organizer.md) <br/> |表示会议的组织者。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> | 标识默认的 Microsoft Exchange Server 2007 文件夹。  <br/><br/>  下面是此元素的 XPath 表达式： <br/> <br/>  `/CreateItem/ParentFolderId/DistinguishedFolderId` <br/>  `/CreateFolder/ParentFolderId/DistinguishedFolderId` <br/> |
|[解决方法](resolution.md) <br/> |包含单个已解析的实体。  <br/> |
|[DLExpansion](dlexpansion.md) <br/> |包含通讯组列表包含的邮箱数组。  <br/> |
|[参与者](attendee.md) <br/> |表示日历项的与会者和资源。  <br/> |
|[CreateManagedFolder](createmanagedfolder.md) <br/> |定义请求以将托管文件夹添加到邮箱。  <br/> |
|[AddDelegate](adddelegate.md) <br/> |定义请求以将代理人添加到邮箱。  <br/> |
|[GetDelegate](getdelegate.md) <br/> |定义请求以获取有关委派给邮箱的信息。  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |定义请求以从邮箱删除代理人。  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |定义请求以更新邮箱中的代理人。  <br/> |
|[ReceivedBy](receivedby.md) <br/> |描述委派访问方案中的代理人。  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |描述委派访问方案中的主体。  <br/> |
|[Member](member-ex15websvcsotherref.md) <br/> |表示一个通讯组列表的成员。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) 和 [ItemId](itemid.md) 元素识别邮箱或通讯组列表。 

[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) 元素通过 SMTP 地址识别邮箱或通讯组列表。 

[ItemId](itemid.md) 元素通过与特定邮箱相关联的项标识符识别邮箱。 

无法使用 [ItemId](itemid.md) 元素向公共联系人文件夹中的通讯组列表或联系人发送邮件。 在尝试向联系人公共文件夹中的通讯组列表或联系人发送邮件时，如果在 CreateItem、UpdateItem 或 SendItem 操作中使用此元素则会引发错误。 使用 ExpandDL 操作获取 SMTP 地址，然后通过使用 [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) 元素发送邮件，而不是使用 [ItemId](itemid.md) 元素。 
  
另一个元素 [邮箱 (可用性)](mailbox-availability.md) 为可用性操作提供信息。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

