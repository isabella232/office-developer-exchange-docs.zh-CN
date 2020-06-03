---
title: 使用 EWS 在 Exchange 公用文件夹访问。
manager: sethgros
ms.date: 7/17/2015
ms.audience: Developer
ms.assetid: d9372057-1deb-45de-8f98-b9149604429a
description: 了解如何使用 EWS 和 EWS 托管 API 访问公用文件夹并路由 Exchange 中的公用文件夹请求。
localization_priority: Priority
ms.openlocfilehash: e921a77b250e11e974b0c47b1d28a8e020837d44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460209"
---
# <a name="public-folder-access-with-ews-in-exchange"></a>使用 EWS 在 Exchange 公用文件夹访问。

了解如何使用 EWS 和 EWS 托管 API 访问公用文件夹并路由 Exchange 中的公用文件夹请求。
  
公用文件夹提供组织中的用户可以访问的项目的共享存储库。 Office 365、Exchange Online 和本地版本的 Exchange 从 Exchange 2013 开始引入了一个新的公用文件夹体系结构。 Exchange 中的公用文件夹使用专用邮箱设计（而不是公用文件夹数据库）来存储公用文件夹层次结构和公用文件夹内容。 公用文件夹权限通过基于角色的访问控制（RBAC）进行管理。
  
客户端访问技术（如 Exchange Web 服务（EWS）和 EWS 托管 API）提供对公用文件夹层次结构和公用文件夹数据库中的内容项目的编程访问。 本文提供了有关如何使用 EWS 和 EWS 托管 API 访问公用文件夹和公用文件夹和公用文件夹数据的信息。 
  
## <a name="ews-operations-and-ews-managed-api-methods-for-public-folder-access"></a>用于公用文件夹访问的 EWS 操作和 EWS 托管 API 方法
<a name="bk_functionality"> </a>

大多数核心 EWS 操作都支持公用文件夹访问。 您可以使用下表中列出的文件夹和项目操作以及 EWS 托管的 API 方法来处理公用文件夹。
  
