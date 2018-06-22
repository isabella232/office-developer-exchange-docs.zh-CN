---
title: 使用 EWS 在 Exchange 公用文件夹访问。
manager: sethgros
ms.date: 7/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d9372057-1deb-45de-8f98-b9149604429a
description: 了解如何使用 EWS 和 EWS 托管 API 访问公用文件夹和 Exchange 路由的公用文件夹请求。
ms.openlocfilehash: cfa089ba617dc760ed12883590e141debb5ecd9b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753010"
---
# <a name="public-folder-access-with-ews-in-exchange"></a>使用 EWS 在 Exchange 公用文件夹访问。

了解如何使用 EWS 和 EWS 托管 API 访问公用文件夹和 Exchange 路由的公用文件夹请求。
  
公用文件夹提供共享存储库的组织中的用户可以访问的项目。 Office 365 和 Exchange Online 中，启动与 Exchange 2013 的 Exchange 内部部署版本中引入公用文件夹的新体系的结构。 Exchange 中的公用文件夹使用专用的邮箱设计 （而不是公用文件夹数据库） 来存储公用文件夹层次结构和公用文件夹内容。 公用文件夹权限管理通过角色基于访问控制 (RBAC)。
  
客户端访问技术，如 Exchange Web Services (EWS) 和 EWS 托管 API 提供了公用文件夹层次结构和公用文件夹数据库中的内容项的编程访问。 本文提供有关如何使用 EWS 和 EWS 托管 API 访问公用文件夹和公用文件夹和公用文件夹数据的信息。 
  
## <a name="ews-operations-and-ews-managed-api-methods-for-public-folder-access"></a>EWS 操作和公用文件夹访问 EWS 托管 API 方法
<a name="bk_functionality"> </a>

大多数核心 EWS 操作支持公用文件夹进行访问。 您可以使用的文件夹和项目操作和下表中列出的 EWS 托管 API 方法处理公用文件夹。
  
