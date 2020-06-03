---
title: Exchange 的统一消息 web 服务参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Unified
api_type:
- schema
ms.assetid: 83afea8a-c716-41df-9eb2-e1000357afb6
description: 在 Exchange 中查找统一消息（UM） web 服务的引用内容。
ms.openlocfilehash: e4bb63f34650dae8fc28016196c97a6b79e69df0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467373"
---
# <a name="unified-messaging-web-service-reference-for-exchange"></a>Exchange 的统一消息 web 服务参考

在 Exchange 中查找统一消息（UM） web 服务的引用内容。
  
统一消息（UM） web 服务提供了一个扩展性点，使客户端能够读取和更改有关 UM 属性的信息，并请求对邮箱存储项进行分析并通过电话设备决定。 本节包含有关组成 UM web 服务的 XML 消息的操作和元素的信息。 此内容适用于类似于 https:// \<yourclientaccessserver\> /EWS/UM2007Legacy 的服务终结点 URL。 
  
您可以使用自动发现服务获取指向 UM web 服务终结点的 URL。 有关自动发现的详细信息，请参阅[Exchange 的自动发现](../exchange-web-services/autodiscover-for-exchange.md)。
  
> [!NOTE]
>  对于从 Exchange 2010 开始的 Exchange 版本，我们建议使用[Exchange Web 服务（EWS）](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx)而不是 UM Web 服务中提供的统一消息操作，原因如下： 
> - 基于 EWS 的 UM 功能在 EWS 托管 API 中具有一流支持。 
> - 在从 Exchange 2010 开始的 Exchange 版本中，新的 UM 功能将添加到 EWS，但不添加到统一消息 web 服务中。 
  
UM web 服务没有显式架构。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [Exchange 的统一消息 web 服务操作](unified-messaging-web-service-operations-for-exchange.md)   
- [Exchange 的统一消息 web 服务 XML 元素](unified-messaging-web-service-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 的自动发现 web 服务参考](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

