---
title: 属性和交换中的 EWS 中的扩展的属性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 68623048-060e-4602-b3fa-62617a94cf72
description: 了解如何使用 Exchange 中的 EWS 定义和访问项目和文件夹上的属性。
localization_priority: Priority
ms.openlocfilehash: 0891cf6d6dddf74518fbbc8efbaebdd8eb0c706b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459333"
---
# <a name="properties-and-extended-properties-in-ews-in-exchange"></a>属性和交换中的 EWS 中的扩展的属性

了解如何使用 Exchange 中的 EWS 定义和访问项目和文件夹上的属性。
  
Exchange 邮箱包含大量项目，包括电子邮件、约会、会议等。 这些项目由属性组成;属性描述项。 您可以使用项目属性执行[搜索](search-and-ews-in-exchange.md)、[同步项目更改](mailbox-synchronization-and-ews-in-exchange.md)和[创建自定义属性类型](https://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)。 本文概述了属性以及如何使用应用程序中的属性。
  
## <a name="exchange-item-properties"></a>Exchange 项目属性
<a name="ItemsAreProperties"> </a>

Exchange 中的项目和文件夹实质上是表中的行。 标识项或文件夹的主属性是其[EWS 标识符](ews-identifiers-in-exchange.md)。 虽然 Exchange 数据库中存在其他与标识符相关的属性，但对于 EWS，EWS 标识符充当描述项目的属性集合的主键。 EWS 标识符属性包含两个部分：
  
- 用于标识项目的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)或[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)属性 
    
- 一个**ChangeKey**属性，该属性包含有关项或文件夹是否已更改的状态信息 
    
