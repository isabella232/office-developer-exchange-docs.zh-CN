---
title: CreateItem Operation
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
description: CreateItem operation，在 Exchange 存储中创建项目。
ms.openlocfilehash: 7e1808c685cdbaa1e8867aa7425b2cc52218d001
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753665"
---
# <a name="createitem-operation"></a>CreateItem Operation

CreateItem operation，在 Exchange 存储中创建项目。
  
## <a name="using-the-createitem-operation"></a>使用 CreateItem 操作

您可以使用 CreateItem 操作创建以下：
  
- 日历项目
    
- 电子邮件
    
- 会议要求
    
- 任务
    
- 联系人
    
有关详细信息，请参阅[CreateItem operation，（日历项）](createitem-operation-calendar-item.md)、 [CreateItem operation，（电子邮件）](createitem-operation-email-message.md)、 [CreateItem operation，（会议请求）](createitem-operation-meeting-request.md)、 [CreateItem operation，（任务）](createitem-operation-task.md)和[CreateItem operation，（联系人）](createitem-operation-contact.md).
  
CreateItem operation 支持响应对象的使用。 响应对象才支持可接受和拒绝会议和处理的标准电子邮件中包含的投票按钮。 下表列出 CreateItem 操作中处理的响应对象。
  
|**响应对象**|**Action**|
|:-----|:-----|
|AcceptItem  <br/> |接受会议请求。  <br/> |
|CancelCalendarItem  <br/> |取消会议。 这不同于正在删除所有与会者，因为它也将删除会议组织者。  <br/> |
|DeclineItem  <br/> |拒绝会议请求。  <br/> |
|ForwardItem  <br/> |作为会议请求发送给其他人的会议请求。  <br/> |
|RemoveItem  <br/> |从日历中删除已取消的会议。  <br/> |
|ReplyAllToItem  <br/> |发送一条消息，包括向所有与会者的会议的原始会议请求的正文。  <br/> |
|ReplyToItem  <br/> |发送一条消息，包括对会议要求的发件人的原始会议请求的正文。  <br/> |
|SendReadReceipt  <br/> |向会议请求的发件人发送已读的回执。  <br/> |
|TentativelyAcceptItem  <br/> |暂时接受会议请求。  <br/> |
   
CreateItem operation，还支持其他会议对象。 下表列出 CreateItem operation 支持的其他对象。
  
|**会议对象**|**说明**|
|:-----|:-----|
|会议消息  <br/> |代表 Exchange 存储中的会议消息。 这是其他会议对象的基对象。  <br/> |
|会议要求  <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|会议响应  <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|取消会议  <br/> |表示 Exchange 存储中的会议取消。  <br/> |
   
## <a name="see-also"></a>另请参阅



[CreateItem operation，（日历项）](createitem-operation-calendar-item.md)
  
[CreateItem operation，（联系人）](createitem-operation-contact.md)
  
[CreateItem operation，（电子邮件）](createitem-operation-email-message.md)
  
[CreateItem operation，（会议请求）](createitem-operation-meeting-request.md)
  
[CreateItem operation，（任务）](createitem-operation-task.md)
  
 **CreateItemType**

