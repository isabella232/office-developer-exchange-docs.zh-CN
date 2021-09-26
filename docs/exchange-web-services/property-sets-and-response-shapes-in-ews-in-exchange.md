---
title: 属性集和响应形状在 EWS 在 Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 04a29804-6067-48e7-9f5c-534e253a230e
description: 了解如何管理 EWS 托管 API 和 EWS 在 Exchange 中返回的响应形状和属性Exchange。
ms.openlocfilehash: 7720a07a6fd288f289bba371ce6fd8a6e349a8ce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543847"
---
# <a name="property-sets-and-response-shapes-in-ews-in-exchange"></a>属性集和响应形状在 EWS 在 Exchange

了解如何管理 EWS 托管 API 和 EWS 在 Exchange 中返回的响应形状和属性Exchange。
  
数据Exchange提供了灵活的存储解决方案，使您可以将不同的项目（如联系人和日历条目）存储在同一文件夹中;但是，它可能会很难管理从调用 EWS 操作或 EWS 托管 API 方法返回的数据。
  
为了便于管理 Exchange Online、Exchange Online 作为 Office 365 的一部分或自 Exchange 2013 起 Excahange 版本返回的数据，EWS 托管 API 使用属性集，EWS 使用响应形状。 这些是提供存储项的最常见属性的预定义集合。 返回的属性集由项目类型决定。 这意味着，在使用托管 API [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) Exchange绑定项时，将获取一组不同的属性，具体取决于要绑定到的项目的类型。 绑定到日历项目将返回一组与绑定到联系人项目不同的属性。 同样，如果使用的是 [EWS，GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) 操作将基于返回的项目类型返回一组不同的属性。 
  
使用 [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) 方法或 [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) 操作绑定到文件夹也会根据请求的文件夹返回不同的属性集。 
  
**表 1.预定义的响应形状**

