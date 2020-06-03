---
title: 为 Exchange 使用自动发现时提高性能
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e65ff6b2-3810-43ad-9728-27308891b193
description: 了解如何提高性能的应用程序中的自动发现过程。
ms.openlocfilehash: 844b56084b4f0b5e49b4ee095688d58ce469baca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456330"
---
# <a name="improving-performance-when-using-autodiscover-for-exchange"></a>为 Exchange 使用自动发现时提高性能

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解如何提高性能的应用程序中的自动发现过程。
  
有大量的 like 自动发现的原因。配置应用程序连接到 Exchange 无用户干预太棒了 ！如果您正在阅读本文，您可能已经知道使用和喜欢自动发现，因此我们不会在此处列出的所有原因。相反，我们将讨论潜在缺点： 性能。
  
自动发现本身不慢的过程，但它也不是本质上是 fast。[自动发现过程](autodiscover-for-exchange.md)涉及大量的网络活动，并的引入了大量的潜在的延迟。自动发现过程具有三个阶段 ；所有三个有可能影响性能： 
  
- 定义自动发现终结点候选池  对于在加入域的计算机上运行的应用程序，这可能会涉及[SCP 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)，这会涉及与 Active Directory 域服务 (AD DS) 进行通信。
    
- 尝试每个候选  这需要对每个应聘者终结点的 HTTP 请求/响应。
    
- 尝试其他选择  时在自动发现终结点候选池中的候选不产生的结果，您可以执行未经身份验证的 GET 请求 （HTTP 请求/响应） 和 DNS 查找。
    
面上这可能看起来不太多。但是，假设其中自动发现终结点候选池是多个或两个 Url，找不到 working 一个之前在池中的最后一个 URL。延迟会变得更显著。因此，可以做什么？
  
## <a name="consider-the-need-for-scp-lookup"></a>考虑需要为 SCP 查找

存在并已配置好 SCP 对象时，他们可以加快自动发现过程。在其他情况下，但是，他们会降低它。如果在您的环境中不使用 SCP，跳过节省时间的自动发现过程的整个 SCP 查找部分。
  
EWS 托管 API 使该轻松： 只需将[ExchangeService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.enablescplookup%28v=exchg.80%29.aspx)属性设为 **false**调用[ExchangeService.AutodiscoverUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx)方法之前。如果您正在使用[AutodiscoverService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx)类， [AutodiscoverService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.enablescplookup%28v=exchg.80%29.aspx)属性设置为 **false**在调用其任何方法之前。 
  
## <a name="use-autodiscover-less-often"></a>经常使用自动发现较少

自动发现未设计为用于经常使用应用程序。自动发现后面目的是应用程序可以使用它来发现配置信息，然后缓存一段时间内的信息。如果未缓存的配置信息，请考虑添加缓存到您的应用程序，以减少使用自动发现的次数。
  
即使您已在缓存，评估缓存配置信息的时间。该标准是[刷新自动发现信息每 24 小时](how-to-refresh-configuration-information-by-using-autodiscover.md)，但您可能能够扩展该时间。您应测试与目标环境，并使用"-生存时间"提出您适合您的配置。
  
## <a name="minimize-requested-data"></a>最小化请求的数据

If you're using the **AutodiscoverService** class in the EWS Managed API, or the [GetUserSettings 操作 (SOAP)](https://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx) operation via SOAP, you have direct control over what settings are returned in the response. Although you can request quite a few settings, chances are that your application only needs a handful of them. Every setting that you request requires more processing on the server, which means more time waiting for a response. Evaluate the settings you are requesting, and eliminate any that you don't need. 
  
如果使用的 EWS 托管 API 中的 **ExchangeService.AutodiscoverUrl** 方法，则无法更改您请求的设置。已经非常高效 ； 但是，此方法它只从 **UserSettingName 枚举**请求的 **ExternalEwsUrl** 和 [InternalEwsUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx) 设置。
  
如果您使用的 POX 自动发现服务，[您不能请求特定的属性](autodiscover-for-exchange.md#bk_Options)。
  
## <a name="see-also"></a>另请参阅


- [Exchange 自动发现](autodiscover-for-exchange.md)
    
- [通过使用 Exchange 中的 SCP 查找来找到自动发现终结点](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [使用自动发现刷新配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [ExchangeService 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)
    
- [AutodiscoverService 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx)
    