有关 EWS 托管 API 方法的信息，请参阅[Ews 托管 api 命名空间](https://msdn.microsoft.com/library/jj220535%28v=exchg.80%29.aspx)。
  
|**EWS 操作**|**EWS 托管的 API 方法**|
|:-----|:-----|
|[CreateFolder 操作](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |**文件夹. Save （）** <br/> |
|[UpdateFolder 操作](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |**Folder. Update （）** <br/> |
|[DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |**Folder。 Delete （）** <br/> |
|[MoveFolder 操作](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx)<sup>1</sup> <br/> |**Folder. Move （）** <br/> |
|[CopyFolder 操作](https://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx)<sup>2</sup> <br/> |**Folder （）** <br/> |
|[GetFolder 操作](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |**文件夹绑定（）** <br/> |
|[EmptyFolder 操作](https://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx)<sup>3</sup> <br/> |**Folder。空（）** <br/> |
|[FindFolder 操作](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |**ExchangeService FindFolders （）** <br/> **FindFolders （）** <br/> |
|[CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |**Item. Save （）** <br/> |
|[MoveItem 操作](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |**Item。 Move （）** <br/> |
|[CopyItem 操作](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |**Item. Copy （）** <br/> |
|[UpdateItem 操作](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |**Item。 Update （）** <br/> |
|[DeleteItem 操作](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |**Item。 Delete （）** <br/> |
|[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)<sup>4</sup> <br/> |**ExchangeService FindItems （）** <br/> **FindItems （）** <br/> |
|[GetItem 操作](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |**Item. Bind （）** <br/> |
|[ConvertId 操作](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx)<sup>5</sup> <br/> |**ExchangeService ConvertId （）** <br/> **ExchangeService ConvertIds （）** <br/> |
   
<sup>1</sup>在从 exchange 2013 开始的 exchange 版本中，在公用文件夹和私有文件夹之间移动文件夹的版本不可用。 
  
<sup>2</sup>此操作仅适用于 exchange server 2007 和 exchange server 2010 中的公用文件夹。 
  
<sup>3</sup>此操作仅适用于 Exchange 2010 中的公用文件夹。 
  
<sup>4</sup>通过从 exchange 2013 开始的 exchange 版本中支持查询字符串搜索选项，在单个公用文件夹中对单个公用文件夹中的全文索引搜索。 
  
<sup>5</sup> ConvertId 操作不能将公用文件夹标识符从 EWS 标识符正确转换为存储标识符。 您可以手动更新作为[解决方法](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx#bk_usingConvertId)返回的标识符。
  
对于从 Exchange 2013 开始的 Exchange 版本中的公用文件夹，不支持或部分支持以下操作：
  
- **CopyFolder** （不支持）。 可以将**CreateFolder**与**CopyItems**操作一起使用，以实现**CopyFolder**操作功能。 
    
- **EmptyFolder** （不支持）。 可以将**FindItem**与**DeleteItem**操作一起使用，以实现**EmptyFolder**操作功能。 
    
- **MoveFolder** （部分受支持）。 无法在私有和公用文件夹之间移动文件夹。 您可以在 Exchange 2007 和 Exchange 2010 中的私人文件夹和公用文件夹之间移动文件夹。 您可以在 Exchange 的所有版本中移动公用文件夹内的文件夹。 
    
EWS 和 EWS 托管 API 不支持用于公用文件夹的以下功能：
  
- 使用**SyncFolderHierarchy**。 使用**FindFolder**、 **GetFolder**和**SyncFolderItems**操作在公用文件夹邮箱中同步项目和文件夹。 
    
- 对公用文件夹层次结构的深层遍历搜索。 使用递归**FindFolder**操作调用遍历公用文件夹层次结构。 
    
- 使用**CreateFolderPath**操作创建公用文件夹的文件夹层次结构。 当您针对公用文件夹邮箱时，您需要在不同的文件夹层次结构中对每个文件夹级别使用**CreateFolder**操作。 
    
- 使用**CreateItem**操作保存已发送电子邮件的副本。 而是使用**MoveItem**操作将邮件的副本移动到公用文件夹中。 
    
## <a name="scenarios-for-using-ews-and-the-ews-managed-api-to-work-with-public-folders"></a>使用 EWS 和 EWS 托管 API 处理公用文件夹的方案
<a name="bk_scenarios"> </a>

公用文件夹为 Exchange 邮箱用户启用了许多重要的方案。 您可以通过使用 EWS 和 EWS 托管 API 为用户实现用于访问和使用公用文件夹及其内容的自定义解决方案。 
  
### <a name="programmatically-access-email-messages-that-have-been-sent-to-distribution-lists"></a>以编程方式访问已发送到通讯组列表的电子邮件

Exchange 邮箱用户可以使用公用文件夹来存储发送到通讯组列表的电子邮件。 这是保存通讯组列表历史记录的简便方法。 您可以使用 EWS 中的[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)，或使用 EWS 托管 API 中的**ExchangeService （）** 和**Folder FindItems （）** 方法来访问存储的通讯组列表电子邮件。 
  
### <a name="share-important-email-messages-and-other-mailbox-items"></a>共享重要的电子邮件和其他邮箱项目

邮箱用户可以将公用文件夹用作邮箱项目的共享存储库。 组织中的不同用户可以通过使用公用文件夹来共享重要的电子邮件或联系人。 EWS 可提供对这些共享邮箱项目的访问权限。 您可以使用 EWS 中的[MoveItem 操作](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)或在 EWS 托管 API 中的**Item （）** 方法将电子邮件、联系人和其他邮箱项目移入和移出公用文件夹。 
  
### <a name="public-discussions-with-post-items"></a>包含帖子项的公共讨论

公用文件夹是用于发布项目的方便容器。 发布项提供了一种使用对话对话的方法，而无需在用户之间发送电子邮件。 用户可以使用公用文件夹和发布项目来托管和维护组织中不同邮箱用户之间的线程对话。 这样，邮箱用户可以访问使用 post 项目的会话的共享历史记录，即使它们不是会话的一部分也是如此。 您可以使用 ews 托管 API 中的[CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)或在 EWS 托管 API 中的**Item （）** 方法来创建和响应存储在公用文件夹中的发布项目。 
  
## <a name="routing-public-folder-requests"></a>路由公用文件夹请求
<a name="bk_routing"> </a>

公用文件夹内容可以存储在多个邮箱服务器上。 公用文件夹层次结构可以存储在一个邮箱上，而公用文件夹的内容存储在另一个邮箱中。 每个服务器可以与请求信息的用户的邮箱服务器不同。 在这些情况下，重要的是要在公用文件夹请求中包含额外的 X-anchormailbox 和 PublicFolderMailbox 标头，以接收有关公用文件夹的准确信息。
  
X-X-anchormailbox 和 X-PublicFolderMailbox 的值可能有所不同，具体取决于您是否在执行与文件夹层次结构或文件夹内容相关的请求。 下表列出了每个 EWS 托管 API 方法或 EWS 操作应遵循的过程。
  
**用于路由公用文件夹请求的 EWS 托管 API 方法和 EWS 操作**

|**调用这些方法时**|**调用这些操作时**|**使用此过程**|
|:-----|:-----|:-----|
|[FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [文件夹。删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [文件夹。更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder。 Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |路由公用文件夹层次结构请求  <br/> |
|[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [项。复制](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item。 Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [文件夹。绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |路由公用文件夹内容请求  <br/> |
   
## <a name="version-differences"></a>版本差异
<a name="VersionDifferences"> </a>

在 Exchange 2007 和 Exchange 2010 中，当将公用文件夹标识符从 EWS 标识符转换为存储标识符时， **ConvertId**操作将按预期方式工作。 
  
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [公用文件夹限制](https://technet.microsoft.com/library/dn594582%28v=exchg.150%29.aspx)
    
- [FAQ：公用文件夹](https://technet.microsoft.com/library/jj552408.aspx)
    
- [公用文件夹过程](https://technet.microsoft.com/library/jj657481.aspx)
    

