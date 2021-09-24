---
title: Id (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Id
api_type:
- schema
ms.assetid: 3e1e37b5-5469-4447-ad1f-c2c6d4e0482f
description: Id 元素标识 Exchange 服务器组织的会议室。
ms.openlocfilehash: 40f2163c4525e766e0fe0377820e87a806562001
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525820"
---
# <a name="id-emailaddresstype"></a>Id (EmailAddressType)

**Id** 元素标识 Exchange 服务器组织的会议室。 
  
[Room](room.md)
  
[Id (EmailAddressType)](id-emailaddresstype.md)
  
```xml
<Id>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Id>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[名称 (EmailAddressType)](name-emailaddresstype.md) <br/> |定义会议室的名称。 此元素为可选。  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |定义会议室的简单邮件传输 (SMTP) 地址。 此元素为可选。  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |定义用于邮箱路由。默认值为 SMTP。此元素是可选的。  <br/> |
|[MailboxType](mailboxtype.md) <br/> |定义邮箱用户的邮箱类型。此元素是可选的。  <br/> |
|[ItemId](itemid.md) <br/> |定义用户联系人文件夹收件人的联系人或私人通讯组列表的项标识符。此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Room](room.md) <br/> |在服务器组织中定义Exchange会议室。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetRooms 操作](getrooms-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

