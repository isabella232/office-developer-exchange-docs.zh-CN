---
title: 任务
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Task
api_type:
- schema
ms.assetid: 7c84927e-db28-4c5d-b0b5-cbcc2b88d869
description: Task 元素表示任务存储Exchange任务。
ms.openlocfilehash: 1a9d44480ec92c9adf158e7e71cf3f928b20b64d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544519"
---
# <a name="task"></a>任务

**Task** 元素表示任务存储Exchange任务。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |包含以 base64Binary (表示) 对象的 MIME 流中的本机多用途 Internet 邮件扩展。  <br/> |
|[ItemId](itemid.md) <br/> |包含项目在项目存储中的唯一标识符Exchange项。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含项目或文件夹的父文件夹的标识符。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的邮件类。  <br/> |
|[主题](subject.md) <br/> |表示用于存储Exchange响应对象的主题。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |包含项目的敏感度状态。  <br/> |
|[正文](body.md) <br/> |表示邮件的实际正文内容。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含附加到项目存储中的项目或Exchange文件。  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |表示接收邮箱中的项目的日期和时间。  <br/> |
|[尺寸](size.md) <br/> |表示项目的大小（以字节为单位）。 此属性是只读的。  <br/> |
|[Categories](categories-ex15websvcsotherref.md) <br/> |表示标识邮箱中项目属于哪些类别的字符串集合。  <br/> |
|[Importance](importance.md) <br/> |描述项目的重要性。  <br/> |
|[InReplyTo](inreplyto.md) <br/> |表示此项是答复项的标识符。  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |指示项目是否已提交到发件箱默认文件夹。  <br/> |
|[IsDraft](isdraft.md) <br/> |表示项目尚未发送。  <br/> |
|[IsFromMe](isfromme.md) <br/> |指示用户是否向自己发送了项目。  <br/> |
|[IsResend](isresend.md) <br/> |指示项目先前是否已发送。  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |指示项目是否已修改。  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |表示包含在邮箱中的项目的所有 Internet 邮件头的集合。  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |表示邮箱中项目的发送日期和时间。  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |表示邮箱中给定项目的创建日期和时间。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与项目存储中的项目关联的所有响应Exchange的集合。  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |表示事件发生的日期和时间。 [ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此功能来确定何时显示提醒。  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |指示是否已为应用商店中的项目设置Exchange提醒。  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |表示在显示提醒时事件前的分钟数。  <br/> |
|[DisplayCc](displaycc.md) <br/> |表示用于"抄送"框内容的显示字符串。 这是所有"抄送"收件人显示名称的串联字符串。  <br/> |
|[DisplayTo](displayto.md) <br/> |表示用于"To"框内容的显示字符串。 这是所有"收件人"收件人显示名称的串联字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示一个属性 **，如果项目** 具有至少一个可见附件，则该属性设置为 true。 此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项目的扩展属性。  <br/> |
|[Culture](culture.md) <br/> |表示邮箱中给定项目的区域性。  <br/> |
|[ActualWork](actualwork.md) <br/> |表示在任务上花费的实际时间量。  <br/> |
|[AssignedTime](assignedtime.md) <br/> |表示任务分配给联系人的时间。  <br/> |
|[BillingInformation](billinginformation.md) <br/> |保存任务的计费信息。  <br/> |
|[ChangeCount](changecount.md) <br/> |指定任务的版本。  <br/> |
|[Companies](companies.md) <br/> |表示与联系人或任务关联的公司的集合。  <br/> |
|[CompleteDate](completedate.md) <br/> |表示任务的完成日期。  <br/> |
|[联系人](contacts-ex15websvcsotherref.md) <br/> |包含与任务关联的联系人列表。  <br/> |
|[DelegationState](delegationstate.md) <br/> |表示委派任务的状态。  <br/> |
|[Delegator](delegator.md) <br/> |包含分配了任务的委派者的名称。  <br/> |
|[DueDate](duedate.md) <br/> |表示任务项到期的日期。  <br/> |
|[IsAssignmentEditable](isassignmenteditable.md) <br/> |指示任务是否可编辑。  <br/> |
|[IsComplete](iscomplete.md) <br/> |指示任务是否已完成。  <br/> |
|[IsRecurring](isrecurring.md) <br/> |指示任务是否是定期项目的一部分。 此元素是只读的。  <br/> |
|[IsTeamTask](isteamtask.md) <br/> |指示任务是否归团队所有。  <br/> |
|[Mileage](mileage.md) <br/> |表示任务项的里程。  <br/> |
|[Owner](owner.md) <br/> |表示任务的所有者。  <br/> |
|[PercentComplete](percentcomplete.md) <br/> |描述任务的完成状态。  <br/> |
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |包含定期任务的定期信息。  <br/> |
|[StartDate](startdate.md) <br/> |表示任务项目的开始日期。  <br/> |
|[状态](status.md) <br/> |表示任务项的状态。  <br/> |
|[StatusDescription](statusdescription.md) <br/> |包含任务状态的说明。  <br/> |
|[TotalWork](totalwork.md) <br/> |包含与项目关联的工作数的说明。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含基于项目或文件夹的权限设置的客户端权限。 此元素是只读的。  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |包含显示名称用户修改项目的详细信息。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |指示项目的上次修改时间。  <br/> |
|[IsAssociated](isassociated.md) <br/> |指示项目是否与文件夹关联。  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |表示连接到 Web App 终结点以读取Microsoft Office Outlook Web App 终结点的 URL Outlook Web App。  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |表示要连接到 Outlook Web App 终结点以编辑项目在Outlook Web App。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含项目或对话的标识符。  <br/> |
|[UniqueBody](uniquebody.md) <br/> |表示 HTML 片段或纯文本，表示此对话的唯一正文。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |描述与会议时间相邻的所有日历项目。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识要追加到 [UpdateItem](updateitem-operation.md)操作期间项目/文件夹的单个属性的数据。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目。  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |标识要在本地客户端存储中创建的单个项目。  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |代表Exchange附加到其他项目的项目Exchange项。  <br/> |
|[Items](items.md) <br/> |包含项目数组。  <br/> |
|[SetItemField](setitemfield.md) <br/> |表示对 [UpdateItem](updateitem-operation.md)操作中某个项目的单个属性的更新。  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |标识要在本地客户端存储中更新的单个项目。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [创建任务](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
- [删除任务](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

