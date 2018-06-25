---
title: 文件夹和 Exchange 中的 EWS 中的项目
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9d8cf6fa-85a4-45ac-8165-e4d3ab92594e
description: 了解有关文件夹和邮箱项目以及如何您 EWS 托管 API 或 EWS 客户端代表它们。
ms.openlocfilehash: a3358844f2317c9b0462456ff7d2f38442c98ee3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752744"
---
# <a name="folders-and-items-in-ews-in-exchange"></a>文件夹和 Exchange 中的 EWS 中的项目

了解有关文件夹和邮箱项目以及如何您 EWS 托管 API 或 EWS 客户端代表它们。
  
文件夹是 Exchange 邮箱的组织元素。 文件夹可以包含邮箱项目，如电子邮件、 联系人、 约会、 会议和任务，也可以包含其他文件夹。 Exchange 包括不同类型的文件夹，但类似于每个其他文件夹类型。 主要区别是项的它们包含的类型。
  
项目，但是，具有唯一的类型。 每个项目类型都有一组不同的属性或架构定义它。 在本文中，我们将讨论的文件夹和可用的项目和它们之间的差异的类型。

<a name="bk_folders"> </a>

## <a name="folders"></a>文件夹

从同一个基类或基类型、 EWS 托管 API 中的[文件夹](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=EXCHG.80%29.aspx)类或 EWS 中的[文件夹](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)类型派生的所有文件夹。 下图显示的 EWS 托管 API 类和 EWS 类型。 
  
**图 1。EWS 托管 API 文件夹类和 EWS 文件夹类型**

![显示从 EWS 托管 API 文件夹类生成的类以及从 EWS 文件夹类型生成的类型，所有类和类型命名为 CalendarFolder、ContactsFolder、SearchFolder 和 TasksFolder。](media/Ex2013_Folder_OverviewTypes.png)
  
