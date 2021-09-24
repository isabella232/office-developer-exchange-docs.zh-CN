---
title: 处理 EWS 中与删除相关的Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1bbe8507-7730-45e5-9232-c4f6fc39c2d9
description: 了解如何在应用程序中使用 EWS 托管 API 或 EWS 开发的应用程序处理与删除Exchange。
ms.openlocfilehash: d82901a2ebc8577258e191cbd014db93cc40d099
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513253"
---
# <a name="handling-deletion-related-errors-in-ews-in-exchange"></a>处理 EWS 中与删除相关的Exchange

了解如何在应用程序中使用 EWS 托管 API 或 EWS 开发的应用程序处理与删除Exchange。
  
如果应用程序 [删除项目和文件夹](deleting-items-by-using-ews-in-exchange.md)，您可能需要处理与删除相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。
  
**表 1：与删除相关的错误以及如何处理这些错误**

|**错误**|**在尝试...**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorAffectedTaskOccurrencesRequired  <br/> |删除定期任务的实例，并且未设置 **AffectedTaskOccurrence** 属性。  <br/> |设置 **AffectedTaskOccurrence** 属性，然后重试删除。  <br/> |
|ErrorCalendarCannotUpdateDeletedItem  <br/> |更新将导致向与会者发送会议邀请时，更新位于"已删除邮件"文件夹中的日历项目。  <br/> |取消更新或将日历项目移回默认的"日历"文件夹并更新日历项目。  <br/> |
|ErrorCalendarOccurrenceIsDeletedFromRecurrence  <br/> |引用定期约会的已删除事件。  <br/> |删除对已删除事件的引用。  <br/> |
|ErrorCannotDeleteObject  <br/> |删除无法删除的项目。  <br/> |退出尝试删除项目。  <br/> |
|ErrorCannotDeleteTaskOccurrence  <br/> |删除非定期任务的发生次数或删除最后一次出现的定期任务。  <br/> |删除非定期任务或退出尝试以删除最后一次出现的定期任务。  <br/> |
|ErrorDeleteDistinguishedFolder  <br/> |删除可分辨文件夹。  <br/> |指示无法删除默认文件夹。  <br/> |
|ErrorItemNotFound  <br/> |访问永久删除的项目。  <br/> |从存储区中删除对项目的引用。 如果恢复项目，请确保恢复对客户端的必需引用。  <br/> |
|ErrorSendMeetingCancellationsRequired  <br/> |删除日历项目，而不指定是否应该发送会议取消。  <br/> |指定应发送或不应发送会议取消。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [使用 Exchange 中的 EWS 删除项目](deleting-items-by-using-ews-in-exchange.md)
    
- [拉取与 EWS 删除相关的邮箱事件Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [使用 Exchange 中的 EWS 删除约会和取消Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