邮箱中的所有项目都存储在同一个 Exchange 数据库中，并使用相同的数据库架构。 项目由[ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx)属性、属性约束和业务逻辑层的组合来区分，这些层将影响在 Exchange 存储中管理它们的方式。 表1显示了如何跨不同的项目类型应用属性;在此示例中，为电子邮件和约会项目。 这两个项目都具有[Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)属性的值。 但请注意，电子邮件项目上未设置[IsAllDayEvent](https://msdn.microsoft.com/library/29140a64-9d7a-4a14-a10d-c98197c9831b%28Office.15%29.aspx)属性，并且不会对约会设置**IsReadReceiptRequested**属性。 幸运的是，您不需要知道哪些属性适用于每个项目类;EWS 可为你处理这种情况。 
  
**表1。约会和电子邮件属性的比较**

|**项目类型**|**Item 类**|**主题**|**IsAllDayEvent**|**IsReadReceiptRequested**|
|:-----|:-----|:-----|:-----|:-----|
|电子邮件  <br/> |IPM.NOTE.便笺  <br/> |状态报告：项目 X 完成  <br/> |不适  <br/> |true  <br/> |
|Appointment  <br/> |IPM.NOTE.日程  <br/> |Contoso 公司会议  <br/> |false  <br/> |不适  <br/> |
   
EWS 架构支持由 Exchange 数据库和介于 EWS 和 Exchange 数据库之间的业务逻辑层管理的许多约束。 EWS 架构将定义的一组属性应用于每个项目类型。 以下是由 EWS 提供的强类型 Exchange 数据库项： 
  
- 电子邮件
    
- 约会
    
- 联系人
    
- 通讯组列表
    
- 会议邮件
    
- 会议请求
    
- 会议响应
    
- 会议取消
    
- 任务
    
- 发布项目
    
通用项目由 EWS 以电子邮件的形式返回。 EWS 托管 API 实现所有这些项目类型。
  
> [!NOTE]
> 响应对象仅由客户端发送到服务器，以响应从其他人收到的项目。 它们在 Exchange 数据库中不存在。 
  
## <a name="what-are-properties-in-ews"></a>什么是 EWS 属性？
<a name="WhatAreEWSProperties"> </a>

EWS 架构描述在 EWS 客户端和 Exchange 之间发送的数据。 架构的大部分部分描述了您可以在 Exchange 数据库中访问的项目和文件夹属性。 EWS 架构描述了可用于您的应用程序的 Exchange 数据库属性的 XML 表示形式。 实际属性（根据哪些属性可用）、它们所采用的表单以及它们返回的值因您尝试执行的操作而异。 例如， **Body**属性将仅返回**FindItem**操作中的前512个字符，但**GetItem**操作将返回项目的完整文本。 尽管大多数属性都是可设置和可检索的，但某些属性仅由 Exchange 设置。 每个属性都以 XML 格式存在于架构中，该格式在存储在 Exchange 数据库中时反映属性，或从存储在 Exchange 数据库中的属性进行计算。 **Subject**属性是可设置属性的一个示例。文件夹的**UnreadCount**属性是计算属性的一个示例。 核心项目类型的通用属性集。 
  
以下因素决定了应用程序从 Exchange 获取的属性集： 
  
- 您的应用程序正在调用的操作
    
- 基本响应形状
    
- 项目类型
    
- 指定的属性路径
    
了解这些不同因素对您可以访问的数据有何影响是非常重要的。 与前面提到的**Body**属性的示例一样，有些信息根据各种因素有条件地可用。 通过帮助您选择正确的选项来访问所需的信息，了解这些因素可节省时间。 若要发现哪些属性是可访问的，需要测试这些因素以确定如何访问您的应用程序所需的属性。 本节介绍这些不同的因素如何影响在 EWS 响应中返回哪些属性。 
  
### <a name="ews-response-shapes"></a>EWS 响应形状

Exchange 存储了大量有关项目的信息。 有时，您的应用程序不需要所有这些信息，在很多情况下，最好不要全部实现。 [EWS 响应形状](property-sets-and-response-shapes-in-ews-in-exchange.md)（也称为 "属性" 形状）指示从服务器返回的属性。 响应形状的核心元素是基准形状。 基准形状是强类型项目的默认预设属性包。 基形状等效的 EWS 托管 API 是[BasePropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx)。 EWS 包含三个默认响应形状。
  
**表2。默认响应形状**

|**默认响应形状名称**|**EWS 托管 API 等效项**|**说明**|
|:-----|:-----|:-----|
|IdOnly  <br/> |BasePropertySet IdOnly 值  <br/> |仅返回 EWS 标识符和更改键。 除非客户端使用 AllProperties 或默认形状返回的所有属性，否则使用 IdOnly 形状并使用**PropertySet**类上设置的属性路径指定其他属性。 大多数应用程序应使用指定了其他属性的 IdOnly 响应形状。 这将减少客户端请求的未使用数据量。  <br/> |
|默认  <br/> |不适用  <br/> |项目类型的一组标准属性。 仅当应用程序使用所有属性时，才使用此响应形状。  <br/> |
|AllProperties  <br/> |BasePropertySet FirstClassProperties 值  <br/> |一组比默认形状更大的属性。 尽管该名称暗示它，但此选项不会返回项目的所有属性。 此属性集返回客户端应用程序最常使用的属性。 如果需要其他属性，可以通过属性路径请求这些属性。  <br/> 如果您的应用程序不使用此响应形状返回的所有属性，请使用 IdOnly 响应形状，并指定其他属性。  <br/> |
   
许多 EWS 操作都返回项目及其属性。 无论您指定的响应形状如何，不同的操作都可以返回不同的属性集。 不同的项目类型也返回不同的属性，具体取决于操作和指定的响应形状。 以下操作使用响应形状来确定要返回的属性。
  
**表3。使用响应形状的操作**

|**EWS 操作**|**EWS 托管的 API 方法**|
|:-----|:-----|
|[GetConversationItems](https://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |
|[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |[Folder 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |
|[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |[Item 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |
|[FindConversation](https://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |
|[FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |[FindFolders 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |
|[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |[FindItems 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> [ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |
|[FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |未实现。  <br/> |
|[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |
|[SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> [ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsearchmailboxes%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
属性形状是标识您希望应用程序返回的属性的一种基本方法。 但有时，您的应用程序需要一组更加细化的特定属性。 为此，可以使用属性路径。
  
### <a name="choose-properties-by-their-property-path"></a>按属性路径选择属性

EWS 属性路径是用于标识请求或响应中的属性的元数据。 
  
**表4。属性路径类型**

|**属性路径类型**|**架构类型**|**EWS 托管 API 实现**|**说明**|
|:-----|:-----|:-----|:-----|
|FieldUri  <br/> |PathToUnindexedFieldType  <br/> |继承自[ServiceObjectSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceobjectschema%28v=exchg.80%29.aspx)的类型。  <br/> |最常见的属性路径。 FieldUri 属性路径是在 EWS 托管 API 中的**PropertySet**对象上指定的。 大多数 EWS 属性可由 FieldUri 属性路径指定。 这是由 EWS 架构中的 UnindexedFieldURIType 描述的。  <br/> FieldUri 属性路径 XML 如下所示：  <br/> ```XML<FieldURI FieldURI="item:Subject"/>```此属性路径等效于 EWS 托管 API 中的 ItemSchema。  <br/> |
|IndexedFieldUri  <br/> |PathToIndexedFieldType  <br/> |继承自[ItemSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx)的类型。  <br/> |标识需要属性索引以指定要返回的值的字典属性。 当属性可以有多个值时，使用此路径。 这由 EWS 架构中的**DictionaryURIType**属性描述。 **DictionaryURIType**属性路径是在 EWS 托管 API 中的**PropertySet**对象上指定的。  <br/> IndexedFieldUri 属性路径 XML 如下所示：  <br/> ```XML<IndexedFieldURI FieldURI="contacts:PhysicalAddress:Street FieldIndex="Home"/>```|
|ExtendedFieldUri  <br/> |PathToExtendedFieldType  <br/> |[ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |标识在项上标识自定义或非架构化属性的扩展属性定义。  <br/> ExtendedFieldUri 属性路径 XML 如下所示：  <br/> ```XML<ExtendedFieldURI> PropertyTag="0x1234" PropertyType="Integer" />```|
|ExceptionFieldUri  <br/> |ExceptionFieldURI  <br/> |[ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) <br/> |指定与 EWS 响应中的错误关联的属性。 这由 EWS 架构中的**ExceptionPropertyURIType**类型进行描述。 这仅发生在使用日历定期模式时发生的错误响应的**MessageXml**元素中。  <br/> |
   
作为一种最佳做法，在请求属性时，请在 EWS 托管 API 中使用 IdOnly 基准形状（[BasePropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) ），然后通过指定属性路径仅请求应用程序所需的属性。 
  
### <a name="schematized-properties"></a>架构化属性

您的 EWS 客户端所需的大多数属性都是由 EWS 架构描述的。 在类型 .xsd 架构中可以找到主文件夹和项目类型定义，其中包含属性定义。 以下架构类型包含您可以使用的大多数对象的属性定义。
  
**表5。包含属性定义的架构类型**

|**EWS 架构类型**|**EWS 托管 API 类型等效**|**定义 .。。**|
|:-----|:-----|:-----|
|**ItemType** <br/> |[Item 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) <br/> |基本项类型属性集。 此类型可从客户端创建，但不会由 Exchange 返回。 Exchange 返回所有泛型对象的 MessageType 对象。  <br/> |
|**MessageType** <br/> |[EmailMessage 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |电子邮件对象属性集和所有泛型对象的属性集。  <br/> |
|**CalendarItemType** <br/> |[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |日历项目属性集;这包括单个约会和定期约会。  <br/> |
|**ContactItemType** <br/> |[Contact 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |联系人项目属性集。  <br/> |
|**DistributionListType** <br/> |[ContactGroup 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |个人通讯组列表属性集。  <br/> |
|**MeetingMessageType** <br/> |[MeetingMessage 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingmessage%28v=exchg.80%29.aspx) <br/> |会议邮件类型属性集。  <br/> |
|**MeetingRequestMessageType** <br/> |[MeetingRequest 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequest%28v=exchg.80%29.aspx) <br/> |会议请求类型属性集。  <br/> |
|**MeetingResponseMessageType** <br/> |[MeetingResponse 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingresponse%28v=exchg.80%29.aspx) <br/> |会议响应类型属性集。  <br/> |
|**MeetingCancellationMessageType** <br/> |[MeetingCancellation 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingcancellation%28v=exchg.80%29.aspx) <br/> |会议取消类型属性集。  <br/> |
|**TaskType** <br/> |[任务类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |任务类型属性集。  <br/> |
|**PostItemType** <br/> |[PostItem 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |Postitem 类型属性集。  <br/> |
|**FolderType** <br/> |[Folder 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |文件夹类型属性集。  <br/> |
|**CalendarFolderType** <br/> |[CalendarFolder 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |SearchFolder 类型属性集。  <br/> |
|**ContactsFolderType** <br/> |[ContactsFolder 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |ContactsFolder 类型属性集。  <br/> |
|**SearchFolderType** <br/> |[SearchFolder 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |SearchFolder 类型属性集。  <br/> |
|**TasksFolderType** <br/> |[TasksFolder 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |TasksFolder 类型属性集。  <br/> |
|**UserConfigurationType** <br/> |[UserConfiguration 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration%28v=exchg.80%29.aspx) <br/> |UserConfiguration 类型属性集。  <br/> |
   
虽然 EWS 架构中的属性足以满足许多应用程序的需要，但不能通过仅使用架构中描述的内容来实现某些方案。 对于这些方案，您可以扩展属性。 
  
### <a name="extended-properties-aka-non-schematized-properties"></a>扩展属性（亦称为非架构化属性）

扩展属性使您能够创建自定义属性，从而使您可以访问在 EWS 架构中未定义的 Exchange 存储中的项目和文件夹上的属性。 您可以使用它们访问 Exchange 数据库中的本机 MAPI 项目和文件夹属性。 可以使用扩展属性访问所有架构化属性，因为在封面下，这些架构化属性是 Exchange 数据库中的 MAPI 属性以外的任何属性。 
  
PathToExtendedFieldType 架构类型位于类型 .xsd 架构中，用于定义代表扩展属性的 XML。 此架构类型定义 XML 实例中的[ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素;换言之，它定义在服务和客户端之间发送的 XML。 ExtendedPropertyType 架构类型定义[ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素以及扩展属性包含的值或值数组。 下表显示了扩展属性 XML 的大致映射以及它如何在 EWS 托管 API 中的项上实现。 
  
**表6。在 EWS 托管 API 中实现的扩展属性 XML**

|**EWS 托管 API 实现**|**包含的内容**|**它映射到的内容**|
|:-----|:-----|:-----|
|[ExtendedProperties 属性](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.extendedproperties%28v=exchg.80%29.aspx) <br/> |项的扩展属性的集合。  <br/> |项的一个或多个扩展属性实例。  <br/> |
|[ExtendedProperty 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedproperty%28v=exchg.80%29.aspx) <br/> |扩展属性定义和值。  <br/> |ExtendedPropertyType 架构类型。  <br/> |
|[ExtendedPropertyDefinition 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |扩展属性定义。  <br/> |PathToExtendedFieldType 架构类型。  <br/> |
   
若要了解有关如何在应用程序中使用扩展属性的详细信息，可以浏览以下代码示例： 
  
- [MFCMapi](http://mfcmapi.codeplex.com/)
    
- [Exchange 2013：以编程方式设置自定义 X 标头](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Exchange 2013：通过属性的属性标记访问属性](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-719875ac)
    
- [Exchange 2013：通过其标识符访问命名属性](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-02dbe22f)
    
- [Exchange 2013：按名称访问命名属性](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-6556e183)
    
- [Exchange 2013：按属性集 GUID 和名称访问属性](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-4021f971)
    
- [Exchange 2013：以编程方式创建自定义扩展属性](https://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)
    
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [使用 Exchange 中的 EWS 设置 x 标头](how-to-provision-x-headers-by-using-ews-in-exchange.md)
    
- [EWS 属性相关的错误](ews-property-related-errors.md)
    
## <a name="see-also"></a>另请参阅


- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)
    
- [MFCMapi](http://mfcmapi.codeplex.com/)
    

