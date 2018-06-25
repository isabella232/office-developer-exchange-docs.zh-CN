---
title: 在 Exchange 处理删除相关 EWS 中的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: 了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中删除相关的错误。
ms.openlocfilehash: 0dc16c3350bb75fb1e91650f0a0f0b7423727eeb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752713"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a>在 Exchange 处理删除相关 EWS 中的错误

了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中删除相关的错误。
  
如果[项目和文件夹中删除](deleting-items-by-using-ews-in-exchange.md)您在应用程序，您可能需要处理删除相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。
  
**表 1： 删除相关错误和如何处理它们**

|**Error**|**您尝试对时发生...**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |删除实例定期任务，并**AffectedTaskOccurrence**属性未设置。  <br/> |设置**AffectedTaskOccurrence**属性，并删除重试。  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |更新日历项目位于已删除邮件文件夹中时更新将导致向与会者发送会议邀请。  <br/> |取消更新或将日历项目移回默认日历文件夹和更新的日历项目。  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |引用已删除的匹配项的定期约会。  <br/> |删除已删除的匹配项的引用。  <br/> |
|ErrorCannotDeleteObject  <br/> |删除无法删除项目。  <br/> |退出尝试删除项。  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |删除非定期任务的匹配项，或删除一个周期性任务的最后一个实例。  <br/> |删除非定期任务或退出尝试删除一个周期性任务的最后一个实例。  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |删除可分辨的文件夹。  <br/> |指示不能删除默认文件夹。  <br/> |
|ErrorItemNotFound  <br/> |永久删除项目的访问。  <br/> |从存储区删除时，请删除项目的引用。 如果项目恢复，请确保您复原对客户端所需的引用。  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |删除日历项目时未指定是否应发送会议取消。  <br/> |指定会议取消应或不应发送。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [通过在 Exchange 使用 EWS 中删除项目](deleting-items-by-using-ews-in-exchange.md)
    
- [在 Exchange 拉 EWS 删除相关邮箱事件通知](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [删除约会，并在 Exchange 使用 EWS 取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

