---
title: 在 Exchange 电子邮件属性和 EWS 中的元素
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5266ff9f-d828-4ef4-b8ec-7b27d355c4c5
description: 了解一类和其他属性以及可以通过在 Exchange 使用 EWS 托管 API 或 EWS 获取电子邮件的元素。
ms.openlocfilehash: 4866c69213eb8b11c785ab14f0595c45448834d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752734"
---
# <a name="email-properties-and-elements-in-ews-in-exchange"></a>在 Exchange 电子邮件属性和 EWS 中的元素

了解一类和其他属性以及可以通过在 Exchange 使用 EWS 托管 API 或 EWS 获取电子邮件的元素。
  
电子邮件有 50 多个属性，并获取的所需，当您所愿，可能会造成混淆，如果您不知道查找的位置。 最重要的事情要了解有关使用电子邮件属性和元素是其中包含每个主要的检索方法和操作返回的一类的属性和元素集中。 根据您使用的检索方法返回的一类的属性集而定。 还有一点不需要欺骗 AllProperties [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) EWS 元素，此名称对应于 EWS 托管 API 中的[BasePropertySet.FirstClassMessageProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx)枚举值的值。 此值不实际包括所有属性，它只包括一类的属性。 
  
## <a name="first-class-properties-and-elements-for-email-messages"></a>一类的属性和元素的电子邮件
<a name="bk_firstclass"> </a>

