---
title: PurportedSender
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PurportedSender
api_type:
- schema
ms.assetid: eb7a54ec-2e48-4030-bbcf-50a31609691b
description: PurportedSender 元素包含有关电子邮件的可能发件人的联系人信息。
ms.openlocfilehash: 115aecad08211f838cabb7dae39f8eb5989ddc81
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523718"
---
# <a name="purportedsender"></a>PurportedSender

**PurportedSender** 元素包含有关电子邮件的可能发件人的联系人信息。 
  
```XML
<PurportedSender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</PurportedSender>
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
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |定义邮箱用户的简单邮件传输协议 (SMTP)地址。此元素是可选的。  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |表示收件人的路由协议。 默认值为 SMTP。 此元素为可选。  <br/> |
|[MailboxType](mailboxtype.md) <br/> |表示由电子邮件地址表示的邮箱的类型。 此元素为可选。  <br/> |
|[ItemId](itemid.md) <br/> |定义用户联系人文件夹收件人的联系人或私人通讯组列表的项标识符。此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |指定要查找的邮件类型的条件。  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |包含 [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) 元素的单个邮件结果。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

