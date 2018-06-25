---
title: 在 Exchange 中的 EWS 中的电子数据展示
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: 在 Exchange 中了解有关电子数据展示中的 ews。
ms.openlocfilehash: 6491fdd9f2246870a89bfa89bf7d97b972d67c92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752707"
---
# <a name="ediscovery-in-ews-in-exchange"></a>在 Exchange 中的 EWS 中的电子数据展示

在 Exchange 中了解有关电子数据展示中的 ews。
  
电子数据展示是允许外部应用程序以执行 Exchange 数据的查询联合的查询 web 服务。
  
发现包含几个阶段，包括标识和保留项数据、 下挑选和查看数据，以及生成庭院中的数据。 电子数据展示查询加快发现过程，通过提供跨 Exchange 和 SharePoint 的单个发现工作流。
  
## <a name="ediscovery-operations"></a>电子数据展示操作

由 EWS 公开该电子数据展示功能，通过在 Exchange Online 中，Exchange Online 作为 Office 365 的一部分和版本的 Exchange 开头 Exchange 2013 中引入的操作。 
  
**表 1。电子数据展示的新操作**

|**操作名称**|**说明**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |获取就地保留，保存查询搜索和启用了发现搜索邮箱的配置信息。  <br/> |
|[GetHoldOnMailboxes](http://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |获取使用[SetHoldOnMailboxes 操作](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)设置了基于查询的保留状态。  <br/> |
|[GetNonIndexableItemDetails](http://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |检索有关无法编制索引的项目的详细信息。 这包括但不限于的项标识符的错误代码、 错误说明，当尝试索引项，以及有关文件的其他信息。  <br/> |
|[GetNonIndexableItemStatistics](http://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |检索邮箱中无法编制索引的项的计数。  <br/> |
|[GetSearchableMailboxes](http://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |获取邮箱的列表的客户端有搜索或上执行电子数据展示的权限。  <br/> |
|[SearchMailboxes](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |搜索查询关键字匹配的特定邮箱中的项目。  <br/> |
|[SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |设置基于查询的保留项。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

