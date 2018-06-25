---
title: What's new in EWS 和其他 web 服务在 Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: aff6328f-cff1-42a6-9a4d-ea4d2d0461cf
description: 找出 what's new in EWS 和 web 服务在 Exchange 和 EWS 托管 API。
ms.openlocfilehash: 9e848babc96707152be767f42b561a587fc6cff0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753023"
---
# <a name="whats-new-in-ews-and-other-web-services-in-exchange"></a>What's new in EWS 和其他 web 服务在 Exchange

找出 what's new in EWS 和 web 服务在 Exchange 和 EWS 托管 API。
  
Exchange 中的 web 服务进行了更新以包含新功能。 
  
**表 1。新的 web 服务功能在 Exchange Online 和 Exchange 2013 EWS 托管 API**

|功能|实现在 Exchange Online|在 Exchange 2013 中实现|EWS 托管 API 中实现|
|:-----|:-----:|:-----:|:-----:|
|[电子数据展示](#eDisc) <br/> |是  <br/> |是  <br/> |是  <br/> |
|[存档](#arch) <br/> |是  <br/> |是  <br/> |是  <br/> |
|[角色](#personas) <br/> |是  <br/> |是  <br/> |否  <br/> |
|[统一的联系人存储库](#unified) <br/> |是  <br/> |是  <br/> |否  <br/> |
|[保留策略](#retentionpolicy) <br/> |是  <br/> |是  <br/> |是  <br/> |
|[用户照片](#userphoto) <br/> |是  <br/> |是  <br/> |否  <br/> |
|[用于 Outlook 管理的邮件应用程序](#ewsmailapps) <br/> |是  <br/> |是  <br/> |是  <br/> |
|[建议新会议时间](#propose) <br/> |是  <br/> |否  <br/> |否  <br/> |

<a name="eDisc"> </a>

## <a name="ediscovery-in-ews"></a>EWS 中的电子数据展示

电子数据展示是允许外部应用程序，如 SharePoint 2013 中，若要执行的 Exchange 数据的查询联合的查询 web 服务。 发现包含几个阶段，包括标识和保留项数据、 下挑选和查看数据，以及生成庭院中的数据。 电子数据展示查询加快发现过程，通过提供跨 Exchange 和 SharePoint 的单个发现工作流。
  
**表 2。EWS 操作和用于处理电子数据展示的 EWS 托管 API 方法**

|**操作名称**|**EWS 托管的 API 方法**|**说明**|
|:-----|:-----|:-----|
|[GetDiscoverySearchConfiguration 操作](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |[ExchangeService.GetDiscoverySearchConfiguration()](http://msdn.microsoft.com/en-us/library/jj670206%28v=exchg.80%29.aspx) <br/> |获取就地保留，保存查询搜索和启用了发现搜索邮箱的配置信息。  <br/> |
|[GetHoldOnMailboxes 操作](http://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |[ExchangeService.GetHoldOnMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getholdonmailboxes%28v=exchg.80%29.aspx) <br/> |获取使用**SetHoldOnMailboxes**操作设置了基于查询的保留状态。  <br/> |
|[GetNonIndexableItemDetails 操作](http://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |[ExchangeService.GetNonIndexableItemDetails()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemdetails%28v=exchg.80%29.aspx) <br/> |获取无法编制索引的项目的详细信息。 这包括但不限于的项标识符的错误代码、 错误说明，当尝试索引项，以及有关项目的其他信息。  <br/> |
|[GetNonIndexableItemStatistics 操作](http://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |[ExchangeService.GetNonIndexableItemStatistics()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemstatistics%28v=exchg.80%29.aspx) <br/> |获取邮箱中无法编制索引的项目。  <br/> |
|[GetSearchableMailboxes 操作](http://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |[ExchangeService.GetSearchableMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getsearchablemailboxes%28v=exchg.80%29.aspx) <br/> |获取邮箱的列表的客户端有搜索或上执行电子数据展示的权限。  <br/> |
|[SearchMailboxes 操作](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService.SearchMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> |搜索查询关键字匹配的特定邮箱中的项目。  <br/> |
|[SetHoldOnMailboxes 操作](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |[ExchangeService.SetHoldOnMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) <br/> |设置基于查询的保留项。  <br/> |

<a name="arch"> </a>

## <a name="archiving-in-ews"></a>EWS 中的存档

存档邮箱的第二与用户关联的邮箱。 存档邮箱通常用于管理电子邮件存储限制。 例如，旧的电子邮件项可能会定期从移收件箱到存档邮箱。 
  
Exchange 介绍可用于存档的一组从主邮箱的邮件项目的两个新的 EWS 操作。 这种方式的收件箱项目存档保留的项目的文件夹层次结构。 此外，现在可以在客户端，本地或是大多数情况下不透明给用户，通过使用文件夹路径指向存档的内容的方式在远程存储存档邮箱。
  
**表 3。EWS 操作和用于处理存档的 EWS 托管 API 方法**

|**操作名称**|**EWS 托管的 API 方法**|**说明**|
|:-----|:-----|:-----|
|[ArchiveItem 操作](http://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |[ExchangeService.ArchiveItems()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.archiveitems%28v=exchg.80%29.aspx) <br/> |将项目从主邮箱移动到存档邮箱。  <br/> |
|[CreateFolderPath 操作](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |未实现。  <br/> |创建在主文件夹层次结构或存档邮箱。  <br/> |

<a name="personas"> </a>

## <a name="personas-in-ews"></a>EWS 中的角色

*个人*与个人相关联的数据的集合。 数据可以来自一个或多个源和相关联角色通过一个常见链接 id。 EWS 中的角色使您能够链接、 搜索、 浏览和来自多个源检索有关个人信息和组织到单个逻辑实体的信息。 角色不同于联系人，联系人是从单个源与个人; 关联的数据的集合例如，Outlook 个人联系人或全局地址列表 (GAL) 中的条目。 
  
EWS 托管 API 无法实现此功能。
  
> [!NOTE]
> 统一联系人存储库还公开个人功能通过支持该功能的操作。 
  
**表 4。使用角色的 EWS 操作**

|**操作名称**|**说明**|
|:-----|:-----|
|[FindPeople 操作](http://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |从指定的联系人文件夹中返回所有角色对象或检索与指定的查询字符串匹配的所有联系人。  <br/> |
|[GetPersona 操作](http://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |检索角色。  <br/> |

<a name="unified"> </a>

## <a name="unified-contact-store-in-ews"></a>EWS 中的统一的联系人存储库

统一联系人存储库是一种功能，Office 产品跨提供一致的联系人体验以及作为第三方应用程序可以使用相同的联系人存储库集成点。 它允许用户和应用程序存储、 管理和访问联系人信息并使其可全局之间 Lync、 Exchange 2013、 Outlook、 Outlook Web App 和实现对统一联系人存储库的访问的任何其他应用程序。 Exchange 的统一联系人存储库体验的联系人存储库。 
  
EWS 托管 API 无法实现此功能。
  
**表 5。使用统一联系人存储库的 EWS 操作**

|**操作名称**|**说明**|
|:-----|:-----|
|[AddNewImContactToGroup 操作](http://msdn.microsoft.com/library/0cb5525f-faa3-48f1-9551-df55ffc26f46%28Office.15%29.aspx) <br/> |将新的 IM 联系人添加到组。 1000 联系人的最多可以包含统一联系人存储库。  <br/> |
|[AddImContactToGroup 操作](http://msdn.microsoft.com/library/376acc42-2684-4596-aca1-82a4a10865c9%28Office.15%29.aspx) <br/> |将现有的即时消息联系人添加到组。 1000 联系人的最多可以包含统一联系人存储库。  <br/> |
|[AddImGroup 操作](http://msdn.microsoft.com/library/6df6e504-b7c8-4773-b10f-ffa5defac229%28Office.15%29.aspx) <br/> |添加一个新的 IM 组。 64 组最多可以包含统一联系人存储库。  <br/> |
|[AddNewTelUriContactToGroup 操作](http://msdn.microsoft.com/library/c9688ce8-2465-45bb-8bd2-94b32ed4885c%28Office.15%29.aspx) <br/> |将新的联系人添加到联系人的电话号码所基于的组。  <br/> |
|[AddDistributionGroupToImList 操作](http://msdn.microsoft.com/library/5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a%28Office.15%29.aspx) <br/> |添加新的通讯组列表组。 64 组最多可以包含统一联系人存储库。  <br/> |
|[GetImItemList 操作](http://msdn.microsoft.com/library/e31d14e1-0c1f-4b69-98b7-157d59c13698%28Office.15%29.aspx) <br/> |检索 IM 组和 IM 联系人角色的列表。  <br/> |
|[GetImItems 操作](http://msdn.microsoft.com/library/51186691-46d2-4d5c-b8bc-4ee2bb20fbe7%28Office.15%29.aspx) <br/> |检索有关指定的 IM 组和 IM 联系人角色的信息。  <br/> |
|[RemoveContactFromImList 操作](http://msdn.microsoft.com/library/28ec96c3-45af-48ff-9f17-718a527dc0ad%28Office.15%29.aspx) <br/> |从所有 IM 组中删除指定的联系人。  <br/> |
|[RemoveImContactFromGroup 操作](http://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) <br/> |从组中删除 IM 联系人。  <br/> |
|[RemoveDistributionGroupFromImList 操作](http://msdn.microsoft.com/library/252bddf2-98b6-4824-b548-2fba2bda5384%28Office.15%29.aspx) <br/> |删除指定的 IM 通讯组列表组。  <br/> |
|[RemoveImGroup 操作](http://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) <br/> |删除指定的 IM 组。  <br/> |
|[SetImGroup 操作](http://msdn.microsoft.com/library/2d48aa07-8152-4c3d-a519-061253e80174%28Office.15%29.aspx) <br/> |更改组的显示名称。  <br/> |

<a name="retentionpolicy"> </a>
  
## <a name="retention-policies-in-ews"></a>EWS 中的保留策略

保留策略向一个图表组在 Exchange 中使用的策略或多个保留标记，将保留设置应用到文件夹或单个项目例如电子邮件和语音邮件，并应用于邮箱的保留设置。
  
Exchange 包括三种类型的保留标记：
  
- 默认策略标记应用于不已应用保留标记的任何其他类型的邮箱项目。
    
- 系统文件夹策略标记应用于默认文件夹，如收件箱。
    
- 用户可以应用于他们创建的文件夹或单个项目的个人标记。
    
只有一个保留策略可以分配给邮箱，但的策略可以有一个或多个链接到它的各种类型的保留标记。 保留标记可链接到或保留策略随时取消链接。 Exchange 中的 EWS 公开新操作， [GetUserRetentionPolicyTags](http://msdn.microsoft.com/library/57c6ff23-5c2c-42ee-824b-5a1b6dafab8c%28Office.15%29.aspx)，并 EWS 托管 API 实现新的方法， [ExchangeService.GetUserRetentionPolicyTags()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuserretentionpolicytags%28v=exchg.80%29.aspx)，提供链接到保留策略的所有标记的列表。 您可以设置并使用**CreateItem**、 **CreateFolder**、 **UpdateItem**、 **UpdateFolder**、 **GetItem**和**GetFolder**操作中检索的项目和文件夹的保留策略标记。 

<a name="userphoto"> </a>

## <a name="requesting-user-photos"></a>请求的用户照片

您可以从 Exchange 服务器请求用户照片，通过使用[GetUserPhoto 操作](http://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)的两个实现之一： [REST](how-to-get-user-photos-by-using-ews-in-exchange.md)或 SOAP。 REST 终结点使用标准的 HTTPS **GET**请求来获取用户照片。 该服务将也返回用户照片在 Exchange 存储或照片从 Active Directory 域服务 (AD DS)。 
  
EWS 托管 API 无法实现此功能。 但是，您可以使用 EWS 托管 API 返回用户照片的邮箱中存储的获取附加到联系人的照片。

<a name="blocksender"> </a>

## <a name="block-senders-and-mark-email-as-junk-in-ews"></a>阻止发件人，并将电子邮件标记为垃圾邮件中的 ews

您现在可以阻止发件人，并将电子邮件标记为垃圾邮件，使用 EWS 中的新[MarkAsJunk 操作](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)或 EWS 托管 API 中的[ExchangeService.MarkAsJunk()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx)方法。 

<a name="ewsmailapps"> </a>

## <a name="mail-apps-for-outlook"></a>Outlook 邮件应用程序

EWS 现在包括用于管理 Outlook 邮件应用程序的支持。 
  
**表 6。EWS 操作和用于处理 EWS 托管 API 方法的 Outlook 邮件应用程序**

|**操作名称**|**EWS 托管的 API 方法**|**说明**|
|:-----|:-----|:-----|
|[DisableApp 操作](http://msdn.microsoft.com/library/211731a3-2470-49af-bda3-1ddfc15a8e46%28Office.15%29.aspx) <br/> |[ExchangeService.DisableApp()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.disableapp%28v=exchg.80%29.aspx) <br/> |禁用已安装的应用程序。  <br/> |
|[GetAppManifests 操作](http://msdn.microsoft.com/library/21a4987c-c24d-4a6e-ace4-e81edcda6303%28Office.15%29.aspx) <br/> |[ExchangeService.GetAppManifests()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getappmanifests%28v=exchg.80%29.aspx) <br/> |获取对邮箱的应用程序清单。  <br/> |
|[GetAppMarketplaceUrl 操作](http://msdn.microsoft.com/library/2c016fc3-0e13-4624-9a5b-d3e84577a860%28Office.15%29.aspx) <br/> |[ExchangeService.GetAppMarketplaceUrl()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getappmarketplaceurl%28v=exchg.80%29.aspx) <br/> |获取应用程序的市场 URL。  <br/> |
|[GetClientAccessToken 操作](http://msdn.microsoft.com/library/086876cc-e22c-4e89-89f9-19e78af51217%28Office.15%29.aspx) <br/> |[ExchangeService.GetClientAccessToken()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getclientaccesstoken%28v=exchg.80%29.aspx) <br/> |获取客户端访问令牌。  <br/> |
|[InstallApp 操作](http://msdn.microsoft.com/library/596eae95-3e78-489a-8bb2-d2dd4a026405%28Office.15%29.aspx) <br/> |[ExchangeService.InstallApp()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.installapp%28v=exchg.80%29.aspx) <br/> |安装邮箱的应用程序。  <br/> |
|[UninstallApp 操作](http://msdn.microsoft.com/library/7707aa6a-381d-43f7-a454-54f6343ed127%28Office.15%29.aspx) <br/> |[ExchangeService.UninstallApp](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.uninstallapp%28v=exchg.80%29.aspx) <br/> |从邮箱中卸载应用程序。  <br/> |

<a name="propose"> </a>

## <a name="propose-new-meeting-time"></a>建议新会议时间

建议新时间功能是 Exchange 15.00.0800.007 版本中引入的。 这将允许会议组织者的[建议新的会议时间](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)会议与会者。 
  
EWS 托管 API 无法实现此功能。
  
## <a name="see-also"></a>另请参阅

- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
- [Outlook 和 Exchange 中的 EWS 的邮件应用程序](mail-apps-for-outlook-and-ews-in-exchange.md)
- [在 Exchange 中 EWS 存档](archiving-in-ews-in-exchange.md)
- [在交换中 EWS eDiscovery](ediscovery-in-ews-in-exchange.md)
- [人员和 Exchange 中的 EWS 中的联系人](people-and-contacts-in-ews-in-exchange.md)
    

