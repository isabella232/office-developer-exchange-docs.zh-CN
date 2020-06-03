---
title: Exchange 的自动发现 web 服务参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a01124a8-a8cf-4b80-8625-d7ee05690bca
description: 在 Exchange 中查找自动发现 web 服务的引用内容。
ms.openlocfilehash: ce7f2bbd662a5e61959c7e3c6748f0cf40cc4fb3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466869"
---
# <a name="autodiscover-web-service-reference-for-exchange"></a>Exchange 的自动发现 web 服务参考

在 Exchange 中查找自动发现 web 服务的引用内容。
  
自动发现 web 服务提供了您的应用程序用来创建与 Exchange 服务器的连接的配置信息。 您可以使用下列选项之一连接到自动发现：
  
- SOAP 自动发现服务—可用于连接到以 Exchange 2010 开头的 Exchange 版本的客户端，包括 Exchange Online。
    
- "纯旧 XML" （POX）自动发现服务—可用于连接到以 Exchange 2007 开头的 Exchange 版本的客户端（包括 Exchange Online）。 
    
SOAP 和 POX 自动发现服务都可以提供您的客户端将用于创建与 Exchange 服务器的连接的配置信息。
  
> [!NOTE]
> 对于从 Exchange 2010 开始的 Exchange 版本，我们建议使用 SOAP 自动发现服务，而不是 POX 自动发现服务。 SOAP 自动发现服务提供批量自动发现设置请求，并更精确地控制响应中返回的设置。 
  
本节包含有关 SOAP 自动发现服务和 POX 自动发现服务的参考信息。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [Exchange 的 SOAP 自动发现 web 服务参考](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [Exchange 的 POX 自动发现 web 服务参考](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange Web 服务参考](web-services-reference-for-exchange.md)
- [自动发现服务（SOAP）](https://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [自动发现服务（POX）](https://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

