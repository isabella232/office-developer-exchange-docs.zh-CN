---
title: GetItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: 查找有关 GetItem EWS 操作的信息。
localization_priority: Priority
ms.openlocfilehash: 8871dde183974454fc27dbddda489e6b0a70f3aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463326"
---
# <a name="getitem-operation"></a>GetItem 操作

查找有关**GetItem** EWS 操作的信息。 
  
**GetItem**操作从 Exchange 存储中获取项目。 
  
## <a name="using-the-getitem-operation"></a>使用 GetItem 操作

**GetItem**操作返回许多项目属性。 **GetItem**响应中返回的属性根据所请求的形状、请求的其他属性和返回的项目类型而有所不同。 
  
[Message](message-ex15websvcsotherref.md)元素表示的电子邮件和所有其他不是由 Exchange Web 服务（EWS）架构强类型化的项目。 项目，如 IPM。共享和 IPM. InfoPath 以[邮件](message-ex15websvcsotherref.md)元素的形式返回。 Exchange 不会在响应中返回基本[项目](item.md)元素。 
  
**GetItem**操作不会返回附件。 它会返回有关附加项或文件的元数据。 若要返回附件，请使用[GetAttachment 操作](getattachment-operation.md)。
  
## <a name="getitem-operation-soap-headers"></a>GetItem 操作 SOAP 标头

**GetItem**操作可以使用下表中列出的 SOAP 标头。 
  
|标头 * * * *|****Element****|****说明****|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |指定对来自服务器的响应中的数据/时间值的解析（以秒或毫秒为单位）。  <br/> |
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序模拟的用户。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器版本。  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |标识要用于来自服务器的所有响应的时区。  <br/> |
   
## <a name="in-this-section"></a>本部分内容

[GetItem 操作（电子邮件）](getitem-operation-email-message.md)
  
[GetItem 操作（日历项目）](getitem-operation-calendar-item.md)
  
[GetItem 操作（任务）](getitem-operation-task.md)
  
[GetItem 操作（联系人）](getitem-operation-contact.md)
  
## <a name="see-also"></a>另请参阅



[Exchange 的 EWS 引用](ews-reference-for-exchange.md)

