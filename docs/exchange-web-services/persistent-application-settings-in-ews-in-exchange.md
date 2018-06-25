---
title: 在 Exchange 中的 EWS 中的持久的应用程序设置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: 了解您 EWS 托管 API 或 EWS 应用程序可用于在 Exchange 中创建持久的自定义应用程序设置的不同选项。
ms.openlocfilehash: b384fd5608dc647950d7cd31e861e24c12e3316f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753005"
---
# <a name="persistent-application-settings-in-ews-in-exchange"></a>在 Exchange 中的 EWS 中的持久的应用程序设置

了解您 EWS 托管 API 或 EWS 应用程序可用于在 Exchange 中创建持久的自定义应用程序设置的不同选项。
  

  
可在邮箱中保留自定义客户端配置的邮箱，或文件夹和项同步的最简单方式是将应用程序设置存储在 Exchange 服务器上。 您可以确保这些设置适用于邮箱，使用下列选项之一： 
  
- 用户配置对象
    
- 扩展属性
    
- 自定义项
    
## <a name="what-are-my-options-for-creating-persistent-application-settings"></a>我创建持久的应用程序设置的选项是什么？
<a name="Options"> </a>

用户配置对象是最好的选择来存储 EWS 客户端应用程序的配置设置。 您还可以使用扩展属性或自定义项或所有这三个的组合。 选择您根据您的设置和您的设置是否需要可供其他应用程序范围的选项。
  
**表 1。用于创建基于范围持久的应用程序设置的建议的选项**

|**设置范围**|**使用...**|**通过访问**|
|:-----|:-----|:-----|
|项目  <br/> |对现有项扩展的属性。  <br/> |EWS 的任何应用程序。 仅限 EWS 的客户端知道属性标识符可以访问扩展的属性。  <br/> |
|Folder  <br/> |用户配置对象上的目标文件夹。 这是一个恰当的方式，以保存视图设置的文件夹。  <br/> |EWS 的任何应用程序。  <br/> |
|Mailbox  <br/> |用户配置对象默认 msgrootfolder 文件夹。  <br/> |EWS 的任何应用程序。  <br/> |
   
### <a name="user-configuration-objects"></a>用户配置对象
<a name="UserConfig"> </a>

用户配置对象是与邮箱中的文件夹关联的特殊项目。 用户配置对象，也称为相关联的文件夹项目，通常是保留应用程序设置，了最佳选项，尤其是与文件夹或邮箱关联的配置信息。 他们通常会不呈现给最终用户。 由于本身，他们可以存储数据流和数据词典，它们是理想的存储配置信息。 使用用户配置对象的最佳方式是存储在 XML 文档中的一组配置，然后将该信息保存的用户配置流属性之一。
  
用户配置对象访问不同的邮箱中存储的其他项类型。 您可以使用[Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) EWS 托管 API 方法或[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS 操作以查找所有项目，但您必须使用的**关联**搜索遍历选项都查找用户配置对象。 **关联**搜索遍历指示搜索结果应包含仅用户配置对象。 EWS 包含一组特定于用户配置对象的操作。 
  
**表 1。EWS 操作和用于处理用户配置对象的 EWS 托管 API 方法**

|**若要...**|**使用此 EWS 操作**|**使用此 EWS 托管 API 方法**|
|:-----|:-----|:-----|
|创建用户配置对象  <br/> |[CreateUserConfiguration 操作](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|获取用户配置对象  <br/> |[GetUserConfiguration 操作](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|更新用户配置对象  <br/> |[UpdateUserConfiguration 操作](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|删除用户配置对象  <br/> |[DeleteUserConfiguration 操作](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> 使用 EWS 创建用户配置对象具有[ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx)前缀开头"IPM。配置。"。 用户配置对象的**ItemClass**是用户配置对象前缀和用户配置对象名称。 您可以使用[Item.ItemClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS 托管 API 属性或**ItemClass** EWS 元素搜索已定义的用户配置对象。 
  
### <a name="extended-properties"></a>扩展属性
<a name="ExtendedProperties"> </a>

如果您想要在项目上存储配置信息，请使用[扩展属性](properties-and-extended-properties-in-ews-in-exchange.md)。 EWS，与 MAPI，不会返回项目的属性包。 这意味着 EWS 客户端必须知道查找和访问扩展的属性的扩展的属性标识符。 如果您需要在项目之外的用户配置对象上存储配置信息，请使用扩展的属性创建自定义属性可能适合您的解决方案。 扩展的属性，可以访问并不是设置的项的标准属性的一部分的属性存储信息。 
  
> [!IMPORTANT]
> Exchange 数据库架构具有有限数量的属性。 针对 Exchange 数据库属性标识符的最大数目是 32767。 如果您使用扩展的属性存储许多设置，我们建议使用一个扩展属性，以便不超过此最大存储这些设置。 
  
您可以使用[Item.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx) EWS 托管 API 方法或[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS 操作来设置用户配置对象的扩展的属性。 
  
### <a name="custom-items"></a>自定义项
<a name="CustomItems"> </a>

自定义项可用于存储信息。 可以重新使用现有的项目属性包含配置信息。 或者，您可以使用扩展的属性来定义您自己的应用程序的属性。 使用自定义项存储配置有以下好处： 
  
- 支持 EWS 的所有版本的 Exchange 工作。
    
- 如果未对项目使用扩展的属性，不计费 Exchange 属性预算。
    
## <a name="where-should-i-store-my-application-settings"></a>我的应用程序设置应存储在哪里？
<a name="ApplicationSettingsLocation"> </a>

邮箱文件夹和其中的项目位于根邮件文件夹中。 此文件夹由 EWS 托管 API 中的[WellKnownFolderName.msgfolderroot](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)值标识。 MAPI 术语中这相当的邮箱的 IPM 子树。 用户配置对象通常用于创建基于 UI 的设置，以便应用程序可以呈现基于用户访问的文件夹的视图设置。 在与文件夹关联的用户配置对象通常设置基于文件夹的视图设置。 但是，有时，您可能希望使您的应用程序的全局设置。 在这种情况下，您可以在根邮件文件夹中存储您的设置。 
  
大多数用户不是了解，通常不访问根邮箱文件夹。 此文件夹由 EWS 托管 API 中的[WellKnownFolderName.root](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)值标识。 MAPI 讲，这是等效的邮箱的非 IPM 子树。 信息的最终用户不直接访问存储在根邮箱文件夹。 您可能想要在此文件夹中存储应用程序设置，因为客户端应用程序不通常访问它。 
  
## <a name="version-differences"></a>版本差异
<a name="VersionDifferences"> </a>

用户配置对象位于 Exchange Online 中，作为 Office 365 的一部分和版本的 Exchange 启动 Exchange 2010 与 Exchange Online。
  
## <a name="see-also"></a>另请参阅


- [在 Exchange 中使用 EWS 管理持久的应用程序设置](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    
- [属性和交换中的 EWS 中的扩展的属性](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 使用文件夹](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [通过在 Exchange 使用 EWS 来处理 Exchange 邮箱项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    