每个文件夹类和文件夹类型的主要区别是项目的文件夹的，可以仅在每种类型中创建特定类型。 区别之一是在客户端文件夹中显示信息的方式。 例如，Exchange 允许您在日历文件夹中创建约会。 后您创建它们，但 Outlook 不会显示这些，您可以将其他类型的项移动到日历文件夹。 Outlook 仅显示日历文件夹，[即使在文件夹中存在的其他类型的项](folders-and-items-in-ews-in-exchange.md#bk_item)中的日历项目，如约会和会议。 
  
**表 1。EWS 托管 API 文件夹类和 EWS 文件夹类型**

|**EWS 托管 API 类**|**EWS 类型**|**FolderClass 值**|**Contains**|**备注**|
|:-----|:-----|:-----|:-----|:-----|
|[Folder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |[Folder](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) <br/> |IPF。注释  <br/> |电子邮件或文件夹。  <br/> | 这是一般文件夹类或以下 EWS 托管 API [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)文件夹和 EWS [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)文件夹类型： <ul><li>  根 （IPM 子树）</li><li>NonIpmSubtree</li><li>Inbox</li><li>已删除的项目</li><li>草稿</li><li>日记</li><li>笔记  </li><li>发件箱</li><li>已发送的邮件</li><li>邮件文件夹</li><li>垃圾邮件</li><li>语音邮件</li></ul> |
|[CalendarFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |[CalendarFolder](http://msdn.microsoft.com/library/48687a78-e757-4c04-9641-bf4302c6b565%28Office.15%29.aspx) <br/> |IPF。约会  <br/> |约会和会议。  <br/> |当用户响应会议请求时，该约会被添加到 EWS 托管 API [WellKnownFolderName.Calendar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)或 EWS [DistinguishedFolderId.CalendarFolder](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)仅。 这些是支持与会议请求和响应的自动进行交互的唯一文件夹。  <br/><br/>此文件夹类或文件夹类型支持的日历视图返回约会和会议使用 EWS 托管 API [Folder.FindItem](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx)方法和[CalendarView](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx)类中或 EWS [FindItem 基于开始日期和结束日期](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作和[CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)元素。  <br/> |
|[ContactsFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |[ContactsFolder](http://msdn.microsoft.com/library/6c299de8-2087-4aeb-8e66-2bc7586509a6%28Office.15%29.aspx) <br/> |IPF。联系人  <br/> |联系人和通讯组列表。  <br/> |无。  <br/> |
|[SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |[SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) <br/> |IPF。注释  <br/> |内容确定限制或筛选器。 搜索文件夹没有子文件夹。  <br/> |在搜索文件夹中; 实际上不包含符合搜索条件的邮件相反，它们是位于其他位置的邮箱中。  <br/> 若要确保在 Outlook 中搜索文件夹，请在 Finder 文件夹中创建。  <br/> |
|[TasksFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |[TasksFolder](http://msdn.microsoft.com/library/5a9a4612-8064-4986-b467-c44f268c64df%28Office.15%29.aspx) <br/> |IPF。任务  <br/> |包含要完成的工作项。  <br/> |无。  <br/> |
   
### <a name="folder-structure"></a>文件夹结构

文件夹提供邮箱结构。 这包括 IPM 子树，称为顶部的信息存储在 EWS，其中大多数用户与他们的邮箱进行交互，以及大多数用户永远不会看到，它们是非 IPM 子树或根中的 ews 中的系统文件夹。 下图显示了用户的文件夹结构，并指示哪些文件夹的用户的项目以及哪些是系统文件夹。
  
**图 2。邮箱中的项目和系统文件夹**

![显示根节点中的系统文件夹的示例，包括“收藏夹”、“查找工具”、“空闲/忙碌数据”和“最上层的信息文件”等。“最上层的信息文件”包含用户文件夹，如“日历”、“联系人等”。](media/Ex2013_Folder_OverviewSampleHierarchy.png)
  
### <a name="well-known-folders"></a>已知文件夹

邮箱中的文件夹，一些特殊文件夹。 这些相当于 EWS 托管 API 中的已知文件夹或可分辨的文件夹中的 ews。 这些文件夹的一些其中它们位于的文件夹结构，以及是否可以删除有文件夹名称，限制。 其他"常规"（非特殊） 文件夹不具有相同的限制。 很重要，因为它们根系统、 用户和搜索文件夹，并且适用于大多数实现要熟悉以下已知或可分辨文件夹。 
  
**表 2。主已知和可分辨文件夹**

|**友好名称**|**EWS 托管 API **WellKnownFolderName**值**|**EWS **DistinguishedFolderId**值**|**说明**|
|:-----|:-----|:-----|:-----|
|根 （非 IPM 子树）  <br/> |WellKnownFolderName.Root  <br/> |DistinguishedFolderId.root  <br/> |包含邮箱，也称为非 IPM 子树的根文件夹。 此文件夹具有没有父级，并且不能移动、 复制、 重命名或删除它。 每个消息存储库包含只有一个根文件夹。  <br/> |
|顶部的信息存储 （IPM 子树）  <br/> |WellKnownFolderName.MsgFolderRoot  <br/> |DistinguishedFolderId.msgfolderroot  <br/> |包含收件箱和其他用户文件夹。  <br/> |
|Finder （搜索文件夹）  <br/> |WellKnownFolderName.SearchFolders  <br/> |DistinguishedFolderId.searchfolders。  <br/> |包含在 Outlook 中可见的搜索文件夹。  <br/> |
   
EWS 托管 API [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.wellknownfoldername%28v=exchg.80%29.aspx)属性值的完整列表，请参阅[WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=EXCHG.80%29.aspx)枚举。 EWS **DistinguishedFolderId**值的完整列表，请参阅[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)。
  
### <a name="folder-properties"></a>Folder 属性

EWS 托管 API 在[文件夹属性](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder_properties%28v=exchg.80%29.aspx)是所有派生自基[文件夹](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=EXCHG.80%29.aspx)类。 和 EWS，所有文件夹都使用对[文件夹](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)类型可用的文件夹元素。 大多数与文件夹相关的属性和元素是简单 （父文件夹 ID、 显示名称等），但一些需要少量详细说明。 
  
下列说明适用于 EWS 托管 API [Folder.FolderClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.folderclass%28v=EXCHG.80%29.aspx)属性或 EWS [FolderClass](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx)元素： 
  
- 如果组、 属性或元素的值必须同意派生的类或文件夹的类型。 例如， **FolderClass**属性或元素不能指示文件夹是类时的联系人文件夹，或文件夹的类型指示文件夹是日历文件夹可以。 
    
- 您可以任一[创建文件夹](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma)的特定类型而不设置**FolderClass**属性或元素，也可以使用的一般文件夹类型创建一个文件夹，并指定**FolderClass**属性或元素。 这两个选项创建相同的结果。 
    
- 通过创建特定类型的文件夹或设置**FolderClass**属性或元素本身设置**FolderClass**值后，您无法更改它。 例如，不能更改 IPF。注意到 IPF 的文件夹。联系人文件夹。 但是，，可以将其更改为 IPF。Note.Contoso 文件夹。 
    
- 在不使用预定义的前缀之一的任何**FolderClass**值被视为 IPF。注意文件夹。 例如，IAmAFolderClass **FolderClass**值视为 IPF。注意文件夹。 
    
可扩展的文件夹类值。 这意味着，表 1 中列出的默认**FolderClass**值被视为前缀，您可以添加自定义值。 例如，您可以使用 IPF **FolderClass**值创建文件夹。Contact.Contoso，并将被视为联系人文件夹。 
  
您可以确定哪些权限客户端有文件夹，例如，删除、 读取和修改，使用 EWS 托管 API [Folder.EffectiveRights](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.effectiverights%28v=EXCHG.80%29.aspx)属性或 EWS [EffectiveRights](http://msdn.microsoft.com/library/bf5278eb-3a1a-4d27-9d16-b8be043bb023%28Office.15%29.aspx)元素。 
  
### <a name="public-folders"></a>公用文件夹

公用文件夹共享访问设计，并提供一种轻松、 有效的方法来收集、 组织信息及与您的工作组或组织中的其他人共享信息。 您可以使用公用文件夹对通讯组内容进行存档。 有关公用文件夹的详细信息，请参阅[在 Exchange 使用 EWS 访问公用文件夹](public-folder-access-with-ews-in-exchange.md)。

<a name="bk_hiddenfolders"> </a>

### <a name="hidden-folders"></a>隐藏文件夹

Exchange 邮箱的根路径上创建的所有文件夹已被都隐藏，并且您可以使用 EWS 托管 API 或 EWS 隐藏顶部信息存储下的其他文件夹。 有关隐藏的文件夹的详细信息，请参阅[Work with Exchange 中使用 EWS 隐藏文件夹](how-to-work-with-hidden-folders-by-using-ews-in-exchange.md)。 

<a name="bk_hiddenfolders"> </a>

### <a name="search-folders"></a>搜索文件夹

搜索文件夹是就像常规文件夹，除非它具有的属性或元素定义的搜索筛选器。 您可以在任何文件夹中的 Exchange 邮箱中创建搜索文件夹，并且您创建这些相同的方式创建任何其他文件夹。 但是，在 Outlook、 Outlook Web App 或 Outlook Live 中显示的搜索文件夹，使用 EWS 托管 API 创建的[SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)对象必须位于[WellKnownFolderName.SearchFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)文件夹和[SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx)使用 EWS 创建的类型必须位于[DistinguishedFolderId.SearchFolders](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)文件夹。 如果在其他位置创建搜索文件夹，则它仍然可用，您可以查看其自定义客户端应用程序中。 

<a name="bk_item"> </a>

## <a name="items"></a>项目

Exchange 中的 EWS 使用**项**来表示单个电子邮件、 约会、 会议、 联系人、 通讯组列表、 任务、 文章和邮箱中的其他项。 项目都是以下任意强类型，这意味着它们具有特定关联的类或架构或不强类型，也称为泛型项。 通用项目是 EWS 托管 API 和[项目](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx)类型中的 ews 中的[项目](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)对象。 常用项目类似于电子邮件、 联系人、 通讯组列表、 文章和任务强类型，您可以在其上设置特定的架构化的属性或元素。 
  
**表 3。强类型的项目**

|**EWS 托管 API 项类型**|**EWS 项元素**|
|:-----|:-----|
|[约会](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[Contact](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[Contact](http://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[ContactGroup](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |[DistributionList](http://msdn.microsoft.com/library/f65aea01-e870-44a2-8571-fa6c001341cc%28Office.15%29.aspx) <br/> |
|[EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[PostItem](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |[PostItem](http://msdn.microsoft.com/library/7727ed84-9591-4a1c-bb04-12129926499b%28Office.15%29.aspx) <br/> |
|[任务](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[任务](http://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
EWS 托管 API 的强类型项目从[项目](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=EXCHG.80%29.aspx)基类派生。 但是，您通常使用表 3 中列出的派生类型之一并不能使用**项**类直接。 当您处理[仅](http://msdn.microsoft.com/en-us/library/dd634001%28v=EXCHG.80%29.aspx)类，但是，您可能使用直接**项目**类的实例。 在这种情况下，应实现确定的**项**类的实例表示的存储区中的项目的类型的逻辑。 若要使用该项目，应使用表示项目的类的实例，绑定到项。 
  
### <a name="items-in-folders"></a>文件夹中的项目

有些文件夹具有限制及其可包含的项目的类型。 这些是 Exchange 邮箱数据库适用于文件夹，不客户端视图限制的限制。 
  
**表 4。文件夹的项目限制**

|**EWS 托管 API 文件夹类**|**EWS 文件夹类型**|**限制**|
|:-----|:-----|:-----|
|[文件夹基类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |[Folder](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) <br/> |仅可以泛型文件夹中创建新的 EWS 托管 API [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象和[PostItem](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx)对象或 EWS[消息](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx)类型或**PostItem**类型。 您可以将其他项目类型移入泛型文件夹，但客户端可能不显示它们。  <br/> |
|[CalendarFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |[CalendarFolder](http://msdn.microsoft.com/library/48687a78-e757-4c04-9641-bf4302c6b565%28Office.15%29.aspx) <br/> |仅可以在日历文件夹中创建新的 EWS 托管 API[约会](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象和 EWS[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)类型。 您可以将其他项目类型移动到日历文件夹中，但客户端可能不显示它们。  <br/> |
|[ContactsFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |[ContactsFolder](http://msdn.microsoft.com/library/6c299de8-2087-4aeb-8e66-2bc7586509a6%28Office.15%29.aspx) <br/> |仅可以在联系人文件夹中创建新的 EWS 托管 API[联系人](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx)和[ContactGroup](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx)对象，或 EWS[联系人](http://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx)类型或[DistributionList](http://msdn.microsoft.com/library/f65aea01-e870-44a2-8571-fa6c001341cc%28Office.15%29.aspx)类型。 您可以将其他项目类型移动到联系人文件夹中，但客户端可能不显示这些  <br/> |
|[SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |[SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) <br/> |没有限制。 项目不实际位于搜索文件夹中。它们位于其他位置的邮箱中。  <br/> |
|[TasksFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |[TasksFolder](http://msdn.microsoft.com/library/5a9a4612-8064-4986-b467-c44f268c64df%28Office.15%29.aspx) <br/> |仅可以在任务文件夹中创建新的 EWS 托管 API[任务](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx)对象或 EWS[任务](http://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx)类型。 您可以将其他项目类型移动到任务文件夹中，但客户端可能不显示这些  <br/> |

<a name="bk_upgrading"> </a>

## <a name="upgrading-from-earlier-product-versions"></a>从早期的产品版本升级

在大多数情况下，文件夹具有原封不动早期和当前的产品版本中。 但请注意，以前版本的 Exchange 使用托管的文件夹执行邮件记录管理 (MRM)。 Exchange Online、 Exchange Online 作为 Office 365 的一部分和版本的 Exchange 开头 Exchange 2013 用于 MRM 保留策略。 您还可以[升级托管文件夹使用保留策略](http://technet.microsoft.com/en-us/library/dd298032%28v=exchg.150%29.aspx)。 
  
早期和当前的产品版本中未更改的项目。

<a name="bk_inthissection"> </a>

## <a name="in-this-section"></a>本节内容

- [在 Exchange 使用 EWS 使用文件夹](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [通过在 Exchange EWS 使用隐藏文件夹](how-to-work-with-hidden-folders-by-using-ews-in-exchange.md)
    
- [通过在 Exchange 使用 EWS 来处理 Exchange 邮箱项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    
- [使用 EWS 在 Exchange 中删除项目](deleting-items-by-using-ews-in-exchange.md)
    
- [导出和导入在 Exchange 使用 EWS 的项目](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)   
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)   
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

