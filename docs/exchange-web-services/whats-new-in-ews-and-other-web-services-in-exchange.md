---
title: Exchange 中的 EWS 和其他 web 服务中的新增功能
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: aff6328f-cff1-42a6-9a4d-ea4d2d0461cf
description: 了解在 Exchange 和 EWS 托管 API 中的 EWS 和 web 服务中的新增功能。
localization_priority: Priority
ms.openlocfilehash: 5e74ad9d4cf5083983c28e477fd50d48e2d7fbb6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529838"
---
# <a name="whats-new-in-ews-and-other-web-services-in-exchange"></a>Exchange 中的 EWS 和其他 web 服务中的新增功能

了解在 Exchange 和 EWS 托管 API 中的 EWS 和 web 服务中的新增功能。
  
Exchange 中的 Web 服务已更新，以包含新功能。 
  
**表1。Exchange Online 中的新 web 服务功能、Exchange 2013 和 EWS 托管 API**

|功能|在 Exchange Online 中实施|在 Exchange 2013 中实施|在 EWS 托管 API 中实现|
|:-----|:-----:|:-----:|:-----:|
|[电子数据展示](#eDisc) <br/> |是  <br/> |是  <br/> |是  <br/> |
|[存档](#arch) <br/> |是  <br/> |是  <br/> |是  <br/> |
|[人数](#personas) <br/> |是  <br/> |是  <br/> |否  <br/> |
|[统一联系人存储](#unified) <br/> |是  <br/> |是  <br/> |否  <br/> |
|[保留策略](#retentionpolicy) <br/> |是  <br/> |是  <br/> |是  <br/> |
|[用户照片](#userphoto) <br/> |是  <br/> |是  <br/> |否  <br/> |
|[Outlook 相关邮件应用程序管理](#ewsmailapps) <br/> |是  <br/> |是  <br/> |是  <br/> |
|[建议新会议时间](#propose) <br/> |是  <br/> |否  <br/> |否  <br/> |

<a name="eDisc"> </a>

## <a name="ediscovery-in-ews"></a>EWS 中的电子数据展示

电子数据展示是一种联合查询 web 服务，它使外部应用程序（如 SharePoint 2013）能够执行 Exchange 数据的查询。 发现包括几个阶段，包括标识和保留关键数据、在法庭中剔除和查看数据以及生成数据。 电子数据展示查询通过跨 Exchange 和 SharePoint 提供单个发现工作流来促进发现过程。
  
**表2。用于处理电子数据展示的 EWS 操作和 EWS 托管 API 方法**

|**操作名称**|**EWS 托管的 API 方法**|**说明**|
|:-----|:-----|:-----|
|[GetDiscoverySearchConfiguration 操作](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |[ExchangeService GetDiscoverySearchConfiguration （）](https://msdn.microsoft.com/library/jj670206%28v=exchg.80%29.aspx) <br/> |获取就地保留的配置信息、已保存的发现搜索以及为发现搜索启用的邮箱。  <br/> |
|[GetHoldOnMailboxes 操作](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |[ExchangeService GetHoldOnMailboxes （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getholdonmailboxes%28v=exchg.80%29.aspx) <br/> |获取基于查询的保留的状态，它是通过使用**SetHoldOnMailboxes**操作设置的。  <br/> |
|[GetNonIndexableItemDetails 操作](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |[ExchangeService GetNonIndexableItemDetails （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemdetails%28v=exchg.80%29.aspx) <br/> |获取有关无法编制索引的项目的详细信息。 这包括但不限于项目标识符、错误代码、错误说明、对项目编制索引时，以及有关项目的其他信息。  <br/> |
|[GetNonIndexableItemStatistics 操作](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |[ExchangeService GetNonIndexableItemStatistics （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemstatistics%28v=exchg.80%29.aspx) <br/> |获取邮箱中无法编制索引的项的计数。  <br/> |
|[GetSearchableMailboxes 操作](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |[ExchangeService GetSearchableMailboxes （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getsearchablemailboxes%28v=exchg.80%29.aspx) <br/> |获取客户端有权搜索或执行电子数据展示的邮箱的列表。  <br/> |
|[SearchMailboxes 操作](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService SearchMailboxes （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> |搜索与查询关键字匹配的特定邮箱中的项目。  <br/> |
|[SetHoldOnMailboxes 操作](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |[ExchangeService SetHoldOnMailboxes （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) <br/> |设置项目的基于查询的保留。  <br/> |

<a name="arch"> </a>

## <a name="archiving-in-ews"></a>在 EWS 中存档

存档邮箱是与用户相关联的辅助邮箱。 存档邮箱通常用于管理电子邮件存储限制。 例如，较旧的电子邮件项目可能会定期从收件箱移动到存档邮箱。 
  
Exchange 引入了两种新的 EWS 操作，可用于存档主邮箱中的一组邮件项目。 以这种方式存档收件箱项目可保留项目的文件夹层次结构。 此外，存档邮箱现在可以本地存储在客户端上，也可以远程存储为用户对用户不透明的方式，方法是使用文件夹路径指向存档的内容。
  
**表3。用于处理存档的 EWS 操作和 EWS 托管 API 方法**

|**操作名称**|**EWS 托管的 API 方法**|**说明**|
|:-----|:-----|:-----|
|[ArchiveItem 操作](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |[ExchangeService ArchiveItems （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.archiveitems%28v=exchg.80%29.aspx) <br/> |将项目从主邮箱移动到存档邮箱。  <br/> |
|[CreateFolderPath 操作](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |未实现。  <br/> |在主邮箱或存档邮箱中创建文件夹层次结构。  <br/> |

<a name="personas"> </a>

## <a name="personas-in-ews"></a>EWS 中的角色

*角色*是与个人相关联的数据的集合。 数据可以来自一个或多个源，并通过通用链接 ID 与角色相关联。 通过 EWS 中的角色，可以从多个源中链接、搜索、浏览和检索有关人员的信息，并将该信息组织到一个逻辑实体中。 角色与联系人的不同之处在于，联系人是与个人相关联的单个源中的数据集合;例如，个人 Outlook 联系人或全局地址列表（GAL）中的条目。 
  
EWS 托管 API 无法实现此功能。
  
> [!NOTE]
> 统一联系人存储区还通过支持该功能的操作公开了角色功能。 
  
**表4。用于处理角色的 EWS 操作**

|**操作名称**|**说明**|
|:-----|:-----|
|[FindPeople 操作](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |返回指定的联系人文件夹中的所有 persona 对象，或检索与指定的查询字符串匹配的所有联系人。  <br/> |
|[GetPersona 操作](https://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |检索角色。  <br/> |

<a name="unified"> </a>

## <a name="unified-contact-store-in-ews"></a>EWS 中的统一联系人存储

统一联系人存储是一项功能，可跨 Office 产品提供一致的联系人体验，并充当第三方应用程序使用相同的联系人存储的集成点。 它允许用户和应用程序存储、管理和访问联系人信息，并使其在 Lync、Exchange 2013、Outlook、Outlook Web App 和任何其他实现对统一联系人存储的访问权限的应用程序之间全局可用。 Exchange 是统一联系人存储区体验的联系人存储区。 
  
EWS 托管 API 无法实现此功能。
  
**表5。使用统一联系人存储区的 EWS 操作**

|**操作名称**|**说明**|
|:-----|:-----|
|[AddNewImContactToGroup 操作](https://msdn.microsoft.com/library/0cb5525f-faa3-48f1-9551-df55ffc26f46%28Office.15%29.aspx) <br/> |将新的 IM 联系人添加到组中。 统一联系人存储最多可以包含1000个联系人。  <br/> |
|[AddImContactToGroup 操作](https://msdn.microsoft.com/library/376acc42-2684-4596-aca1-82a4a10865c9%28Office.15%29.aspx) <br/> |将现有 IM 联系人添加到组中。 统一联系人存储最多可以包含1000个联系人。  <br/> |
|[AddImGroup 操作](https://msdn.microsoft.com/library/6df6e504-b7c8-4773-b10f-ffa5defac229%28Office.15%29.aspx) <br/> |添加新的 IM 组。 统一联系人存储最多可包含64个组。  <br/> |
|[AddNewTelUriContactToGroup 操作](https://msdn.microsoft.com/library/c9688ce8-2465-45bb-8bd2-94b32ed4885c%28Office.15%29.aspx) <br/> |根据联系人的电话号码将新联系人添加到组中。  <br/> |
|[AddDistributionGroupToImList 操作](https://msdn.microsoft.com/library/5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a%28Office.15%29.aspx) <br/> |添加新的通讯组列表组。 统一联系人存储最多可包含64个组。  <br/> |
|[GetImItemList 操作](https://msdn.microsoft.com/library/e31d14e1-0c1f-4b69-98b7-157d59c13698%28Office.15%29.aspx) <br/> |检索 IM 组和 IM 联系人角色的列表。  <br/> |
|[GetImItems 操作](https://msdn.microsoft.com/library/51186691-46d2-4d5c-b8bc-4ee2bb20fbe7%28Office.15%29.aspx) <br/> |检索有关指定的 IM 组和 IM 联系人角色的信息。  <br/> |
|[RemoveContactFromImList 操作](https://msdn.microsoft.com/library/28ec96c3-45af-48ff-9f17-718a527dc0ad%28Office.15%29.aspx) <br/> |从所有 IM 组中删除指定的联系人。  <br/> |
|[RemoveImContactFromGroup 操作](https://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) <br/> |从组中删除 IM 联系人。  <br/> |
|[RemoveDistributionGroupFromImList 操作](https://msdn.microsoft.com/library/252bddf2-98b6-4824-b548-2fba2bda5384%28Office.15%29.aspx) <br/> |删除指定的 IM 通讯组列表组。  <br/> |
|[RemoveImGroup 操作](https://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) <br/> |删除指定的 IM 组。  <br/> |
|[SetImGroup 操作](https://msdn.microsoft.com/library/2d48aa07-8152-4c3d-a519-061253e80174%28Office.15%29.aspx) <br/> |更改组的显示名称。  <br/> |

<a name="retentionpolicy"> </a>
  
## <a name="retention-policies-in-ews"></a>EWS 中的保留策略

保留策略是 Exchange 中用于对一个或多个保留标记进行分组的策略，用于将保留设置应用于文件夹或单个项目（如电子邮件和语音邮件），并将保留设置应用于邮箱。
  
Exchange 包括三种类型的保留标记：
  
- 应用于未应用其他类型的保留标记的邮箱项目的默认策略标记。
    
- 应用于默认文件夹（如收件箱）的系统文件夹策略标记。
    
- 用户可应用于他们创建的文件夹或单个项目的个人标记。
    
只有一个保留策略可分配给一个邮箱，但策略可以有一个或多个链接到它的不同类型的保留标记。 可以随时将保留标记链接到保留策略或从保留策略中取消链接。 Exchange 中的 EWS 公开新操作、 [GetUserRetentionPolicyTags](https://msdn.microsoft.com/library/57c6ff23-5c2c-42ee-824b-5a1b6dafab8c%28Office.15%29.aspx)和 EWS 托管 API 实现一个新的方法[ExchangeService （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuserretentionpolicytags%28v=exchg.80%29.aspx)，该方法提供链接到保留策略的所有标记的列表。 您可以使用**CreateItem**、 **CreateFolder**、 **UpdateItem**、 **UpdateFolder**、 **GetItem**和**GetFolder**操作来设置和检索项目和文件夹的保留策略标记。 

<a name="userphoto"> </a>

## <a name="requesting-user-photos"></a>请求用户照片

您可以使用[GetUserPhoto 操作](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)的两个实现中的一种实现，从 Exchange 服务器请求用户照片： [REST](how-to-get-user-photos-by-using-ews-in-exchange.md)或 SOAP。 REST 终结点使用标准 HTTPS **get**请求获取用户照片。 服务将返回存储在 Exchange 中的用户照片或 Active Directory 域服务（AD DS）中的照片。 
  
EWS 托管 API 无法实现此功能。 但是，可以通过获取附加到联系人的照片，使用 EWS 托管 API 返回存储在邮箱中的用户照片。

<a name="blocksender"> </a>

## <a name="block-senders-and-mark-email-as-junk-in-ews"></a>阻止发件人并在 EWS 中将电子邮件标记为垃圾邮件

您现在可以使用 EWS 中的新[MarkAsJunk 操作](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)或 EWS 托管 API 中的[ExchangeService （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx)方法，阻止发件人并将电子邮件标记为垃圾邮件。 

<a name="ewsmailapps"> </a>

## <a name="mail-apps-for-outlook"></a>Outlook 邮件应用程序

EWS 现在支持对 Outlook 的邮件应用程序进行管理。 
  
**表6。使用适用于 Outlook 的邮件应用程序的 EWS 操作和 EWS 托管 API 方法**

|**操作名称**|**EWS 托管的 API 方法**|**说明**|
|:-----|:-----|:-----|
|[DisableApp 操作](https://msdn.microsoft.com/library/211731a3-2470-49af-bda3-1ddfc15a8e46%28Office.15%29.aspx) <br/> |[ExchangeService DisableApp （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.disableapp%28v=exchg.80%29.aspx) <br/> |禁用已安装的应用程序。  <br/> |
|[Getappmanifests 已操作](https://msdn.microsoft.com/library/21a4987c-c24d-4a6e-ace4-e81edcda6303%28Office.15%29.aspx) <br/> |[ExchangeService Getappmanifests 已（）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getappmanifests%28v=exchg.80%29.aspx) <br/> |获取邮箱的应用程序清单。  <br/> |
|[GetAppMarketplaceUrl 操作](https://msdn.microsoft.com/library/2c016fc3-0e13-4624-9a5b-d3e84577a860%28Office.15%29.aspx) <br/> |[ExchangeService GetAppMarketplaceUrl （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getappmarketplaceurl%28v=exchg.80%29.aspx) <br/> |获取应用程序市场 URL。  <br/> |
|[GetClientAccessToken 操作](https://msdn.microsoft.com/library/086876cc-e22c-4e89-89f9-19e78af51217%28Office.15%29.aspx) <br/> |[ExchangeService GetClientAccessToken （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getclientaccesstoken%28v=exchg.80%29.aspx) <br/> |获取客户端访问令牌。  <br/> |
|[InstallApp 操作](https://msdn.microsoft.com/library/596eae95-3e78-489a-8bb2-d2dd4a026405%28Office.15%29.aspx) <br/> |[ExchangeService InstallApp （）](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.installapp%28v=exchg.80%29.aspx) <br/> |为邮箱安装应用程序。  <br/> |
|[UninstallApp 操作](https://msdn.microsoft.com/library/7707aa6a-381d-43f7-a454-54f6343ed127%28Office.15%29.aspx) <br/> |[ExchangeService。 UninstallApp](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.uninstallapp%28v=exchg.80%29.aspx) <br/> |从邮箱中卸载应用程序。  <br/> |

<a name="propose"> </a>

## <a name="propose-new-meeting-time"></a>建议新会议时间

建议的新时间功能是在 Exchange 的15.00.0800.007 版本中引入的。 这样，会议与会者就可以向会议组织者[建议新的会议时间](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)。 
  
EWS 托管 API 无法实现此功能。
  
## <a name="see-also"></a>另请参阅

- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
- [Outlook 和 Exchange 中的 EWS 的邮件应用程序](mail-apps-for-outlook-and-ews-in-exchange.md)
- [在 Exchange 中 EWS 存档](archiving-in-ews-in-exchange.md)
- [在交换中 EWS eDiscovery](ediscovery-in-ews-in-exchange.md)
- [人员和 Exchange 中的 EWS 中的联系人](people-and-contacts-in-ews-in-exchange.md)
    

