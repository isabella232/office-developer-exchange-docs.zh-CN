---
title: 收件人
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Recipient
api_type:
- schema
ms.assetid: 52adbb30-3bfd-48aa-9ea8-9f7d3b4bee44
description: Recipient 元素表示发生事件的收件人。
ms.openlocfilehash: 5978ca36a6caa33be086e6a051df944cfd07b457
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532222"
---
# <a name="recipient"></a>收件人

Recipient 元素表示发生事件的收件人。 
  
```XML
<Recipient>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Recipient>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[名称 (EmailAddressType)](name-emailaddresstype.md) <br/> |表示邮箱用户的名称。 此元素为可选。  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |定义邮箱用户的主简单邮件传输 (SMTP) 地址。 此元素为可选。  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |定义供邮箱使用的路由。 默认值为 SMTP。 此元素为可选。  <br/> |
|[MailboxType](mailboxtype.md) <br/> |表示由电子邮件地址表示的邮箱的类型。 此元素为可选。  <br/> |
|[ItemId](itemid.md) <br/> |定义用户的联系人文件夹中的收件人的联系人或个人通讯组列表的项标识符。此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |包含收件人的单个事件的信息。  <br/> |
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |指定要查找的邮件类型的条件。  <br/> |
   
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



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

