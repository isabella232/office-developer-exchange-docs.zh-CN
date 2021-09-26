---
title: 联系人
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Contact
api_type:
- schema
ms.assetid: 66bfff50-7a91-4d81-b6a0-610b9962f677
description: Contact 元素表示应用商店中的联系人Exchange项。
ms.openlocfilehash: a91d8cab7db0bfe0cc102aa75d51df5b60603a77
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543539"
---
# <a name="contact"></a>联系人

Contact 元素表示联系人存储中的Exchange项。 
  
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
|[MimeContent](mimecontent.md) <br/> |包含以 base64Binary (表示) 对象的 MIME 流中的本机多用途 Internet 邮件扩展。  <br/> |
|[ItemId](itemid.md) <br/> |包含项目存储中项的唯一标识符Exchange项。  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |表示包含项目或文件夹的父文件夹的标识符。  <br/> |
|[ItemClass](itemclass.md) <br/> |表示项目的邮件类。  <br/> |
|[主题](subject.md) <br/> |表示用于存储Exchange响应对象的主题。  <br/> |
|[Sensitivity](sensitivity.md) <br/> |指示项目的敏感度级别。  <br/> |
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
|[DisplayCc](displaycc.md) <br/> |表示用于抄送行内容的显示字符串。 这是所有"抄送"收件人显示名称的串联字符串。  <br/> |
|[DisplayTo](displayto.md) <br/> |表示用于"To"行内容的显示字符串。 这是所有"收件人"收件人显示名称的串联字符串。  <br/> |
|[HasAttachments](hasattachments.md) <br/> |表示一个属性 **，如果项目** 具有至少一个可见附件，则该属性设置为 true。 此属性是只读的。  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项目的扩展属性。  <br/> |
|[Culture](culture.md) <br/> |表示邮箱中给定项目的区域性。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |包含显示名称用户修改项目的详细信息。  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |指示项目的上次修改时间。  <br/> |
|[IsAssociated](isassociated.md) <br/> |指示项目是否与文件夹关联。  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |表示连接到 Web App 终结点以读取Microsoft Office Outlook Web App 终结点的 URL Outlook Web App。  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |表示要连接到 Outlook Web App 终结点以编辑 Outlook Web App 中的项目的 URL。  <br/> |
|[ConversationId](conversationid.md) <br/> |包含项目或对话的标识符。  <br/> |
|[UniqueBody](uniquebody.md) <br/> |表示 HTML 片段或纯文本，表示此对话的唯一正文。  <br/> |
|[FileAs](fileas.md) <br/> |表示联系人在"联系人"文件夹中的存档。  <br/> |
|[FileAsMapping](fileasmapping.md) <br/> |定义如何构造为联系人显示的内容。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |定义显示名称的联系人属性。  <br/> |
|[GivenName](givenname.md) <br/> |包含联系人的给定姓名。  <br/> |
|[缩写](initials.md) <br/> |表示联系人的缩写。  <br/> |
|[MiddleName](middlename.md) <br/> |表示联系人的中间名。  <br/> |
|[Nickname](nickname.md) <br/> |表示联系人的昵称。  <br/> |
|[CompleteName](completename.md) <br/> |表示某个联系人的完整名称。  <br/> |
|[CompanyName](companyname.md) <br/> |表示与联系人关联的公司名称。  <br/> |
|[EmailAddresses](emailaddresses.md) <br/> |表示联系人的电子邮件地址的集合。  <br/> |
|[PhysicalAddresses](physicaladdresses.md) <br/> |包含与联系人关联的物理地址的集合。  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |代表联系人的电话号码集合。  <br/> |
|[AssistantName](assistantname.md) <br/> |代表联系人的助理。  <br/> |
|[生日](birthday.md) <br/> |表示联系人的出生日期。  <br/> |
|[BusinessHomePage](businesshomepage.md) <br/> |代表联系人 (主页) 电子邮件地址。  <br/> |
|[子女](children.md) <br/> |包含联系人的子项的名称。  <br/> |
|[Companies](companies.md) <br/> |表示与联系人关联的公司的集合。  <br/> |
|[ContactSource](contactsource.md) <br/> |描述联系人位于 active Directory Exchange还是 Active Directory 目录服务中。  <br/> |
|[Department](department.md) <br/> |表示联系人的工作部门。  <br/> |
|[生成](generation.md) <br/> |代表联系人的全名后代缩写。  <br/> |
|[ImAddresses](imaddresses.md) <br/> |表示联系人的即时消息地址的集合。  <br/> |
|[JobTitle](jobtitle.md) <br/> |表示联系人职务。  <br/> |
|[Manager](manager.md) <br/> |表示联系人的经理。  <br/> |
|[Mileage](mileage.md) <br/> |表示联系人项目的里程。  <br/> |
|[OfficeLocation](officelocation.md) <br/> |表示联系人的办公地点。  <br/> |
|[PostalAddressIndex](postaladdressindex.md) <br/> |表示物理地址的显示类型。  <br/> |
|[职业](profession.md) <br/> |代表联系人的工作。  <br/> |
|[SpouseName](spousename.md) <br/> |表示联系人配偶/伙伴的姓名。  <br/> |
|[Surname](surname.md) <br/> |表示联系人的姓氏。  <br/> |
|[WeddingAnniversary](weddinganniversary.md) <br/> |包含联系人的周年日。  <br/> |
|[HasPicture](haspicture.md) <br/> |指示联系人项目是否有代表联系人图片的文件附件。  <br/> |
|[PhoneticFullName](phoneticfullname.md) <br/> |包含联系人的全名，包括拼写为拼音的名字和姓氏。  <br/> |
|[PhoneticFirstName](phoneticfirstname.md) <br/> |包含用拼音拼写的联系人的名字。  <br/> |
|[PhoneticLastName](phoneticlastname.md) <br/> |包含联系人的姓氏，拼写为拼音。  <br/> |
|[Alias](alias.md) <br/> |包含联系人的电子邮件别名。  <br/> |
|[Notes (Contact)](notes-contact.md) <br/> |包含补充联系人信息。  <br/> |
|[照片](photo.md) <br/> |包含一个值，该值对联系人的照片进行编码。  <br/> |
|[UserSMIMECertificate](usersmimecertificate.md) <br/> |包含一个值，该值对联系人的 SMIME 证书进行编码。  <br/> |
|[MSExchangeCertificate](msexchangecertificate.md) <br/> |包含一个值，该值对联系人Exchange Microsoft 证书进行编码。  <br/> |
|[DirectoryId](directoryid.md) <br/> |包含联系人的目录 ID。  <br/> |
|[ManagerMailbox](managermailbox.md) <br/> |包含标识联系人的经理邮箱的 SMTP 信息。  <br/> |
|[DirectReports](directreports.md) <br/> |包含标识联系人的直接下属的 SMTP 信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素名**|**说明**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |描述与会议时间相邻的所有日历项目。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识要追加到 [UpdateItem](updateitem-operation.md)操作期间项目或文件夹的单个属性的数据。  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |标识与会议时间冲突的所有项目  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |标识要在本地客户端存储中创建一个文件夹。  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |代表Exchange附加到其他项目的项目Exchange项。  <br/> |
|[Items](items.md) <br/> |包含项目数组。  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |包含在由 [TargetFolderIdType 元素的 ParentFolderId ](parentfolderid-targetfolderidtype.md) (标识的文件夹中) 数组。  <br/> |
|[解决方法](resolution.md) <br/> |包含单个已解析的实体。  <br/> |
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


[创建联系人（Exchange Web 服务）](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[更新联系人](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[删除联系人](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

