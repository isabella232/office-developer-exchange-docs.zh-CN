---
title: GetItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: 查找信息执行 GetItem EWS 操作。
ms.openlocfilehash: 9b63032b2eaa3bf26027a42e38bfa06bedcbac86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754602"
---
# <a name="getitem-operation"></a>GetItem Operation

查找有关**GetItem** EWS 操作的信息。 
  
**GetItem**操作获取从 Exchange 存储的项。 
  
## <a name="using-the-getitem-operation"></a>使用 GetItem 操作

**GetItem**操作返回许多项属性。 **GetItem**响应中返回的属性有所不同，根据该请求的形状，返回请求的其他属性，和项目类型。 
  
[消息](message-ex15websvcsotherref.md)元素表示电子邮件和非 Exchange Web Services (EWS) 架构的强类型的所有其他项目。 如 IPM 的项目。共享和[消息](message-ex15websvcsotherref.md)元素以返回 IPM.InfoPath。 Exchange 不在响应中返回基本的[Item](item.md)元素。 
  
**GetItem**操作不会返回附件。 它确实返回有关的附加的项或文件的元数据。 若要返回附件，请使用[GetAttachment 操作](getattachment-operation.md)。
  
## <a name="getitem-operation-soap-headers"></a>GetItem 操作 SOAP 标头

**GetItem**操作可以使用下表中列出的 SOAP 标头。 
  
|标头 ***|****Element****|****说明****|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |指定在从服务器中，以秒为单位，或以毫秒为单位的响应中的数据/时间值的分辨率。  <br/> |
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识模拟客户端应用程序的用户。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应该请求的服务器的版本。  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |确定要用于来自服务器的所有响应的时区。  <br/> |
   
## <a name="in-this-section"></a>本部分内容

[GetItem 操作 （电子邮件）](getitem-operation-email-message.md)
  
[GetItem 操作 （日历项）](getitem-operation-calendar-item.md)
  
[GetItem 操作 （任务）](getitem-operation-task.md)
  
[GetItem 操作 （联系人）](getitem-operation-contact.md)
  
## <a name="see-also"></a>另请参阅



[Exchange 的 EWS 引用](ews-reference-for-exchange.md)

