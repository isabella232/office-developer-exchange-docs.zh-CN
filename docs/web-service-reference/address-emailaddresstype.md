---
title: Address (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Address
api_type:
- schema
ms.assetid: 518641c8-7f6f-496c-86f9-341e7c1bb44c
description: Address 元素表示完全解析的电子邮件地址。
ms.openlocfilehash: ff26a8d6de1e9bf36bb8dff5bc0141974220cf90
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546810"
---
# <a name="address-emailaddresstype"></a>Address (EmailAddressType)

**Address** 元素表示完全解析的电子邮件地址。 
  
```XML
<Address>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Address >
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[名称 (EmailAddressType)](name-emailaddresstype.md) <br/> |定义邮箱用户的名称。此元素是可选的。  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |定义用于邮箱路由。默认值为 SMTP。此元素是可选的。  <br/> |
|[MailboxType](mailboxtype.md) <br/> |定义邮箱用户的邮箱类型。此元素是可选的。  <br/> |
|[ItemId](itemid.md) <br/> |定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[OriginalRecipients](originalrecipients.md) <br/> |包含表示跟踪邮件的原始收件人的电子邮件地址的集合。  <br/> |
|[RoomLists](roomlists.md) <br/> |包含组织中会议室的列表。  <br/> |
|[SentToAddresses](senttoaddresses.md) <br/> |包含传入邮件必须发送到的电子邮件地址列表，以便条件或例外情况适用。  <br/> |
   
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
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md) 
- [GetRoomLists 操作](getroomlists-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

