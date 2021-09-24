---
title: 在交换 EWS 持久应用程序设置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: 了解您的 EWS 托管 API 或 EWS 应用程序可用于在 Exchange 中创建自定义应用程序设置的不同选项。
ms.openlocfilehash: 3fdc7ad3d5acabf6b498743afe8d93f0eff048c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516136"
---
# <a name="persistent-application-settings-in-ews-in-exchange"></a>在交换 EWS 持久应用程序设置

了解您的 EWS 托管 API 或 EWS 应用程序可用于在 Exchange 中创建自定义应用程序设置的不同选项。
  

  
使自定义客户端配置保持邮箱或邮箱中的文件夹和项目同步的最简单方法是将应用程序设置存储在 Exchange 服务器上。 您可以通过使用下列选项之一来确保邮箱的这些设置持续存在： 
  
- 用户配置对象
    
- 扩展属性
    
- 自定义项
    
## <a name="what-are-my-options-for-creating-persistent-application-settings"></a>我用于创建永久应用程序设置的选项是什么？
<a name="Options"> </a>

用户配置对象是存储 EWS 客户端应用程序的配置设置的最佳选项。 您还可以使用扩展属性或自定义项，或所有这三者的组合。 根据设置的范围以及你的设置是否需要可供其他应用程序使用来选择你的选项。
  
**表 1.基于作用域创建永久应用程序设置的推荐选项**

|**设置范围**|**使用...**|**访问者**|
|:-----|:-----|:-----|
|Item  <br/> |现有项目的扩展属性。  <br/> |任何 EWS 应用程序。 只有知道属性标识符的 EWS 客户端可以访问扩展属性。  <br/> |
|Folder  <br/> |目标文件夹上的用户配置对象。 这是保存文件夹视图设置的良好方法。  <br/> |任何 EWS 应用程序。  <br/> |
|邮箱  <br/> |默认 msgrootfolder 文件夹中的用户配置对象。  <br/> |任何 EWS 应用程序。  <br/> |
   
### <a name="user-configuration-objects"></a>用户配置对象
<a name="UserConfig"> </a>

用户配置对象是与邮箱中的文件夹关联的特殊项目。 用户配置对象（也称为文件夹关联项目）通常是保留应用程序设置的最佳选项，尤其是在配置信息与文件夹或邮箱关联时。 它们通常不会向最终用户公开。 因为它们可以在本机存储数据流和数据字典，所以非常适合存储配置信息。 使用用户配置对象的最佳方法就是将一组配置存储在 XML 文档中，然后将该信息保存在用户配置流属性之一中。
  
访问用户配置对象的方式与邮箱中存储的其他项目类型不同。 可以使用[Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) EWS 托管 API 方法或[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS 操作查找所有项目，但必须使用"关联的搜索遍历"选项查找用户配置对象。 关联的 **搜索** 遍历指示搜索结果应仅包含用户配置对象。 EWS 包括一组特定于用户配置对象的操作。 
  
**表 1.用于处理用户配置对象的 EWS 操作和 EWS 托管 API 方法**

|**若要...**|**使用此 EWS 操作**|**使用此 EWS 托管 API 方法**|
|:-----|:-----|:-----|
|创建用户配置对象  <br/> |[CreateUserConfiguration 操作](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|获取用户配置对象  <br/> |[GetUserConfiguration 操作](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|更新用户配置对象  <br/> |[UpdateUserConfiguration 操作](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|删除用户配置对象  <br/> |[DeleteUserConfiguration 操作](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> 使用 EWS 创建的用户配置对象具有以"IPM"开头的 [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) 前缀。Configuration."。 用户 **配置对象的 ItemClass** 是用户配置对象前缀和用户配置对象名称。 可以使用 [Item.ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS 托管 API 属性或 **ItemClass** EWS 元素搜索已定义的用户配置对象。 
  
### <a name="extended-properties"></a>扩展属性
<a name="ExtendedProperties"> </a>

如果要 [在项目](properties-and-extended-properties-in-ews-in-exchange.md) 上存储配置信息，请使用扩展属性。 与 MAPI 不同，EWS 不会返回项目的属性包。 这意味着 EWS 客户端必须知道扩展属性标识符，才能查找和访问扩展属性。 如果需要存储用户配置对象外的其他项目的配置信息，使用扩展属性创建自定义属性可能是您的解决方案。 扩展属性使您能够访问和存储不是项目的标准属性集一部分的属性的信息。 
  
> [!IMPORTANT]
> 数据库Exchange具有有限数量的属性。 数据库的最大属性标识符数Exchange 32，767。 如果你使用扩展属性存储许多设置，我们建议你使用单个扩展属性来存储这些设置，以便不会超过此最大值。 
  
可以使用 [Item.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx) EWS 托管 API 方法或 [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS 操作设置用户配置对象的扩展属性。 
  
### <a name="custom-items"></a>自定义项
<a name="CustomItems"> </a>

自定义项还可用于存储信息。 现有项属性可以重新用于包含配置信息。 或者，可以使用扩展属性为应用程序定义自己的属性。 使用自定义项存储配置具有以下优点： 
  
- 它们适用于支持 EWS 的所有Exchange版本。
    
- 如果不对项目使用扩展属性，则不Exchange属性的预算。
    
## <a name="where-should-i-store-my-application-settings"></a>应在何处存储我的应用程序设置？
<a name="ApplicationSettingsLocation"> </a>

邮箱文件夹及其中的项目位于根邮件文件夹中。 此文件夹由 EWS 托管 API 中的 [WellKnownFolderName.msgfolderroot](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) 值标识。 在 MAPI 术语中，这是邮箱的 IPM 子树的等效项。 用户配置对象通常用于创建基于 UI 的设置，以便应用程序可以基于用户访问的文件夹呈现视图设置。 通常，在与该文件夹关联的用户配置对象上设置基于文件夹的视图设置。 但有时，你可能希望将设置全局设置为应用程序。 在这种情况下，您可以将设置存储在根邮件文件夹中。 
  
大多数用户都不知道，并且通常无法访问根邮箱文件夹。 此文件夹由 EWS 托管 API 中的 [WellKnownFolderName.root](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) 值标识。 在 MAPI 术语中，这是邮箱的非 IPM 子树的等效项。 最终用户不直接访问的信息存储在根邮箱文件夹中。 您可能需要将应用程序设置存储在此文件夹中，因为客户端应用程序通常不访问它。 
  
## <a name="version-differences"></a>版本差异
<a name="VersionDifferences"> </a>

用户配置对象Exchange Online 2010 Exchange Online Office 365，Exchange 2010 Exchange版本。
  
## <a name="see-also"></a>另请参阅


- [在应用程序中使用 EWS 管理永久性Exchange](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    
- [属性和交换中的 EWS 中的扩展的属性](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 处理文件夹](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 处理 Exchange 邮箱项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    