一组的一类的属性和 EWS 托管 API [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)方法和 EWS [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)操作返回的元素是稍有不同组一类的属性和元素返回的 EWS托管的 API [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法和 EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作。 返回由**FindItems**方法和**FindItem**操作的一类属性是**绑定**方法和**GetItem** operation，返回的属性的子集。 表 1 列出了由**Bind**方法和**GetItem**操作，返回的所有一类属性，并指定其中的哪些不返回**FindItems**方法或**FindItem**操作。 请注意，不能扩展**FindItems**方法或**FindItem**操作来检索其他属性和元素，例如**ToRecipients**、 **CcRecipients**和**BccRecipients**。 如果您需要检索这些值，请使用**FindItems**方法或**FindItem**操作可获取电子邮件的项 Id，然后使用**Bind**方法或**GetItem**操作，以检索所需的属性。 有关演示如何使用**绑定**或**FindItems**方法检索项的代码示例，请参阅[获取使用 EWS 托管 API 的项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma)。 有关演示如何检索项目使用**GetItem**或**FindItem**操作的代码示例，请参阅[获取使用 EWS 项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews)。
  
下表中的响应中的显示的顺序中列出了一类的属性和元素。
  
**表 1。一类的电子邮件属性和元素**

|**EWS 托管 API 属性**|**EWS 元素**|**为**FindItems**方法或**FindItem**操作的一类属性？**|**读 / 写或只读**|
|:-----|:-----|:-----|:-----|
|
  [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) <br/> |[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[ParentFolderId](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.parentfolderid%28v=exchg.80%29.aspx) <br/> |[ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[ItemClass](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) <br/> |[ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[Subject](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx) <br/> |[Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[Sensitivity](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.sensitivity%28v=exchg.80%29.aspx) <br/> |[Sensitivity](http://msdn.microsoft.com/library/d872423a-c26e-4675-9028-23361fb4a43d%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[Body](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) <br/> |[Body](http://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) <br/> |否  <br/> |读 / 写  <br/> |
|[附件](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) <br/> |[附件](http://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) <br/> |否  <br/> |读 / 写  <br/> |
|[DateTimeReceived](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.datetimereceived%28v=exchg.80%29.aspx) <br/> |[DateTimeReceived](http://msdn.microsoft.com/library/8f489bd4-2434-4d0a-91fe-1b5ba7eb5765%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[Size](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.size%28v=exchg.80%29.aspx) <br/> |[Size](http://msdn.microsoft.com/library/966f4daf-c20e-49f8-aeb6-965f3e2da7c3%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[类别](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.categories%28v=exchg.80%29.aspx) <br/> |[类别](http://msdn.microsoft.com/library/d84d4927-b524-4e62-bf3d-1f12fec8c21a%28Office.15%29.aspx) <br/> |否  <br/> |读 / 写  <br/> |
|[Importance](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.importance%28v=exchg.80%29.aspx) <br/> |[Importance](http://msdn.microsoft.com/library/1557f59a-41f2-43fb-9ded-88f3ec5c76cb%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[InReplyTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.inreplyto%28v=exchg.80%29.aspx) <br/> |[InReplyTo](http://msdn.microsoft.com/library/561b8941-1c26-4bbe-aa0f-b49ec8a79af5%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[IsSubmitted](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.issubmitted%28v=exchg.80%29.aspx) <br/> |[IsSubmitted](http://msdn.microsoft.com/library/2399e27e-bd8c-46b6-a3aa-674842e098c9%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[IsDraft](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.isdraft%28v=exchg.80%29.aspx) <br/> |[IsDraft](http://msdn.microsoft.com/library/8b8d9cc9-a512-458a-94e4-af210ac83bd7%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[IsFromMe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.isfromme%28v=exchg.80%29.aspx) <br/> |[IsFromMe](http://msdn.microsoft.com/library/d3c5fbf0-a95c-46e5-890f-953e50ac49d6%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[IsResend](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.isresend%28v=exchg.80%29.aspx) <br/> |[IsResend](http://msdn.microsoft.com/library/8f758b6b-dcee-4f95-9d39-e4be2bd92961%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[IsUnmodified](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.isunmodified%28v=exchg.80%29.aspx) <br/> |[IsUnmodified](http://msdn.microsoft.com/library/8f758b6b-dcee-4f95-9d39-e4be2bd92961%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[InternetMessageHeaders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.internetmessageheaders%28v=exchg.80%29.aspx) <br/> |[InternetMessageHeaders](http://msdn.microsoft.com/library/4dcf8671-96df-4a2d-9836-7e8e3a67e0db%28Office.15%29.aspx) <br/> |否  <br/> |只读  <br/> |
|[DateTimeSent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.datetimesent%28v=exchg.80%29.aspx) <br/> |[DateTimeSent](http://msdn.microsoft.com/library/81784ef3-8912-4d63-8502-73419a906999%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[DateTimeCreated](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.datetimecreated%28v=exchg.80%29.aspx) <br/> |[DateTimeCreated](http://msdn.microsoft.com/library/42ae0067-4688-49d9-93c5-c4dbeb54cee1%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[AllowedResponseActions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.allowedresponseactions%28v=exchg.80%29.aspx) <br/> |[ResponseObjects](http://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) <br/> |否  <br/> |只读  <br/> |
|[ReminderDueBy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.reminderdueby%28v=exchg.80%29.aspx) <br/> |[ReminderDueBy](http://msdn.microsoft.com/library/e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[IsReminderSet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.isreminderset%28v=exchg.80%29.aspx) <br/> |[ReminderIsSet](http://msdn.microsoft.com/library/fa366afe-77a0-4c14-9edb-ffc9699131ba%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[ReminderMinutesBeforeStart](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.reminderminutesbeforestart%28v=exchg.80%29.aspx) <br/> |[ReminderMinutesBeforeStart](http://msdn.microsoft.com/library/65ea14bc-5f19-48cc-aef1-46227e06f5f5%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[DisplayCc](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.displaycc%28v=exchg.80%29.aspx) <br/> |[DisplayCc](http://msdn.microsoft.com/library/af386e06-80f3-42c7-8b3c-1f7993c49d10%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[DisplayTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.displayto%28v=exchg.80%29.aspx) <br/> |[DisplayTo](http://msdn.microsoft.com/library/16a0b22d-063b-417c-8aba-efcf9490b072%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) <br/> |[HasAttachments](http://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[区域性](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.culture%28v=exchg.80%29.aspx) <br/> |[区域性](http://msdn.microsoft.com/library/71bd62c6-3fec-48db-9a5e-02121e9bc20b%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[EffectiveRights](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.effectiverights%28v=exchg.80%29.aspx) <br/> |[EffectiveRights](http://msdn.microsoft.com/library/bf5278eb-3a1a-4d27-9d16-b8be043bb023%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[LastModifiedName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.lastmodifiedname%28v=exchg.80%29.aspx) <br/> |[LastModifiedName](http://msdn.microsoft.com/library/4f1a90c1-e27e-4e16-93c3-e79d4cb720d1%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[LastModifiedTime](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.lastmodifiedtime%28v=exchg.80%29.aspx) <br/> |[LastModifiedTime](http://msdn.microsoft.com/library/6db2cabc-e7f4-4d71-962b-789de6a192a4%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[IsAssociated](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.isassociated%28v=exchg.80%29.aspx) <br/> |[IsAssociated](http://msdn.microsoft.com/library/637f0798-6680-487f-bcbf-aaddc4a74186%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[WebClientReadFormQueryString](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.webclientreadformquerystring%28v=exchg.80%29.aspx) <br/> |[WebClientReadFormQueryString](http://msdn.microsoft.com/library/13e8871a-32a6-4bb9-9493-864c4c07efff%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[WebClientEditFormQueryString](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.webclienteditformquerystring%28v=exchg.80%29.aspx) <br/> |[WebClientEditFormQueryString](http://msdn.microsoft.com/library/9e571021-d58f-424b-8db2-48cf683533dc%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[ConversationId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.conversationid%28v=exchg.80%29.aspx) <br/> |[ConversationId](http://msdn.microsoft.com/library/d5f1ddb3-9af3-4677-a6ba-111b304a951e%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[Flag](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.flag%28v=exchg.80%29.aspx) <br/> |[Flag](http://msdn.microsoft.com/library/7b47bc74-a60d-4308-8674-5d52444a1753%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[InstanceKey](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.instancekey%28v=exchg.80%29.aspx) <br/> |[InstanceKey](http://msdn.microsoft.com/library/bb4dbe9b-aea0-4527-b7d6-e928066caf38%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[EntityExtractionResult](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.entityextractionresult%28v=exchg.80%29.aspx) <br/> |[EntityExtractionResult](http://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx) <br/> |否  <br/> |只读  <br/> |
|[发件人](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx) <br/> |[发件人](http://msdn.microsoft.com/library/26d1a46e-e1d3-44b8-a02d-fa6f83aa5cda%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[ToRecipients](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) <br/> |[ToRecipients](http://msdn.microsoft.com/library/72dc3be8-30bb-4ae1-acf4-fb94ff490631%28Office.15%29.aspx) <br/> |否  <br/> |只读  <br/> |
|[CcRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.ccrecipients%28v=exchg.80%29.aspx) <br/> |[CcRecipients](http://msdn.microsoft.com/library/5c20ec3a-0bee-4e67-b220-586ed0d601c9%28Office.15%29.aspx) <br/> |否  <br/> |只读  <br/> |
|[BccRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bccrecipients%28v=exchg.80%29.aspx) <br/> |[BccRecipients](http://msdn.microsoft.com/library/c4e05168-d36b-4740-a526-4b7da53553c1%28Office.15%29.aspx) <br/> |否  <br/> |只读  <br/> |
|[IsReadReceiptRequested](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.isreadreceiptrequested%28v=exchg.80%29.aspx) <br/> |[IsReadReceiptRequested](http://msdn.microsoft.com/library/7ab6edd5-c7ed-4701-8de3-d7dc7ecfa9c2%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[IsDeliveryReceiptRequested](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.isdeliveryreceiptrequested%28v=exchg.80%29.aspx) <br/> |[IsDeliveryReceiptRequested](http://msdn.microsoft.com/library/97776b7e-942c-4663-8277-165d64364daa%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[ConversationIndex](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.conversationindex%28v=exchg.80%29.aspx) <br/> |[ConversationIndex](http://msdn.microsoft.com/library/fdf47e22-8d93-4ae4-883b-0c9f07f48724%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[ConversationTopic](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.conversationtopic%28v=exchg.80%29.aspx) <br/> |[ConversationTopic](http://msdn.microsoft.com/library/46cacf42-4039-4c8a-9b20-c42cdd9f2760%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[发件人](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.from%28v=exchg.80%29.aspx) <br/> |[发件人](http://msdn.microsoft.com/library/5a52d644-3677-4049-874c-12bd5c3080dc%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[InternetMessageId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.internetmessageid%28v=exchg.80%29.aspx) <br/> |[InternetMessageId](http://msdn.microsoft.com/library/a5a9563f-e761-4658-9957-0e13566f6a35%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[IsRead](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx) <br/> |[IsRead](http://msdn.microsoft.com/library/161455d5-a870-4c99-b2eb-c759c538f1bc%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[IsResponseRequested](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.isresponserequested%28v=exchg.80%29.aspx) <br/> |[IsResponseRequested](http://msdn.microsoft.com/library/8cb874ed-a538-4de6-ab22-2631092dcdd0%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[回复](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.replyto%28v=exchg.80%29.aspx) <br/> |[回复](http://msdn.microsoft.com/library/6b6ae792-e2c4-4aa0-95cb-b49b446f1e08%28Office.15%29.aspx) <br/> |否  <br/> |只读  <br/> |
|[引用](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.references%28v=exchg.80%29.aspx) <br/> |[引用](http://msdn.microsoft.com/library/d78f9a48-cd24-452f-af65-4c01933227ce%28Office.15%29.aspx) <br/> |是  <br/> |读 / 写  <br/> |
|[ReceivedBy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.receivedby%28v=exchg.80%29.aspx) <br/> |[ReceivedBy](http://msdn.microsoft.com/library/ac84c9c5-d2fe-4b6f-bf4d-0444131d835b%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
|[ReceivedRepresenting](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.receivedrepresenting%28v=exchg.80%29.aspx) <br/> |[ReceivedRepresenting](http://msdn.microsoft.com/library/1157b042-6dce-4cdc-9700-e22b749da39f%28Office.15%29.aspx) <br/> |是  <br/> |只读  <br/> |
   
## <a name="other-properties-and-elements-for-email-messages"></a>其他属性和元素的电子邮件
<a name="bk_notfirstclass"> </a>

并非所有重要的电子邮件属性和元素是一类的属性和元素。 若要获取的属性或元素，您需要将其添加到您的[属性集](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx)，如果您正在使用 EWS 托管 API，或使用属性的路径以将其添加到 EWS 操作呼叫。 例如，若要检索的文本正文和消息的 MIME 内容，您**属性集**所示创建的**绑定**或**负载**的方法。 
  
```cs
PropertySet(BasePropertySet.IdOnly, ItemSchema.TextBody, ItemSchema.MimeContent);
```

或者，如果您正在使用 EWS，元素向 element 中添加[AdditionalProperties](http://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx)在**GetItem**操作要求中，如下所示。 
  
```XML
<t:AdditionalProperties>
    <t:FieldURI FieldURI="item:TextBody" />
    <t:FieldURI FieldURI="item:MimeContent" />
</t:AdditionalProperties>
```

 从 EWS 托管 API [ServiceObject](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobject%28v=exchg.80%29.aspx)对象继承的**EmailMessage**属性不能包含一个**绑定**方法; 设置的属性但是，所有**ServiceObject**属性是可读**EmailMessage**对象，并且通过**Bind**方法检索。 
  
**表 2。其他电子邮件属性和元素**

|**EWS 托管 API 属性**|**EWS 元素**|**读 / 写或只读**|
|:-----|:-----|:-----|
|[ArchiveTag](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.archivetag%28v=exchg.80%29.aspx) <br/> |[ArchiveTag](http://msdn.microsoft.com/library/c4cb0718-37cd-41aa-86e7-b492c4bb86aa%28Office.15%29.aspx) <br/> |读 / 写  <br/> |
|[ExtendedProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.extendedproperties%28v=exchg.80%29.aspx) <br/> |[ExtendedProperty](http://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx) <br/> |只读  <br/> |
|[IconIndex](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.iconindex%28v=exchg.80%29.aspx) <br/> |[IconIndex](http://msdn.microsoft.com/library/92020822-2a86-4dfc-aee1-3067af4d4edf%28Office.15%29.aspx) <br/> |只读  <br/> |
|[IsAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.isattachment%28v=exchg.80%29.aspx) <br/> |不适用  <br/> |只读  <br/> |
|[IsDirty](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobject.isdirty%28v=exchg.80%29.aspx) <br/> |不适用  <br/> |只读  <br/> |
|[IsNew](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.isnew%28v=exchg.80%29.aspx) <br/> |不适用  <br/> |只读  <br/> |
|[Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobject.item%28v=exchg.80%29.aspx) <br/> |[Item](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) <br/> |只读  <br/> |
|[MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) <br/> |[MimeContent](http://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx) <br/> |只读  <br/> |
|不适用  <br/> |[MimeContentUTF8](http://msdn.microsoft.com/library/31544c95-5231-4b57-958c-2a689464d29b%28Office.15%29.aspx) <br/> |只读  <br/> |
|[NormalizedBody](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.normalizedbody%28v=exchg.80%29.aspx) <br/> |[NormalizedBody](http://msdn.microsoft.com/library/bfb813e4-642d-4f1b-9e91-1fee89dbd083%28Office.15%29.aspx) <br/> |只读  <br/> |
|[PolicyTag](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.policytag%28v=exchg.80%29.aspx) <br/> |[PolicyTag](http://msdn.microsoft.com/library/fa4b1447-dc7b-47ad-a677-78fcee443dc6%28Office.15%29.aspx) <br/> |读 / 写  <br/> |
|[预览](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.preview%28v=exchg.80%29.aspx) <br/> |[预览](http://msdn.microsoft.com/library/5d33f557-c9d5-4f7f-82c0-d800412f8b7e%28Office.15%29.aspx) <br/> |读 / 写  <br/> |
|[RetentionDate](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.retentiondate%28v=exchg.80%29.aspx) <br/> |[RetentionDate](http://msdn.microsoft.com/library/0c1df5e2-b56a-4947-a047-2b73b32e5fb7%28Office.15%29.aspx) <br/> |只读  <br/> |
|[架构](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobject.schema%28v=exchg.80%29.aspx) <br/> |不适用  <br/> |只读  <br/> |
|[服务](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobject.service%28v=exchg.80%29.aspx) <br/> |不适用  <br/> |只读  <br/> |
|[StoreEntryId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.storeentryid%28v=exchg.80%29.aspx) <br/> |[StoreEntryId](http://msdn.microsoft.com/library/f536e264-8c4d-4cc5-bab8-22a4fa38de39%28Office.15%29.aspx) <br/> |只读  <br/> |
|[TextBody](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.textbody%28v=exchg.80%29.aspx) <br/> |[TextBody](http://msdn.microsoft.com/library/bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820%28Office.15%29.aspx) <br/> |只读  <br/> |
|[UniqueBody](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.uniquebody%28v=exchg.80%29.aspx) <br/> |[UniqueBody](http://msdn.microsoft.com/library/06bc95d7-121c-433b-bd27-c2b0eb8c011f%28Office.15%29.aspx) <br/> |只读  <br/> |
   
## <a name="see-also"></a>另请参阅


- [电子邮件和 Exchange 中的 EWS](email-and-ews-in-exchange.md)
    
- [属性和交换中的 EWS 中的扩展的属性](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [属性集和响应形状在 EWS 在 Exchange](property-sets-and-response-shapes-in-ews-in-exchange.md)
    
- [通过在 Exchange 使用 EWS 来处理 Exchange 邮箱项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    