|**响应形状**|**EWS 托管 API 等效项**|**说明**|
|:-----|:-----|:-----|
|仅 ID  <br/> |[BasePropertySet.IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |仅返回项目或文件夹的标识符。 大多数应用程序都应使用此响应形状并指定所需的任何其他属性。  <br/> |
|默认值  <br/> |不适用  <br/> |返回一组预定义的属性，这些属性是项目或文件夹的默认设置 (EWS) 。  <br/> |
|所有属性  <br/> |[BasePropertySet.FirstClassProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |返回客户端应用程序最常用的属性。 可以使用属性路径返回其他属性。  <br/> |
   
## <a name="default-response-shapes"></a>默认响应形状

EWS 包括文件夹和项目的默认响应形状集。 
  
下表列出了 [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) 和 [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) EWS 操作返回的每个文件夹的默认属性。 
  
**表 2.默认文件夹属性**

|**Property**|**收件箱**|**日历**|**联系人**|**已删除项目**|**草稿**|**注意**|**其他文件夹**|**发件箱**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|显示名称  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|文件夹 ID  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|子文件夹计数  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|总计数  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|未读计数  <br/> |X  <br/> |||X  <br/> |X  <br/> ||X  <br/> |X  <br/> |
   
下表列出了 [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) 和 [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS 操作为每个项目类型返回的默认属性。 
  
**表 3.默认项目属性**

|**Property**|**日历项目**|**联系人项目**|**邮件项目**|**任务项目**|
|:-----|:-----|:-----|:-----|:-----|
|正文  <br/> |||X (1)   <br/> ||
|CalendarItemType  <br/> ||x  <br/> |||
|CompanyName  <br/> ||x  <br/> |||
|CompleteName  <br/> ||x  <br/> |||
|DateTimeCreated  <br/> |||x  <br/> ||
|DateTimeSent  <br/> |||x  <br/> ||
|DueDate  <br/> ||||x (2)   <br/> |
|EmailAddresses  <br/> ||x  <br/> |||
|End  <br/> |x  <br/> ||||
|FileAs  <br/> ||x  <br/> |||
|发件人  <br/> |||x  <br/> ||
|HasAttachments  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ImAddresses  <br/> ||x  <br/> |||
|IsAssociated  <br/> |x  <br/> ||x  <br/> ||
|IsDeliveryReceiptRequested  <br/> |||x  <br/> ||
|ItemId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|JobTitle  <br/> ||x  <br/> |||
|LegacyFreeBusyStatus  <br/> |x  <br/> ||||
|位置  <br/> |x  <br/> ||||
|组织者  <br/> |x  <br/> ||||
|PercentComplete  <br/> ||||x  <br/> |
|PhoneNumbers  <br/> ||x  <br/> |||
|PhysicalAddresses  <br/> ||x  <br/> |||
|ResponseObjects  <br/> |x (1)   <br/> ||x (1)   <br/> ||
|Sensitity  <br/> |||x  <br/> ||
|Size  <br/> |||x  <br/> ||
|StartDate  <br/> ||||x (2)   <br/> |
|状态  <br/> ||||x  <br/> |
|主题  <br/> |x  <br/> ||x  <br/> |x  <br/> |
   
注意：
  
1. 包含在 **GetItem** 操作的响应中。 未包含在 **FindItem** 操作的响应中。 
    
2. 仅在字段包含数据时包含在响应中。 如果字段为空，则不包括在响应中。
    
### <a name="all-properties-set-and-response-shape"></a>所有属性集和响应形状

下表列出了通过调用 EWS 托管 API [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) 和 [Item.FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) EWS 托管 API 方法返回的一类属性，以及 [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) 和 [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS 操作返回的"所有属性"响应形状。 
  
可以将其他属性添加到属性集或包括扩展属性。 有关详细信息，请参阅[EWS 中的属性和扩展Exchange。](properties-and-extended-properties-in-ews-in-exchange.md)
  
**表 4.一级属性**

|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
|属性  <br/> |日历项目  <br/> |联系人项目  <br/> |邮件项目  <br/> |Post 项  <br/> |任务项目  <br/> |
|ActualWork  <br/> |||||x  <br/> |
|AdjacentMeetingCount  <br/> |x  <br/> |||||
|AdjacentMeetings  <br/> |x  <br/> |||||
|Alias  <br/> ||x  <br/> ||||
|AllowNewTimeProposal  <br/> |x  <br/> |||||
|AppointmentReplyTime  <br/> |x  <br/> |||||
|AppointmentSequenceNumber  <br/> |x  <br/> |||||
|AppointmentState  <br/> |x  <br/> |||||
|AssignedTime  <br/> |||||x  <br/> |
|AssistantName  <br/> ||x  <br/> ||||
|BccRecipients  <br/> |||x  <br/> |||
|BillingInformation  <br/> |||||x  <br/> |
|正文  <br/> |x (1)   <br/> |x (1)   <br/> |x (1)   <br/> ||x (1)   <br/> |
|BusinessHomePage  <br/> ||x  <br/> |x  <br/> |||
|CalendarItemType  <br/> |x  <br/> |||||
|类别  <br/> |x  <br/> ||x  <br/> |x  <br/> |x  <br/> |
|CcRecipients  <br/> |||x  <br/> |||
|ChangeCount  <br/> |||||x  <br/> |
|Children  <br/> ||x  <br/> ||||
|Companies  <br/> |||||x  <br/> |
|CompleteDate  <br/> |||||x  <br/> |
|CompleteName  <br/> ||x  <br/> ||||
|ConferenceType  <br/> |x  <br/> |||||
|ConflictingMeetingCount  <br/> |x  <br/> |||||
|ConflictingMeetings  <br/> |x  <br/> |||||
|联系人  <br/> |||||x  <br/> |
|ContactSource  <br/> ||x  <br/> ||||
|ConversationId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ConversationIndex  <br/> |||x  <br/> |x  <br/> ||
|ConversationTopic  <br/> |||x  <br/> |x  <br/> ||
|Culture  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeCreated  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeReceived  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeSent  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeStamp  <br/> |x  <br/> |||||
|DelegationState  <br/> |||||x  <br/> |
|Delegator  <br/> |||||x  <br/> |
|DeletedOccurrences  <br/> |x  <br/> |||||
|部门  <br/> ||x  <br/> ||||
|DirectoryId  <br/> ||x  <br/> ||||
|DirectReports  <br/> ||x  <br/> ||||
|DisplayCc  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DisplayName  <br/> ||x  <br/> ||||
|DisplayTo  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DueDate  <br/> |||||x  <br/> |
|期限  <br/> |x  <br/> |||||
|EffectiveRights  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|EmailAddresses  <br/> ||x  <br/> ||||
|End  <br/> |x  <br/> |||||
|EndTimeZone  <br/> |x  <br/> |||||
|FileAs  <br/> ||x  <br/> ||||
|FileAsMapping  <br/> ||x  <br/> ||||
|FirstOccurrence  <br/> |x  <br/> |||||
|发件人  <br/> |||x  <br/> |x  <br/> ||
|Generation  <br/> ||x  <br/> ||||
|GivenName  <br/> ||x  <br/> ||||
|HasAttachments  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|HasPicture  <br/> ||x  <br/> ||||
|ImAddresses  <br/> ||x  <br/> ||||
|Importance  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Initials  <br/> ||x  <br/> ||||
|InReplyTo  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|InternetMessageId  <br/> |||x  <br/> |x  <br/> ||
|InternetMessageHeaders  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsAllDayEvent  <br/> |x  <br/> |||||
|IsAssociated  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsCancelled  <br/> |x  <br/> |||||
|IsComplete  <br/> |||||x  <br/> |
|IsDeliveryReceiptRequested  <br/> |||x  <br/> |||
|IsDraft  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsFromMe  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsMeeting  <br/> |x  <br/> |||||
|IsOnlineMeeting  <br/> |x  <br/> |||||
|IsRead  <br/> |||x  <br/> |||
|IsReadReceiptRequested  <br/> |||x  <br/> |||
|IsRecurring  <br/> |x  <br/> ||||x  <br/> |
|IsResend  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsResponseRequested  <br/> |x  <br/> ||x  <br/> |||
|IsSubmitted  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsUnmodified  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ItemClass  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ItemId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|JobTitle  <br/> ||x  <br/> ||||
|LastModifiedName  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|LastModifiedTime  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|LastOccurrance  <br/> |x  <br/> |||||
|LegacyFreeBusyStatus  <br/> |x  <br/> |||||
|位置  <br/> |x  <br/> |||||
|Manager  <br/> ||x  <br/> ||||
|MeetingRequestWasSent  <br/> |x  <br/> |||||
|MeetingTimeZone  <br/> |x  <br/> |||||
|MeetingWorkspaceUrl  <br/> |x  <br/> |||||
|MiddleName  <br/> ||x  <br/> ||||
|Mileage  <br/> ||x  <br/> |||x  <br/> |
|ModifiedOccurrances  <br/> |x  <br/> |||||
|MyResponseType  <br/> |x  <br/> |||||
|NetShowUrl  <br/> |x  <br/> |||||
|NickName  <br/> ||x  <br/> ||||
|注释  <br/> ||x  <br/> ||||
|OfficeLocation  <br/> ||x  <br/> ||||
|OptionalAttendees  <br/> |x  <br/> |||||
|组织者  <br/> |x  <br/> |||||
|OriginalStart  <br/> |x  <br/> |||||
|所有者  <br/> |||||x  <br/> |
|ParentFolderId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|PercentComplete  <br/> |||||x  <br/> |
|PhoneNumbers  <br/> ||x  <br/> ||||
|PhoneticFirstName  <br/> ||x  <br/> ||||
|PhoneticFullName  <br/> ||x  <br/> ||||
|PhoneticLastName  <br/> ||x  <br/> ||||
|Photo  <br/> ||x  <br/> ||||
|PhysicalAddresses  <br/> ||x  <br/> ||||
|PostalAddressIndex  <br/> ||x  <br/> ||||
|PostedTime  <br/> ||||x  <br/> ||
|Profession  <br/> ||x  <br/> ||||
|ReceivedBy  <br/> |||x  <br/> |||
|ReceivedRepresenting  <br/> |||x  <br/> |||
|Reccurrence  <br/> |x  <br/> ||||x  <br/> |
|参考  <br/> |||x  <br/> |x  <br/> ||
|ReminderDueBy  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderIsSet  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderMinutesBeforeStart  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReplyTo  <br/> |||x  <br/> |||
|RequiredAttendees  <br/> |x  <br/> |||||
|资源  <br/> |x  <br/> |||||
|ResponseObjects  <br/> |x (1)   <br/> |x (1)   <br/> |x (1)   <br/> |x (1)   <br/> |x (1)   <br/> |
|发件人  <br/> |||x  <br/> |x  <br/> ||
|敏感度  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Size  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|SpouseName  <br/> ||x  <br/> ||||
|开始  <br/> |x  <br/> |||||
|StartDate  <br/> |||||x  <br/> |
|StartTimeZone  <br/> |x  <br/> |||||
|状态  <br/> |||||x  <br/> |
|StatusDescription  <br/> |||||x  <br/> |
|主题  <br/> |x  <br/> |x  <br/> |x  <br/> ||x  <br/> |
|Surname  <br/> ||x  <br/> ||||
|TimeZone  <br/> |x  <br/> |||||
|ToRecipients  <br/> |||x  <br/> |||
|TotalWork  <br/> |||||x  <br/> |
|WebClientEditFormQueryString  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|WebClientReadFormQueryString  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
   
注意：
  
1. 在 [绑定到项时和](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)操作的响应中包含 。 未包括在 [Item.FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) 方法的结果或 [FindItem 操作的响应中](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)。
    
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [GetItem 操作](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)
    
- [FindFolder 操作](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [GetFolder Operation](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)
    

