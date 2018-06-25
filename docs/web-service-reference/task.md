---
title: 任务
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Task
api_type:
- schema
ms.assetid: 7c84927e-db28-4c5d-b0b5-cbcc2b88d869
description: Task 元素表示 Exchange 存储中的任务。
ms.openlocfilehash: 2c61fca6ac85290e34f1365b0cb9e841e1fe279f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838191"
---
# <a name="task"></a>任务

**Task**元素表示 Exchange 存储中的任务。 
  
```xml
<Task>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <ActualWork/>
   <AssignedTime/>
   <BillingInformation/>
   <ChangeCount/>
   <Companies/>
   <CompleteDate/>
   <Contacts/>
   <DelegationState/>
   <Delegator/>
   <DueDate/>
   <IsAssignmentEditable/>
   <IsComplete/>
   <IsRecurring/>
   <IsTeamTask/>
   <Mileage/>
   <Owner/>
   <PercentComplete/>
   <Recurrence/>
   <StartDate/>
   <Status/>
   <StatusDescription/>
   <TotalWork/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</Task>
```

**TaskType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |包含一个对象，表示 base64Binary 格式的本机多用途 Internet 邮件扩展 (MIME) 流。  <br/> |
|[ItemId](itemid.md) <br/> |包含在 Exchange 存储中的项目的唯一标识符和更改的键。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含的项目或文件夹的父文件夹的标识符。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的消息类。  <br/> |
|[Subject](subject.md) <br/> |代表 Exchange 存储项和响应对象主题。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |包含项目的敏感度的状态。  <br/> |
|[Body](body.md) <br/> |表示一条消息的实际正文内容。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含的项或附加到 Exchange 存储中的项目文件。  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |表示的日期和接收邮箱中的项目的时间。  <br/> |
|[Size](size.md) <br/> |表示的大小，以字节为单位的项目。 此属性是只读的。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |表示标识的邮箱中项目所属的类别的字符串的集合。  <br/> |
|[Importance](importance.md) <br/> |描述项目的重要性。  <br/> |
|[InReplyTo](inreplyto.md) <br/> |表示此项将答复到项目的标识符。  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |指示项目是否已提交到默认发件箱文件夹。  <br/> |
|[IsDraft](isdraft.md) <br/> |表示是否尚未发送项目。  <br/> |
|[IsFromMe](isfromme.md) <br/> |指示用户是否发送到他或她自己的项目。  <br/> |
|[IsResend](isresend.md) <br/> |指示是否已以前被发送项目。  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |指示是否已修改项目。  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |代表在邮箱中某个项目中包含的所有 Internet 邮件头的集合。  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |表示的日期和时间发送邮箱中的项目。  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |表示的日期和给定的邮箱中项目的创建时间。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与 Exchange 存储中的项相关联的所有响应对象的集合。  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |表示的日期和时间事件发生。 这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |指示是否已设置提醒的项在 Exchange 存储中。  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |表示事件时显示提醒前的分钟数。  <br/> |
|[DisplayCc](displaycc.md) <br/> |表示用于抄送框的内容显示字符串。 这是连接的所有抄送收件人的显示名称的字符串。  <br/> |
|[DisplayTo](displayto.md) <br/> |表示用于收件人框的内容显示字符串。 这是连接的所有收件人的显示名称的字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示如果项目具有至少一个可见的附件设置为**true**的属性。 此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项扩展的属性。  <br/> |
|[区域性](culture.md) <br/> |表示给定邮箱中项目的区域性。  <br/> |
|[ActualWork](actualwork.md) <br/> |代表对任务的实际所花费的时间量。  <br/> |
|[AssignedTime](assignedtime.md) <br/> |表示当一个任务分配给联系人的时间。  <br/> |
|[BillingInformation](billinginformation.md) <br/> |保留帐单任务的信息。  <br/> |
|[ChangeCount](changecount.md) <br/> |指定任务的版本。  <br/> |
|[公司](companies.md) <br/> |代表与一个联系人或任务相关联的公司的集合。  <br/> |
|[CompleteDate](completedate.md) <br/> |代表在其完成任务的日期。  <br/> |
|[联系人](contacts-ex15websvcsotherref.md) <br/> |包含与任务相关联的联系人的列表。  <br/> |
|[DelegationState](delegationstate.md) <br/> |代表委派的任务的状态。  <br/> |
|[Delegator](delegator.md) <br/> |包含 delegator 分配任务的名称。  <br/> |
|[DueDate](duedate.md) <br/> |表示任务项目的到期日期。  <br/> |
|[IsAssignmentEditable](isassignmenteditable.md) <br/> |指示任务是否是可编辑。  <br/> |
|[程序](iscomplete.md) <br/> |指示任务是否已完成或未。  <br/> |
|[IsRecurring](isrecurring.md) <br/> |指示任务是否定期项的一部分。 此元素是只读的。  <br/> |
|[IsTeamTask](isteamtask.md) <br/> |指示是否小组拥有任务。  <br/> |
|[里程](mileage.md) <br/> |代表为任务项 mileage。  <br/> |
|[Owner](owner.md) <br/> |表示任务的所有者。  <br/> |
|[完成百分比](percentcomplete.md) <br/> |描述任务的完成状态。  <br/> |
|[定期 (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |包含定期周期性任务信息。  <br/> |
|[StartDate](startdate.md) <br/> |代表任务项目的开始日期。  <br/> |
|[Status](status.md) <br/> |表示任务项的状态。  <br/> |
|[StatusDescription](statusdescription.md) <br/> |包含任务状态的说明。  <br/> |
|[TotalWork](totalwork.md) <br/> |包含多少工作量是与项关联的说明。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端基于的项目或文件夹的权限设置的权限。 此元素是只读的。  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |包含要修改的项目的最后一个用户的显示名称。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |指示上次修改的项。  <br/> |
|[IsAssociated](isassociated.md) <br/> |指示项目是否与文件夹关联。  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含项目或会话的标识符。  <br/> |
|[UniqueBody](uniquebody.md) <br/> |代表一个 HTML 片段或代表此对话的唯一正文的纯文本。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |介绍所有彼此相邻的会议时间的日历项目。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识要追加到的项目/文件夹单个属性[UpdateItem 操作](updateitem-operation.md)期间数据。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目。  <br/> |
|[创建 (ItemSync)](create-itemsync.md) <br/> |标识在本地客户端库中创建的单个项。  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |代表附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[Items](items.md) <br/> |包含项的数组。  <br/> |
|[SetItemField](setitemfield.md) <br/> |表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。  <br/> |
|[更新 (ItemSync)](update-itemsync.md) <br/> |标识要更新本地客户端存储中的单个项。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [创建任务](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
- [删除任务](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

