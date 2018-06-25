---
title: 联系人
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contact
api_type:
- schema
ms.assetid: 66bfff50-7a91-4d81-b6a0-610b9962f677
description: 联系人元素表示 Exchange 存储中的联系人项目。
ms.openlocfilehash: 7b2e7c0197914c2a0a0ba3815dd05fca52a5f872
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753499"
---
# <a name="contact"></a>联系人

**联系人**元素表示 Exchange 存储中的联系人项目。 
  
```XML
<Contact>
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
   <Importance/>
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
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
   <FileAs/>
   <FileAsMapping/>
   <DisplayName/>
   <GivenName/>
   <Initials/>
   <MiddleName/>
   <Nickname/>
   <CompleteName/>
   <CompanyName/>
   <EmailAddresses/>
   <PhysicalAddresses/>
   <PhoneNumbers/>
   <AssistantName/>
   <Birthday/>
   <BusinessHomePage/>
   <Children/>
   <Companies/>
   <ContactSource/>
   <Department/>
   <Generation/>
   <ImAddresses/>
   <JobTitle/>
   <Manager/>
   <Mileage/>
   <OfficeLocation/>
   <PostalAddressIndex/>
   <Profession/>
   <SpouseName/>
   <Surname/>
   <WeddingAnniversary/>
   <HasPicture/>
   <PhoneticFullName/>
   <PhoneticFirstName/>
   <PhoneticLastName/>
   <Alias/>
   <Notes/>
   <Photo/>
   <UserSMIMECertificate/>
   <MSExchangeCertificate/>
   <DirectoryId/>
   <ManagerMailbox/>
   <DirectReports/>
</Contact>
```

 **ContactItemType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素名**|**说明**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |包含一个对象，表示 base64Binary 格式的本机多用途 Internet 邮件扩展 (MIME) 流。  <br/> |
