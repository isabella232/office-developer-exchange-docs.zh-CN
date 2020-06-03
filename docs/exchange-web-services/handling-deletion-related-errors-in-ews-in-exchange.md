---
title: 在 Exchange 中处理 EWS 中的与删除相关的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: 了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中与删除相关的错误。
ms.openlocfilehash: 41c217c1c3815606d898b8237ea327f34869174b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455945"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a>在 Exchange 中处理 EWS 中的与删除相关的错误

了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中与删除相关的错误。
  
如果您的应用程序[删除项目和文件夹](deleting-items-by-using-ews-in-exchange.md)，则可能需要处理与删除相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。
  
**表1：与删除相关的错误及其处理方法**

|**Error**|**当您尝试 .。。**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |删除定期任务的实例，并且不设置**AffectedTaskOccurrence**属性。  <br/> |设置**AffectedTaskOccurrence**属性，然后重试删除。  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |更新将导致向与会者发送会议邀请时，更新 "已删除邮件" 文件夹中的 "日历" 项目。  <br/> |取消更新或将日历项目移回默认的 "日历" 文件夹，并更新 "日历" 项目。  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |引用定期约会的已删除事件。  <br/> |删除对已删除事件的引用。  <br/> |
|ErrorCannotDeleteObject  <br/> |删除无法删除的项目。  <br/> |退出删除项目的尝试。  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |删除非定期任务的事件或删除定期任务的最后一个事件。  <br/> |删除非定期任务或退出删除定期任务的最后一个事件的尝试。  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |删除可分辨文件夹。  <br/> |指示不能删除默认文件夹。  <br/> |
|ErrorItemNotFound  <br/> |访问永久删除的项目。  <br/> |从存储区中删除对项的引用。 如果某项已恢复，请确保恢复对客户端所需的引用。  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |删除日历项目，而不指定是否应发送会议取消。  <br/> |指定应发送还是不应发送会议取消通知。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [使用 Exchange 中的 EWS 删除项目](deleting-items-by-using-ews-in-exchange.md)
    
- [Exchange 中有关与 EWS 删除相关邮箱事件的拉取通知](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [使用 Exchange 中的 EWS 删除约会和取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

