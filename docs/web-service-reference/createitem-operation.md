---
title: CreateItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 78a52120-f1d0-4ed7-8748-436e554f75b6
description: CreateItem 操作在 Exchange 存储中创建项目。
ms.openlocfilehash: f6aaa9ed8e8257f19780492d6137fb015c1b6136
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458864"
---
# <a name="createitem-operation"></a>CreateItem 操作

CreateItem 操作在 Exchange 存储中创建项目。
  
## <a name="using-the-createitem-operation"></a>使用 CreateItem 操作

您可以使用 CreateItem 操作创建以下内容：
  
- 日历项目
    
- 电子邮件
    
- 会议请求
    
- 任务
    
- 联系人
    
有关详细信息，请参阅[CreateItem 操作（日历项目）](createitem-operation-calendar-item.md)、 [CreateItem 操作（电子邮件）](createitem-operation-email-message.md)、 [CreateItem 操作（会议请求）](createitem-operation-meeting-request.md)、 [CreateItem 操作（任务）](createitem-operation-task.md)和[CreateItem 操作（联系人）](createitem-operation-contact.md)。
  
CreateItem 操作支持使用 response 对象。 Response 对象支持会议的接受和拒绝，以及处理标准电子邮件中包含的投票按钮。 下表列出了在 CreateItem 操作中处理的响应对象。
  
|**Response 对象**|**Action**|
|:-----|:-----|
|AcceptItem  <br/> |接受会议请求。  <br/> |
|CancelCalendarItem  <br/> |取消会议。 这与删除所有与会者的方法不同，因为它也会删除组织者的会议。  <br/> |
|DeclineItem  <br/> |拒绝会议请求。  <br/> |
|ForwardItem  <br/> |将会议请求作为会议请求发送给其他人。  <br/> |
|RemoveItem  <br/> |从日历中删除取消的会议。  <br/> |
|ReplyAllToItem  <br/> |向会议的所有与会者发送包含原始会议请求正文的邮件。  <br/> |
|ReplyToItem  <br/> |将包含原始会议请求正文的邮件发送给会议请求的发件人。  <br/> |
|SendReadReceipt  <br/> |将 "已读" 回执发送给会议请求的发件人。  <br/> |
|TentativelyAcceptItem  <br/> |暂时接受会议请求。  <br/> |
   
CreateItem 操作还支持其他会议对象。 下表列出了 CreateItem 操作支持的其他对象。
  
|**会议对象**|**说明**|
|:-----|:-----|
|会议邮件  <br/> |表示 Exchange 存储中的会议邮件。 这是其他会议对象的基本对象。  <br/> |
|会议要求  <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|会议响应  <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|会议取消  <br/> |表示 Exchange 存储中的会议取消。  <br/> |
   
## <a name="see-also"></a>另请参阅



[CreateItem 操作（日历项目）](createitem-operation-calendar-item.md)
  
[CreateItem 操作（联系人）](createitem-operation-contact.md)
  
[CreateItem 操作（电子邮件）](createitem-operation-email-message.md)
  
[CreateItem 操作（会议请求）](createitem-operation-meeting-request.md)
  
[CreateItem 操作（任务）](createitem-operation-task.md)
  
 **CreateItemType**

