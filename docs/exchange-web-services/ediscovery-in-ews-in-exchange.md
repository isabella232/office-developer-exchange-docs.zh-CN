---
title: 在交换中 EWS eDiscovery
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: 了解 Exchange 中的 EWS 中的电子数据Exchange。
ms.openlocfilehash: 0b4f211e7f8a6ec085fd03ada1cc5a35187106e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512308"
---
# <a name="ediscovery-in-ews-in-exchange"></a>在交换中 EWS eDiscovery

了解 Exchange 中的 EWS 中的电子数据Exchange。
  
电子数据展示是一种联合查询 Web 服务，它使外部应用程序能够执行Exchange查询。
  
发现包括几个阶段，包括识别和保留关键数据、剔除并审查数据，以及在诉讼中生成数据。 电子数据展示查询通过跨跨 Exchange 和 SharePoint 提供单个发现工作流来加快发现SharePoint。
  
## <a name="ediscovery-operations"></a>电子数据展示操作

EWS 公开的电子数据展示功能可通过 Exchange Online 中引入的操作、Exchange Online 作为 Office 365 的一部分以及 Exchange 从 Exchange 2013 开始的版本提供。 
  
**表 1.电子数据展示的新操作**

|**操作名称**|**说明**|
|:-----|:-----|
|[GetDiscoverySearchConfiguration](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |获取就地保留、保存的发现搜索和启用发现搜索的邮箱的配置信息。  <br/> |
|[GetHoldOnMailboxes](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |获取基于查询的保留的状态，该保留通过使用 [SetHoldOnMailboxes 操作进行设置](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)。  <br/> |
|[GetNonIndexableItemDetails](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |检索有关无法编制索引的项目的详细信息。 这包括（但不限于）项目标识符、错误代码、错误描述、尝试对项目编制索引时以及有关文件的其他信息。  <br/> |
|[GetNonIndexableItemStatistics](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |检索邮箱中无法编制索引的项目数。  <br/> |
|[GetSearchableMailboxes](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |获取客户端有权搜索或执行电子数据展示的邮箱列表。  <br/> |
|[SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |搜索特定邮箱中与查询关键字匹配的项目。  <br/> |
|[SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |对项目设置基于查询的保留。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

