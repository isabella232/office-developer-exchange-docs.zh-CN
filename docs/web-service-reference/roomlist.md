---
title: RoomList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoomList
api_type:
- schema
ms.assetid: cb02bdf0-df9f-4e31-b7dd-cd9f2f2cc2b2
description: RoomList 元素表示标识会议室列表的电子邮件地址。
ms.openlocfilehash: 0444475cb9fffbb89ba2861096baee0c7e645995
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460517"
---
# <a name="roomlist"></a>RoomList

**RoomList**元素表示标识会议室列表的电子邮件地址。 
  
[GetRooms](getrooms.md)
  
[RoomList](roomlist.md)
  
```XML
<RoomList>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</RoomList>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[名称 (EmailAddressType)](name-emailaddresstype.md) <br/> |定义会议室列表的显示名称。 此元素为可选。  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |定义会议室列表的简单邮件传输协议（SMTP）地址。 此元素为可选。  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |定义用于邮箱路由。默认值为 SMTP。此元素是可选的。  <br/> |
|[MailboxType](mailboxtype.md) <br/> |定义邮箱用户的邮箱类型。此元素是可选的。  <br/> |
|[ItemId](itemid.md) <br/> |定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetRooms](getrooms.md) <br/> |请求中的根元素，用于获取特定聊天室列表中的聊天室列表。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
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



[GetRooms 操作](getrooms-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

