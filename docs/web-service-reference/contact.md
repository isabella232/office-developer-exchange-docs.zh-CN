---
title: Contact
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
description: Contact 元素表示 Exchange 存储中的联系人项目。
ms.openlocfilehash: b5b4af211815dbbd09449ca2f3c6b6b2dfba6f93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44445648"
---
# <a name="contact"></a>Contact

**Contact**元素表示 Exchange 存储中的联系人项目。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素名**|**说明**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。  <br/> |
|[ItemId](itemid.md) <br/> |包含 Exchange 存储中某项的唯一标识符和更改键。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含项或文件夹的父文件夹的标识符。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的邮件类。  <br/> |
|[主题](subject.md) <br/> |表示 Exchange 存储项和响应对象的主题。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示项的敏感度级别。  <br/> |
|[Body](body.md) <br/> |表示邮件的实际正文内容。  <br/> |
|[附件](attachments-ex15websvcsotherref.md) <br/> |包含附加到 Exchange 存储中的项目的项目或文件。  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |表示邮箱中的项目的接收日期和时间。  <br/> |
|[大小](size.md) <br/> |表示项的大小（以字节为单位）。 此属性是只读的。  <br/> |
|[类别](categories-ex15websvcsotherref.md) <br/> |表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。  <br/> |
|[Importance](importance.md) <br/> |介绍项的重要性。  <br/> |
|[InReplyTo](inreplyto.md) <br/> |表示此项是其回复项的标识符。  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |指示是否已将项目提交到 "发件箱" 默认文件夹。  <br/> |
|[IsDraft](isdraft.md) <br/> |表示是否尚未发送某个项目。  <br/> |
|[IsFromMe](isfromme.md) <br/> |指示用户是否向自己发送了一个项目。  <br/> |
|[IsResend](isresend.md) <br/> |指示以前是否已发送过该项目。  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |指示项目是否已被修改。  <br/> |
|[Message](internetmessageheaders.md) <br/> |表示邮箱中的项目所包含的所有 Internet 邮件头的集合。  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |表示邮箱中的项目的发送日期和时间。  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |表示邮箱中的给定项目的创建日期和时间。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与 Exchange 存储中的项目关联的所有响应对象的集合。  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |表示事件发生的日期和时间。 [ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |指示是否已为 Exchange 存储中的某个项目设置提醒。  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |表示在显示提醒时事件之前的分钟数。  <br/> |
|[DisplayCc](displaycc.md) <br/> |代表用于 "抄送" 行内容的显示字符串。 这是所有 Cc 收件人显示名称的串联字符串。  <br/> |
|[DisplayTo](displayto.md) <br/> |表示用于 "To" 行的内容的显示字符串。 这是所有收件人显示名称的串联字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。 此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项的扩展属性。  <br/> |
|[Culture](culture.md) <br/> |表示邮箱中给定项目的区域性。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |包含上次修改项目的用户的显示名称。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |指示项目的上次修改时间。  <br/> |
|[IsAssociated](isassociated.md) <br/> |指示项目是否与文件夹相关联。  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中编辑项目的 URL。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含项或对话的标识符。  <br/> |
|[UniqueBody](uniquebody.md) <br/> |表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。  <br/> |
|[FileAs](fileas.md) <br/> |表示联系人在 "联系人" 文件夹中的存档方式。  <br/> |
|[FileAsMapping](fileasmapping.md) <br/> |定义如何构建联系人的显示内容。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |定义联系人的显示名称。  <br/> |
|[GivenName](givenname.md) <br/> |包含联系人的名称。  <br/> |
|[缩写](initials.md) <br/> |代表联系人的缩写。  <br/> |
|[MiddleName](middlename.md) <br/> |表示联系人的中间名。  <br/> |
|[昵称](nickname.md) <br/> |表示联系人的昵称。  <br/> |
|[CompleteName](completename.md) <br/> |表示某个联系人的完整名称。  <br/> |
|[CompanyName](companyname.md) <br/> |表示与联系人关联的公司名称。  <br/> |
|[EmailAddresses](emailaddresses.md) <br/> |表示联系人的电子邮件地址的集合。  <br/> |
|[PhysicalAddresses](physicaladdresses.md) <br/> |包含与联系人关联的物理地址的集合。  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |表示联系人的电话号码的集合。  <br/> |
|[AssistantName](assistantname.md) <br/> |表示联系人的助理。  <br/> |
|[生日](birthday.md) <br/> |表示联系人的出生日期。  <br/> |
|[BusinessHomePage](businesshomepage.md) <br/> |表示联系人的主页（Web 地址）。  <br/> |
|[子女](children.md) <br/> |包含联系人子女的姓名。  <br/> |
|[Companies](companies.md) <br/> |表示与联系人关联的公司的集合。  <br/> |
|[ContactSource](contactsource.md) <br/> |描述联系人是否位于 Exchange 存储或 Active Directory 目录服务中。  <br/> |
|[Department](department.md) <br/> |代表工作中联系人的部门。  <br/> |
|[生成](generation.md) <br/> |代表联系人的全名后面的代缩写。  <br/> |
|[ImAddresses](imaddresses.md) <br/> |表示联系人的即时消息地址的集合。  <br/> |
|[JobTitle](jobtitle.md) <br/> |表示联系人的职务。  <br/> |
|[Manager](manager.md) <br/> |表示联系人的经理。  <br/> |
|[Mileage](mileage.md) <br/> |表示联系人项目的里程。  <br/> |
|[OfficeLocation](officelocation.md) <br/> |表示联系人的办公室位置。  <br/> |
|[PostalAddressIndex](postaladdressindex.md) <br/> |表示物理地址的显示类型。  <br/> |
|[职业](profession.md) <br/> |表示联系人的职业。  <br/> |
|[SpouseName](spousename.md) <br/> |表示联系人配偶/伴侣的名称。  <br/> |
|[姓氏](surname.md) <br/> |表示联系人的姓氏。  <br/> |
|[WeddingAnniversary](weddinganniversary.md) <br/> |包含联系人的婚礼周年纪念。  <br/> |
|[HasPicture](haspicture.md) <br/> |指示联系人项目是否具有表示联系人图片的文件附件。  <br/> |
|[PhoneticFullName](phoneticfullname.md) <br/> |包含联系人的全名，包括名字和姓氏（按发音拼写）。  <br/> |
|[PhoneticFirstName](phoneticfirstname.md) <br/> |包含按发音拼写的联系人的第一个名称。  <br/> |
|[PhoneticLastName](phoneticlastname.md) <br/> |包含按发音拼写的联系人的姓氏。  <br/> |
|[Alias](alias.md) <br/> |包含联系人的电子邮件别名。  <br/> |
|[注释（联系人）](notes-contact.md) <br/> |包含附属联系人信息。  <br/> |
|[照片](photo.md) <br/> |包含对联系人的照片进行编码的值。  <br/> |
|[UserSMIMECertificate](usersmimecertificate.md) <br/> |包含对联系人的 SMIME 证书进行编码的值。  <br/> |
|[MSExchangeCertificate](msexchangecertificate.md) <br/> |包含对联系人的 Microsoft Exchange 证书进行编码的值。  <br/> |
|[DirectoryId](directoryid.md) <br/> |包含联系人的目录 ID。  <br/> |
|[ManagerMailbox](managermailbox.md) <br/> |包含标识联系人的经理邮箱的 SMTP 信息。  <br/> |
|[DirectReports](directreports.md) <br/> |包含标识联系人的直接下属的 SMTP 信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素名**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |介绍与会议时间相邻的所有日历项目。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项或文件夹的单个属性的数据。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项  <br/> |
|[创建（ItemSync）](create-itemsync.md) <br/> |标识要在本地客户端存储中创建一个文件夹。  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |表示附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[Items](items.md) <br/> |包含项的数组。  <br/> |
|[项目（NonEmptyArrayOfAllItemsType）](items-nonemptyarrayofallitemstype.md) <br/> |包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。  <br/> |
|[解决方法](resolution.md) <br/> |包含单个已解析的实体。  <br/> |
|[SetItemField](setitemfield.md) <br/> |表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。  <br/> |
|[Update （ItemSync）](update-itemsync.md) <br/> |标识要在本地客户端存储中更新的单个项目。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

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


[创建联系人（Exchange Web 服务）](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[更新联系人](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[删除联系人](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

