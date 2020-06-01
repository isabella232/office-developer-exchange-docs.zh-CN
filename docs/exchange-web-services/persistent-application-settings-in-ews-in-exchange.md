---
title: 在交换 EWS 持久应用程序设置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: 了解你的 EWS 托管 API 或 EWS 应用程序可用于在 Exchange 中创建持久自定义应用程序设置的不同选项。
ms.openlocfilehash: b1faa057e5a0c1a96498efcc23738c83d25ae986
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457401"
---
# <a name="persistent-application-settings-in-ews-in-exchange"></a>在交换 EWS 持久应用程序设置

了解你的 EWS 托管 API 或 EWS 应用程序可用于在 Exchange 中创建持久自定义应用程序设置的不同选项。
  

  
为邮箱或邮箱中的文件夹和项目保持同步自定义客户端配置的最简单方法是，将应用程序设置存储在 Exchange 服务器上。 您可以通过使用以下各项之一来确保邮箱的这些设置保持不变： 
  
- 用户配置对象
    
- 扩展属性
    
- 自定义项
    
## <a name="what-are-my-options-for-creating-persistent-application-settings"></a>什么是用于创建持久应用程序设置的选项？
<a name="Options"> </a>

用户配置对象是存储 EWS 客户端应用程序的配置设置的最佳选择。 您还可以使用扩展属性或自定义项，或使用所有三种的组合。 根据您的设置范围选择您的选项，并确定是否需要对其他应用程序使用您的设置。
  
**表1。基于作用域创建持久应用程序设置的推荐选项**

|**设置范围**|**使用 .。。**|**访问者**|
|:-----|:-----|:-----|
|项目  <br/> |现有项的扩展属性。  <br/> |任何 EWS 应用程序。 只有知道该属性标识符的 EWS 客户端才能访问扩展属性。  <br/> |
|Folder  <br/> |目标文件夹上的用户配置对象。 这是保存文件夹的视图设置的一种很有用的方法。  <br/> |任何 EWS 应用程序。  <br/> |
|邮箱  <br/> |默认 msgrootfolder 文件夹上的用户配置对象。  <br/> |任何 EWS 应用程序。  <br/> |
   
### <a name="user-configuration-objects"></a>用户配置对象
<a name="UserConfig"> </a>

用户配置对象是与邮箱中的文件夹相关联的特殊项目。 用户配置对象（也称为文件夹关联项）通常是保留应用程序设置的最佳选择，尤其是在配置信息与文件夹或邮箱相关联时。 它们通常不会向最终用户呈现。 由于它们可以以本机方式存储数据流和数据字典，因此它们是存储配置信息的理想选择。 使用用户配置对象的最佳方式是将一组配置存储在 XML 文档中，然后将该信息保存在某个用户配置流属性中。
  
用户配置对象的访问方式不同于邮箱中存储的其他项目类型。 您可以使用[FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) EWS 托管 API 方法或[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS 操作查找所有项，但必须使用**关联**的搜索遍历选项来查找用户配置对象。 **关联**的搜索遍历指示搜索结果应仅包含用户配置对象。 EWS 包含一组特定于用户配置对象的操作。 
  
**表1。用于处理用户配置对象的 EWS 操作和 EWS 托管 API 方法**

|**若要...**|**使用此 EWS 操作**|**使用此 EWS 托管 API 方法**|
|:-----|:-----|:-----|
|创建用户配置对象  <br/> |[CreateUserConfiguration 操作](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|获取用户配置对象  <br/> |[GetUserConfiguration 操作](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|更新用户配置对象  <br/> |[UpdateUserConfiguration 操作](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|删除用户配置对象  <br/> |[DeleteUserConfiguration 操作](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> 使用 EWS 创建的用户配置对象具有以 "IPM." 开头的[ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx)前缀。配置 "。 用户配置对象的**ItemClass**是用户配置对象前缀和用户配置对象名称。 您可以使用[ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS 托管 API 属性或**ItemClass** EWS 元素来搜索您定义的用户配置对象。 
  
### <a name="extended-properties"></a>扩展属性
<a name="ExtendedProperties"> </a>

如果要将配置信息存储在项目上，请使用[扩展属性](properties-and-extended-properties-in-ews-in-exchange.md)。 与 MAPI 不同，EWS 不会返回项目的属性包。 这意味着 EWS 客户端必须知道扩展属性标识符才能查找和访问扩展属性。 如果需要将配置信息存储在除用户配置对象以外的其他项上，则使用扩展属性来创建自定义属性可能是解决方案。 利用扩展属性，可以访问和存储不属于项目的标准属性集的属性的信息。 
  
> [!IMPORTANT]
> Exchange 数据库架构具有有限数量的属性。 Exchange 数据库的属性标识符的最大数目为32767。 如果要使用扩展属性存储许多设置，建议使用一个扩展属性来存储这些设置，这样您就不会超过此最大值。 
  
您可以使用[项目。更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx)EWS 托管 API 方法或[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS 操作，以设置用户配置对象的扩展属性。 
  
### <a name="custom-items"></a>自定义项
<a name="CustomItems"> </a>

此外，还可以使用自定义项来存储信息。 现有项目属性可以改变用途以包含配置信息。 或者，您可以使用扩展属性为您自己的应用程序定义自己的属性。 使用自定义项目存储配置可提供以下好处： 
  
- 它们适用于支持 EWS 的所有 Exchange 版本。
    
- 如果不对项目使用扩展属性，则不会收取 Exchange 属性的预算。
    
## <a name="where-should-i-store-my-application-settings"></a>我应将应用程序设置存储在哪里？
<a name="ApplicationSettingsLocation"> </a>

邮箱文件夹及其内的项目位于根邮件文件夹中。 此文件夹由 EWS 托管 API 中的 msgfolderroot 值标识[WellKnownFolderName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) 。 在 MAPI 术语中，这是邮箱的 IPM 子树的等效项。 用户配置对象通常用于创建基于 UI 的设置，以便应用程序可以基于用户所访问的文件夹呈现视图设置。 通常在与文件夹相关联的 "用户配置" 对象上设置基于文件夹的视图设置。 但有时，您可能希望将您的设置设为全局应用程序。 在这种情况下，您可以将设置存储在根邮件文件夹中。 
  
大多数用户不知道，通常不会访问根邮箱文件夹。 此文件夹由 EWS 托管 API 中的[WellKnownFolderName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)值标识。 在 MAPI 术语中，这与邮箱的非 IPM 子树是等效的。 最终用户无法直接访问的信息存储在根邮箱文件夹中。 您可能需要将应用程序设置存储在此文件夹中，因为客户端应用程序通常不会访问它。 
  
## <a name="version-differences"></a>版本差异
<a name="VersionDifferences"> </a>

用户配置对象在 Exchange Online 上可用，Exchange Online 作为 Office 365 的一部分，以及从 Exchange 2010 开始的 Exchange 版本。
  
## <a name="see-also"></a>另请参阅


- [使用 Exchange 中的 EWS 管理持久应用程序设置](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    
- [Exchange 中 EWS 的属性和扩展属性](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 处理文件夹](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 处理 Exchange 邮箱项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    