有关 EWS 托管 API 方法的信息，请参阅[EWS 托管 API 的命名空间](http://msdn.microsoft.com/en-us/library/jj220535%28v=exchg.80%29.aspx)。
  
|**EWS 操作**|**EWS 托管的 API 方法**|
|:-----|:-----|
|[CreateFolder Operation](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |**Folder.Save()** <br/> |
|[UpdateFolder Operation](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |**Folder.Update()** <br/> |
|[DeleteFolder 操作](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |**Folder.Delete()** <br/> |
|[MoveFolder 操作](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx)<sup>1</sup> <br/> |**Folder.Move()** <br/> |
|[CopyFolder 操作](http://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx)<sup>2</sup> <br/> |**Folder.Copy()** <br/> |
|[GetFolder Operation](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |**Folder.Bind()** <br/> |
|[EmptyFolder 操作](http://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx)<sup>3</sup> <br/> |**Folder.Empty()** <br/> |
|[FindFolder Operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |**ExchangeService.FindFolders()** <br/> **Folder.FindFolders()** <br/> |
|[CreateItem 操作](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |**Item.Save()** <br/> |
|[MoveItem 操作](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |**Item.Move()** <br/> |
|[CopyItem 操作](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |**Item.Copy()** <br/> |
|[UpdateItem 操作](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |**Item.Update()** <br/> |
|[删除项操作](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |**Item.Delete()** <br/> |
|[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)<sup>4</sup> <br/> |**ExchangeService.FindItems()** <br/> **Folder.FindItems()** <br/> |
|[GetItem 操作](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |**Item.Bind()** <br/> |
|[ConvertId 操作](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx)<sup>5</sup> <br/> |**ExchangeService.ConvertId()** <br/> **ExchangeService.ConvertIds()** <br/> |
   
<sup>1</sup>公用文件夹和专用文件夹之间移动文件夹不是 Exchange 开头 Exchange 2013 版本中可用。 
  
<sup>2</sup>此操作仅适用于 Exchange Server 2007 和 Exchange Server 2010 中的公用文件夹。 
  
<sup>3</sup>此操作仅适用于公用文件夹在 Exchange 2010。 
  
<sup>4</sup>开头 Exchange 2013 的 Exchange 版本中受支持的查询字符串搜索选项通过单个公用文件夹内的全文索引的搜索。 
  
<sup>5</sup> ConvertId 操作不能正确转换公用文件夹标识符从 EWS 标识符与存储标识符。 您可以手动更新作为[解决方法](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx#bk_usingConvertId)返回的标识符。
  
以下操作不受支持，或部分受支持的版本的 Exchange 开头 Exchange 2013 中的公用文件夹：
  
- **CopyFolder**（不支持）。 您可以使用与**CopyItems**操作**CreateFolder**实现**CopyFolder**操作功能。 
    
- **EmptyFolder**（不支持）。 您可以使用**FindItem** **删除项**操作来实现**EmptyFolder**操作功能。 
    
- **MoveFolder**（部分支持）。 不能专用和公用文件夹之间移动文件夹。 您可以在 Exchange 2007 中的专用和公用文件夹和 Exchange 2010 之间移动文件夹。 您可以在所有版本的 Exchange 公用文件夹内移动文件夹。 
    
EWS 和 EWS 托管 API 不支持以下功能的公用文件夹：
  
- 使用**SyncFolderHierarchy**。 使用**FindFolder**、 **GetFolder**和**SyncFolderItems**操作同步公用文件夹邮箱中项目和文件夹。 
    
- 公用文件夹层次结构的深度遍历搜索。 使用递归**FindFolder**操作调用遍历公用文件夹层次结构。 
    
- 使用**CreateFolderPath**操作创建公用文件夹的文件夹层次结构。 您将需要使用不同的文件夹层次结构中的每个文件夹级别的**CreateFolder**操作时目标公用文件夹邮箱。 
    
- 使用**CreateItem** operation 保存发送的电子邮件的副本。 而是使用**MoveItem**操作移动到的公用文件夹的邮件的副本。 
    
## <a name="scenarios-for-using-ews-and-the-ews-managed-api-to-work-with-public-folders"></a>使用 EWS 和 EWS 托管 API 来使用公用文件夹方案
<a name="bk_scenarios"> </a>

公用文件夹启用 Exchange 邮箱用户的许多重要的方案。 您可以通过使用 EWS 和 EWS 托管 API 来实现自定义解决方案的访问和使用公用文件夹和及其内容为用户提供强大功能。 
  
### <a name="programmatically-access-email-messages-that-have-been-sent-to-distribution-lists"></a>以编程方式访问电子邮件已发送到通讯组列表

Exchange 邮箱用户可以使用公用文件夹来存储电子邮件发送到通讯组列表。 这是一种将通讯组列表历史记录保存简便方法。 您可以使用 ews [FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)或 EWS 托管 API 中的**ExchangeService.FindItems()** 和**Folder.FindItems()** 方法访问存储通讯组列表的电子邮件。 
  
### <a name="share-important-email-messages-and-other-mailbox-items"></a>共享重要的电子邮件和其他邮箱项目

邮箱用户可用作公用文件夹共享存储库的邮箱项目。 组织中的不同用户可以通过使用公用文件夹共享重要的电子邮件或联系人。 EWS 可以提供这些共享的邮箱项目的访问权限。 您可以使用 ews [MoveItem 操作](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)或 EWS 托管 API 中的**Item.Move()** 方法和注销的公用文件夹移动电子邮件、 联系人和其他邮箱项目。 
  
### <a name="public-discussions-with-post-items"></a>公共公告项讨论

公用文件夹是公告项的一个方便的容器。 公告项提供一种方式使用而无需发送电子邮件用户之间的线程的对话。 用户可以使用公用文件夹，并发布项目承载和维护组织中的不同的邮箱用户之间的线程的对话。 这种方式，邮箱用户可以访问共享的使用投递项目，即使它们不是部分对话的对话历史记录。 您可以使用 EWS 中的[CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)或 EWS 托管 API 中的**Item.Save()** 方法，以创建并发布的公用文件夹中存储的项目的响应。 
  
## <a name="routing-public-folder-requests"></a>公用文件夹请求路由
<a name="bk_routing"> </a>

公用文件夹内容可以存储在多个邮箱服务器上。 公用文件夹层次结构可以存储上一个邮箱，而公用文件夹的内容存储在另一个。 每个服务器可以为不同的邮箱服务器的请求信息的用户。 在这些情况下，务必要包含在您的公用文件夹请求接收有关公用文件夹的正确信息中的其他的 X AnchorMailbox 和 X PublicFolderMailbox 标头。
  
X AnchorMailbox 和 X PublicFolderMailbox 的值可以有所不同具体取决于是否正在执行请求与文件夹层次结构或文件夹内容。 下表标识了哪些过程需遵循的每个 EWS 托管 API 方法或 EWS 操作。
  
**EWS 托管 API 方法和路由的公用文件夹请求的 EWS 操作**

|**当调用这些方法**|**调用这些操作时**|**使用此过程**|
|:-----|:-----|:-----|
|[Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |公用文件夹层次结构请求路由  <br/> |
|[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item.Copy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item.Move](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [删除项](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |公用文件夹内容请求路由  <br/> |
   
## <a name="version-differences"></a>版本差异
<a name="VersionDifferences"> </a>

在 Exchange 2007 和 Exchange 2010 中，按预期的 EWS 标识符的公用文件夹标识符转换为存储标识符时，将工作**ConvertId**操作。 
  
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [公用文件夹限制](http://technet.microsoft.com/en-us/library/dn594582%28v=exchg.150%29.aspx)
    
- [常见问题： 公用文件夹](http://technet.microsoft.com/en-us/library/jj552408.aspx)
    
- [公用文件夹过程](http://technet.microsoft.com/en-us/library/jj657481.aspx)
    