|[ItemId](itemid.md) <br/> |包含在 Exchange 存储中的项目的唯一标识符和更改的键。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含的项目或文件夹的父文件夹的标识符。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的消息类。  <br/> |
|[Subject](subject.md) <br/> |代表 Exchange 存储项和响应对象主题。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示项目的敏感度级别。  <br/> |
|[Body](body.md) <br/> |表示一条消息的实际正文内容。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含的项或附加到 Exchange 存储中的项目文件。  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |表示的日期和接收邮箱中的项目的时间。  <br/> |
|[Size](size.md) <br/> |表示以字节为单位的项目的大小。 此属性是只读的。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |表示标识的邮箱中项目所属的类别的字符串的集合。  <br/> |
|[Importance](importance.md) <br/> |描述项目的重要性。  <br/> |
|[InReplyTo](inreplyto.md) <br/> |表示此项将答复到项目的标识符。  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |指示项目是否已提交到默认发件箱文件夹。  <br/> |
|[IsDraft](isdraft.md) <br/> |表示是否尚未发送项目。  <br/> |
|[IsFromMe](isfromme.md) <br/> |指示用户是否发送给自己的项目。  <br/> |
|[IsResend](isresend.md) <br/> |指示是否已以前被发送项目。  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |指示是否已修改项目。  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |代表在邮箱中某个项目中包含的所有 Internet 邮件头的集合。  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |表示的日期和时间发送邮箱中的项目。  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |表示的日期和给定的邮箱中项目的创建时间。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与 Exchange 存储中的项相关联的所有响应对象的集合。  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |表示的日期和时间事件发生。 这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |指示是否已设置提醒的项在 Exchange 存储中。  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |表示事件时显示提醒前的分钟数。  <br/> |
|[DisplayCc](displaycc.md) <br/> |表示用于 Cc 行的内容显示字符串。 这是连接的所有抄送收件人的显示名称的字符串。  <br/> |
|[DisplayTo](displayto.md) <br/> |表示用于 To 行的内容显示字符串。 这是连接的所有收件人的显示名称的字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示如果项目具有至少一个可见的附件设置为**true**的属性。 此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项扩展的属性。  <br/> |
|[区域性](culture.md) <br/> |表示给定邮箱中项目的区域性。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |包含要修改的项目的最后一个用户的显示名称。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |指示上次修改的项。  <br/> |
|[IsAssociated](isassociated.md) <br/> |指示项目是否与文件夹关联。  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含项目或会话的标识符。  <br/> |
|[UniqueBody](uniquebody.md) <br/> |代表一个 HTML 片段或代表此对话的唯一正文的纯文本。  <br/> |
|[FileAs](fileas.md) <br/> |代表联系人联系人文件夹中的存档的方式。  <br/> |
|[FileAsMapping](fileasmapping.md) <br/> |定义如何构造联系人显示的内容。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |定义一个联系人的显示名称。  <br/> |
|[GivenName](givenname.md) <br/> |包含联系人的名字。  <br/> |
|[首字母缩写](initials.md) <br/> |代表联系人的姓名缩写。  <br/> |
|[MiddleName](middlename.md) <br/> |代表中间名的联系人。  <br/> |
|[昵称](nickname.md) <br/> |代表联系人的别名。  <br/> |
|[CompleteName](completename.md) <br/> |表示某个联系人的完整名称。  <br/> |
|[公司名称](companyname.md) <br/> |表示与联系人关联的公司名称。  <br/> |
|[EmailAddresses](emailaddresses.md) <br/> |表示一个联系人的电子邮件地址的集合。  <br/> |
|[PhysicalAddresses](physicaladdresses.md) <br/> |包含与联系人关联的物理地址的集合。  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |表示联系人的电话号码的集合。  <br/> |
|[AssistantName](assistantname.md) <br/> |向联系人代表助理。  <br/> |
|[生日](birthday.md) <br/> |表示联系人出生日期。  <br/> |
|[BusinessHomePage](businesshomepage.md) <br/> |代表联系人主页上 （Web 地址）。  <br/> |
|[子女](children.md) <br/> |包含联系人的子级的名称。  <br/> |
|[公司](companies.md) <br/> |代表与联系人关联的公司的集合。  <br/> |
|[ContactSource](contactsource.md) <br/> |描述联系人是否位于 Exchange 存储或 Active Directory 目录服务。  <br/> |
|[部门](department.md) <br/> |代表在工作场所的联系人所在的部门。  <br/> |
|[生成](generation.md) <br/> |代表代缩写的联系人的完整名称。  <br/> |
|[ImAddresses](imaddresses.md) <br/> |表示一个联系人的即时消息地址的集合。  <br/> |
|[JobTitle](jobtitle.md) <br/> |代表联系人的职务。  <br/> |
|[Manager](manager.md) <br/> |代表联系人管理器。  <br/> |
|[里程](mileage.md) <br/> |代表为联系人项 mileage。  <br/> |
|[OfficeLocation](officelocation.md) <br/> |代表联系人的办公室位置。  <br/> |
|[PostalAddressIndex](postaladdressindex.md) <br/> |表示物理地址的显示类型。  <br/> |
|[Profession](profession.md) <br/> |代表联系人的职业。  <br/> |
|[配偶姓名](spousename.md) <br/> |表示联系人的配偶的名称。  <br/> |
|[姓](surname.md) <br/> |代表联系人的姓。  <br/> |
|[WeddingAnniversary](weddinganniversary.md) <br/> |包含联系人的婚礼周年的日。  <br/> |
|[HasPicture](haspicture.md) <br/> |指示联系人项目是否有代表联系人的图片的文件附件。  <br/> |
|[PhoneticFullName](phoneticfullname.md) <br/> |包含一个联系人，包括第一个和最后一个名称，按发音拼写的完整名称。  <br/> |
|[PhoneticFirstName](phoneticfirstname.md) <br/> |包含名的联系人，按发音拼写。  <br/> |
|[PhoneticLastName](phoneticlastname.md) <br/> |包含最后一个联系人的姓名，拼写发音排序。  <br/> |
|[Alias](alias.md) <br/> |包含联系人的电子邮件别名。  <br/> |
|[备注 （联系人）](notes-contact.md) <br/> |包含联系人的补充信息。  <br/> |
|[照片](photo.md) <br/> |包含一个值，它将编码的联系人的照片。  <br/> |
|[UserSMIMECertificate](usersmimecertificate.md) <br/> |包含一个值，它将编码的联系人的 SMIME 证书。  <br/> |
|[MSExchangeCertificate](msexchangecertificate.md) <br/> |包含一个值，它将编码的联系人的 Microsoft Exchange 证书。  <br/> |
|[DirectoryId](directoryid.md) <br/> |包含目录 ID 的联系人。  <br/> |
|[ManagerMailbox](managermailbox.md) <br/> |包含标识的联系人管理器邮箱的 SMTP 信息。  <br/> |
|[DirectReports](directreports.md) <br/> |包含标识联系人的直接下属的 SMTP 信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素名**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |介绍所有彼此相邻的会议时间的日历项目。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识要[UpdateItem 操作](updateitem-operation.md)期间追加到单个项目或文件夹的属性数据。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目  <br/> |
|[创建 (ItemSync)](create-itemsync.md) <br/> |标识要在本地客户端存储中创建一个文件夹。  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |代表附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[Items](items.md) <br/> |包含项的数组。  <br/> |
|[项目 (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。  <br/> |
|[解决方法](resolution.md) <br/> |包含单个已解析的实体。  <br/> |
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


[Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[更新联系人](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[删除联系人](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

