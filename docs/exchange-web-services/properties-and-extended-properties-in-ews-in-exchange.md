---
title: 属性和交换中的 EWS 中的扩展的属性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 68623048-060e-4602-b3fa-62617a94cf72
description: 了解如何定义并通过在 Exchange 使用 EWS 访问项目和文件夹的属性。
ms.openlocfilehash: 0c01d9bd21cbef0a3536c8dbd85e192199b7b8ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753008"
---
# <a name="properties-and-extended-properties-in-ews-in-exchange"></a>属性和交换中的 EWS 中的扩展的属性

了解如何定义并通过在 Exchange 使用 EWS 访问项目和文件夹的属性。
  
Exchange 邮箱包含大量项目，包括电子邮件、 约会、 会议和等等。 这些项目组成的属性。属性描述了项目。 项目属性可用于执行[搜索](search-and-ews-in-exchange.md)和[同步项的更改](mailbox-synchronization-and-ews-in-exchange.md)，并[创建自定义属性类型](http://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)。 本文概述了属性和您可以如何使用属性应用程序中。
  
## <a name="exchange-item-properties"></a>Exchange 项目属性
<a name="ItemsAreProperties"> </a>

项目和 Exchange 中的文件夹是本质上表中的行。 标识项目或文件夹的主属性是其[EWS 标识符](ews-identifiers-in-exchange.md)。 虽然在 Exchange 数据库中，为 EWS，还有其他标识符相关的属性的 EWS 标识符用作描述项目的属性集的主关键字。 EWS 标识符属性包含两部分：
  
- 标识项目[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)或[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)属性 
    
- 包含状态信息项或文件夹是否已更改的**更改密钥**属性 
    
邮箱中的所有项相同的 Exchange 数据库中存储和使用相同的数据库架构。 项目组合来区分[ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx)属性、 属性约束和影响 Exchange 中如何管理他们的业务逻辑图层的存储。 表 1 显示了如何跨不同项目类型; 应用属性在此示例、 电子邮件和约会项。 这两个项目具有[Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)属性的值。 但请注意[IsAllDayEvent](http://msdn.microsoft.com/library/29140a64-9d7a-4a14-a10d-c98197c9831b%28Office.15%29.aspx)属性未设置对电子邮件项目，并且**IsReadReceiptRequested**属性未设置约会。 幸运的是，您不需要知道哪些属性适用于每个项类;EWS 为您处理此操作。 
  
**表 1。约会和电子邮件属性的比较**

|**项目类型**|**项类**|**Subject**|**IsAllDayEvent**|**IsReadReceiptRequested**|
|:-----|:-----|:-----|:-----|:-----|
|Email  <br/> |IPM。注释  <br/> |状态报告： 项目 X 完成  <br/> |NULL  <br/> |True  <br/> |
|Appointment  <br/> |IPM.Appointment  <br/> |Contoso 公司的会议  <br/> |false  <br/> |NULL  <br/> |
   
EWS 架构支持许多托管的 Exchange 数据库和业务逻辑层 EWS 和 Exchange 数据库之间的约束。 EWS 架构适用定义一组属性设置为每个项类型。 以下是提供 EWS 的强类型 Exchange 数据库项目： 
  
- 电子邮件
    
- 约会
    
- 联系人
    
- 通讯组列表
    
- 会议消息
    
- 会议要求
    
- 会议响应
    
- 会议取消
    
- 任务
    
- 发布项目
    
通用项目由 EWS 返回作为电子邮件。 EWS 托管 API 可实现所有这些项类型。
  
> [!NOTE]
> 响应对象仅由客户端发送响应接收来自其他人的项目中的服务器。 不存在 Exchange 数据库中。 
  
## <a name="what-are-properties-in-ews"></a>EWS 中的属性是什么？
<a name="WhatAreEWSProperties"> </a>

EWS 架构描述了 EWS 客户端和 Exchange 之间发送的数据。 架构的大型一部分介绍您可以访问 Exchange 数据库中的项目和文件夹属性。 EWS 架构描述了 Exchange 数据库属性可供您的应用程序的 XML 表示形式。 实际属性，在该属性是可用，什么表单它们采用，然后返回，因基于您尝试执行操作的值。 例如， **Body**属性将在**FindItem**操作中，仅返回首先 512 个字符，但**GetItem**操作返回的项的完整文本。 尽管大多数属性都可设置并且可供检索，但仅通过 Exchange 设置某些属性。 每个属性以 XML 格式架构中存在以下任意反映属性，其存储在 Exchange 数据库，或计算从 Exchange 数据库中存储的属性。 **Subject**属性是属性的可设置; 的示例文件夹上的**UnreadCount**属性是计算属性的示例。 一组核心属性共有的核心项目类型。 
  
以下因素将确定您的应用程序获取从 Exchange 设置该属性： 
  
- 正在呼叫您的应用程序操作
    
- 基本响应形状
    
- 项目类型
    
- 指定的属性路径
    
务必了解这些不同因素如何影响您可以访问的数据。 作为和更早版本，提到的**Body**属性的示例一些信息是根据各种因素一定条件下可用。 了解这些因素可能节省时间通过帮助您选择正确的选项来访问所需的信息。 可以发现哪些属性可访问，您将需要测试这些因素，以便确定如何访问属性应用程序的需要。 本节介绍这些不同因素如何影响在 EWS 响应中返回的属性。 
  
### <a name="ews-response-shapes"></a>EWS 响应形状

Exchange 存储大量项目的信息。 有时，您的应用程序不需要的所有的信息，并在许多情况下，最好不是要获取其所有。 [EWS 响应形状](property-sets-and-response-shapes-in-ews-in-exchange.md)，也称为属性形状，指示从服务器返回的属性。 响应形状的核心元素是基本形状。 基本形状是强类型的项目的默认预设的属性包。 EWS 托管 API 的基本形状等同于[BasePropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx)。 EWS 包括三个默认响应形状。
  
**表 2。默认响应形状**

|**默认响应形状名称**|**EWS 托管 API 等效项**|**说明**|
|:-----|:-----|:-----|
|IdOnly  <br/> |BasePropertySet.IdOnly 值  <br/> |返回 EWS 标识符和更改密钥。 除非客户端使用由 AllProperties 或默认形状的所有属性都返回，使用 IdOnly 形状以及如何通过使用**属性集**类上设置以下属性路径指定其他属性。 大多数应用程序应使用 IdOnly 响应形状与指定的其他属性。 这会减少未使用客户端请求的数据量。  <br/> |
|默认  <br/> |N/A  <br/> |一组标准属性项类型。 如果您的应用程序使用的所有属性，则仅使用此响应形状。  <br/> |
|AllProperties  <br/> |BasePropertySet.FirstClassProperties 值  <br/> |比默认形状属性一大组。 尽管名称可以看出它，此选项不项目上返回所有属性。 设置此属性返回客户端应用程序最常使用的属性。 如果您需要其他属性，您可以将这些请求由其属性路径。  <br/> 如果您的应用程序不使用与此响应形状返回的所有属性，则都使用 IdOnly 响应形状与指定的其他属性。  <br/> |
   
许多 EWS 操作返回项和其属性。 无论您指定的响应形状，不同操作可以返回不同的属性集。 不同项目类型也返回不同的属性，具体取决于操作和指定的响应形状。 以下操作使用响应形状来标识要返回的属性。
  
**表 3。使用响应形状的操作**

|**EWS 操作**|**EWS 托管的 API 方法**|
|:-----|:-----|
|[GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |[ExchangeService.GetConversationItems 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |
|[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |[Folder.Bind 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |
|[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |[Item.Bind 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [ExchangeService.BindToItems 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |
|[FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |[ExchangeService.FindConversation 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |
|[FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |[Folder.FindFolders 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindFolders 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |
|[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |[Folder.FindItems 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindItems 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |
|[FindPeople](http://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |未实现。  <br/> |
|[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |[ExchangeService.ResolveNames 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |
|[SearchMailboxes](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService.SearchMailboxes 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSearchMailboxes 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsearchmailboxes%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderHierarchy 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderItems 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
属性形状是一个基本方式来标识您希望应用程序返回的属性。 有时，但是，您的应用程序需要更精细的一组特定属性。 为此，您可以使用属性路径。
  
### <a name="choose-properties-by-their-property-path"></a>选择属性按属性路径

EWS 属性路径是用于标识的请求或响应中的属性的元数据。 
  
**表 4。属性路径类型**

|**属性路径类型**|**架构类型**|**EWS 托管 API 实现**|**说明**|
|:-----|:-----|:-----|:-----|
|FieldUri  <br/> |PathToUnindexedFieldType  <br/> |从[ServiceObjectSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobjectschema%28v=exchg.80%29.aspx)继承的类型。  <br/> |最常见的属性路径。 EWS 托管 API 中的**属性集**对象上指定 FieldUri 属性路径。 大多数 EWS 属性可指定 FieldUri 属性路径。 介绍了 EWS 架构中 UnindexedFieldURIType。  <br/> FieldUri 属性路径 XML 如下所示：  <br/> ```XML<FieldURI FieldURI="item:Subject"/>```此属性路径是 ItemSchema.Subject EWS 托管 API 中的等效项。  <br/> |
|IndexedFieldUri  <br/> |PathToIndexedFieldType  <br/> |从[ItemSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx)继承的类型。  <br/> |标识需要可用于指定要返回的值的属性索引的词典属性。 属性可以具有多个值时，请使用此路径。 介绍了 EWS 架构中的**DictionaryURIType**属性。 EWS 托管 API 中的**属性集**对象上指定**DictionaryURIType**属性路径。  <br/> IndexedFieldUri 属性路径 XML 如下所示：  <br/> ```XML<IndexedFieldURI FieldURI="contacts:PhysicalAddress:Street FieldIndex="Home"/>```|
|ExtendedFieldUri  <br/> |PathToExtendedFieldType  <br/> |[ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |标识标识项目的自定义或非架构化属性扩展的属性定义。  <br/> ExtendedFieldUri 属性路径 XML 如下所示：  <br/> ```XML<ExtendedFieldURI> PropertyTag="0x1234" PropertyType="Integer" />```|
|ExceptionFieldUri  <br/> |ExceptionFieldURI  <br/> |[服务](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) <br/> |指定与 EWS 响应中的错误关联的属性。 介绍了 EWS 架构中的**ExceptionPropertyURIType**类型。 这只发生在您正在使用日历定期模式时，会发生的错误响应的**MessageXml**元素。  <br/> |
   
作为最佳实践，当您请求属性，使用 IdOnly 基本形状 (EWS 托管 API 的[BasePropertySet.IdOnly](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) )，然后请求仅应用程序需要通过指定的属性路径的属性。 
  
### <a name="schematized-properties"></a>架构化的属性

通过 EWS 架构描述的大多数 EWS 客户端所需的属性。 Types.xsd 架构中找到的主文件夹和项目类型定义，其中包含的属性定义。 以下架构类型包含您可以使用的大多数对象的属性定义。
  
**表 5。包含属性定义的架构类型**

|**EWS 架构类型**|**EWS 托管 API 类型等效项**|**定义...**|
|:-----|:-----|:-----|
|**ItemType** <br/> |[项类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) <br/> |基本项的 type 属性设置。 此类型可以创建从客户端，而由 Exchange 永远不会返回。 Exchange 返回 MessageType 对象的所有泛型对象。  <br/> |
|**MessageType** <br/> |[EmailMessage 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |电子邮件消息对象的属性集和为所有的通用对象的属性。  <br/> |
|**CalendarItemType** <br/> |[约会类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |日历项目属性设置;这包括单个和定期约会。  <br/> |
|**ContactItemType** <br/> |[联系类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |联系人项目的属性集。  <br/> |
|**DistributionListType** <br/> |[ContactGroup 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |个人通讯组列表属性设置。  <br/> |
|**MeetingMessageType** <br/> |[MeetingMessage 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingmessage%28v=exchg.80%29.aspx) <br/> |会议消息类型属性设置。  <br/> |
|**MeetingRequestMessageType** <br/> |[MeetingRequest 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequest%28v=exchg.80%29.aspx) <br/> |会议请求 type 属性设置。  <br/> |
|**MeetingResponseMessageType** <br/> |[MeetingResponse 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingresponse%28v=exchg.80%29.aspx) <br/> |会议响应 type 属性设置。  <br/> |
|**MeetingCancellationMessageType** <br/> |[MeetingCancellation 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingcancellation%28v=exchg.80%29.aspx) <br/> |会议取消 type 属性设置。  <br/> |
|**TaskType** <br/> |[任务类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |任务 type 属性设置。  <br/> |
|**PostItemType** <br/> |[PostItem 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |Postitem 的类型属性集。  <br/> |
|**FolderType** <br/> |[文件夹类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |文件夹 type 属性设置。  <br/> |
|**CalendarFolderType** <br/> |[CalendarFolder 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |SearchFolder 类型属性集。  <br/> |
|**ContactsFolderType** <br/> |[ContactsFolder 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |ContactsFolder 类型属性集。  <br/> |
|**SearchFolderType** <br/> |[SearchFolder 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |SearchFolder 类型属性集。  <br/> |
|**TasksFolderType** <br/> |[TasksFolder 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |TasksFolder 类型属性集。  <br/> |
|**UserConfigurationType** <br/> |[UserConfiguration 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration%28v=exchg.80%29.aspx) <br/> |UserConfiguration 类型属性集。  <br/> |
   
足够的多个应用程序中的 EWS 架构的属性时，您不能使用仅中所述架构中实现一些方案。 对于这些方案中，您可以扩展的属性。 
  
### <a name="extended-properties-aka-non-schematized-properties"></a>扩展的属性 （也称为非架构化属性）

扩展的属性使您能够创建自定义属性，您可以访问授予项目和 Exchange 存储中未定义 EWS 架构中的文件夹的属性。 您可以使用这些访问 Exchange 数据库中的本机 MAPI 项和文件夹属性。 您可以使用扩展的属性访问所有架构化的属性，因为隐式，这些架构化的属性是只是 Exchange 数据库中的 MAPI 属性。 
  
PathToExtendedFieldType 架构类型，位于 types.xsd 架构定义表示扩展的属性的 XML。 此架构类型定义中 XML 实例; [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素换句话说，它定义之间的服务和客户端发送的 XML。 ExtendedPropertyType 架构类型定义[ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素和值或包含扩展的属性的值的数组。 下表显示近似 XML 的扩展属性的映射和如何实现 EWS 托管 API 中的项。 
  
**表 6。扩展的属性中 EWS 托管 API 实施的 XML**

|**EWS 托管 API 实现**|**它包含的内容**|**映射到**|
|:-----|:-----|:-----|
|[Item.ExtendedProperties 属性](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.extendedproperties%28v=exchg.80%29.aspx) <br/> |在项目上的扩展属性的集合。  <br/> |在项目上的扩展属性的一个或多个实例。  <br/> |
|[ExtendedProperty 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedproperty%28v=exchg.80%29.aspx) <br/> |扩展的属性定义和值。  <br/> |ExtendedPropertyType 架构类型。  <br/> |
|[ExtendedPropertyDefinition 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |扩展的属性定义。  <br/> |PathToExtendedFieldType 架构类型。  <br/> |
   
如果您想要了解有关如何在您的应用程序中使用扩展的属性，您可以浏览下面的代码示例： 
  
- [MFCMapi](http://mfcmapi.codeplex.com/)
    
- [Exchange 2013： 以编程方式设置自定义 X 标头](http://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Exchange 2013： 根据属性标记访问属性](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-719875ac)
    
- [Exchange 2013： 通过其标识符来访问的命名的属性](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-02dbe22f)
    
- [Exchange 2013： 通过其名称来访问的命名的属性](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-6556e183)
    
- [Exchange 2013： 访问的属性的属性集 GUID 和名称](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-4021f971)
    
- [Exchange 2013： 创建自定义以编程方式扩展属性](http://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)
    
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [在 Exchange 使用 EWS 的设置 x 标头](how-to-provision-x-headers-by-using-ews-in-exchange.md)
    
- [EWS 属性相关错误](ews-property-related-errors.md)
    
## <a name="see-also"></a>另请参阅


- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [MFCMapi](http://mfcmapi.codeplex.com/)
    

