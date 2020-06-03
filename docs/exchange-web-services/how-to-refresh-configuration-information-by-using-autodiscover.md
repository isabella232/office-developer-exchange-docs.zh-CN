---
title: 使用自动发现刷新配置信息
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2f3c6a5-e8ea-4375-b41a-686a6f238d33
description: 了解如何以及何时使用自动发现刷新 Exchange 连接的配置信息。
ms.openlocfilehash: b9a4264d150d09b0e143e0bf7365af351bb2ef44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527752"
---
# <a name="refresh-configuration-information-by-using-autodiscover"></a>使用自动发现刷新配置信息

了解如何以及何时使用自动发现刷新 Exchange 连接的配置信息。
  
当您的 EWS 应用程序第一次运行时，自动发现为您收集所需的信息以连接到用户的 Exchange 邮箱提供了一种非常好的方法。 但自动发现并不仅用于首次使用。 定期使用自动发现有助于让应用程序对 Exchange 部署中的更改做出响应，从而帮助保持应用程序的连接。
  
## <a name="cache-autodiscover-endpoint-and-ews-settings"></a>缓存自动发现终结点和 EWS 设置
<a name="bk_CacheSettings"> </a>

尽管我们建议您定期使用自动发现，但在使用它时需要考虑一些事项。 理想情况下，您可以对环境中的更改进行快速平衡，以生成不必要的网络通信。 当应用程序首次获得成功的自动发现响应时，应保存以下信息，以便在每次发送 EWS 请求时无需重复自动发现过程。
  
**表1。用于自动发现请求的缓存信息**

|**设置为缓存**|**有效期为 .。。**|**详细信息**|
|:-----|:-----|:-----|
|自动发现终结点  <br/> |只要工作正常  <br/> |如果保存返回成功响应的自动发现终结点，则无需重复[生成自动发现终结点列表的](how-to-generate-a-list-of-autodiscover-endpoints.md)过程，并在收到成功的响应之前尝试这些终结点。<br/><br/> **注意**： EWS 托管 API 不支持缓存自动发现终结点。           |
|EWS URL 和从自动发现响应中检索到的任何其他设置  <br/> |一周  <br/> |通过保存 EWS URL 和其他相关设置，您无需为每个 EWS 请求[发送新的自动发现请求](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)，或者如果您的应用程序重新启动。 但是，即使 EWS URL 适用于你的用户，服务器的可用性也可能更佳。<br/><br/> 例如，用户的邮箱可能已移动到新的邮箱服务器，从而导致新的首选 EWS 终结点。 我们建议您在一周后通过发送新的自动发现请求来刷新您的用户设置（自上次的自动发现请求后）。 可以对此时间进行调整，以满足应用程序的要求。  <br/> |
   
## <a name="refresh-cached-configuration-information"></a>刷新缓存的配置信息
<a name="bk_RefreshConfig"> </a>

现在您已缓存了信息，我们来看看如何将缓存保持最新。 我们建议您在以下情况中刷新缓存的信息：
  
- 信息的有效期已过期。
    
- 将发生[与连接相关的错误](#bk_ConnectionErrors)，并且缓存的信息在一小时前进行刷新。
    
若要刷新缓存的信息，请向缓存的自动发现终结点发送自动发现请求，并执行以下操作：
  
- 如果请求成功，请将响应中的 EWS 终结点与缓存的 EWS 终结点进行比较，并执行以下操作：
    
  - 如果它们不同，则使用新的 EWS 终结点。 如果要刷新以从错误中恢复，请使用新终结点重试失败的请求。
    
  - 如果它们相同，则继续使用原始 EWS 终结点。 如果要刷新以从错误中恢复，请根据需要处理错误。
    
- 如果请求失败，则从头开始启动[自动发现过程](autodiscover-for-exchange.md)。 在收到成功的响应之后，将缓存的自动发现终结点替换为成功的自动发现终结点，并继续使用新的 EWS 终结点。 如果未收到成功的响应，请继续使用原始自动发现终结点和 EWS 终结点。 如果要刷新以从错误中恢复，请根据需要处理错误。 
    
下图提供了此过程的直观表示形式。
  
**图1。使用自动发现刷新配置信息的过程**

![此示意图说明自动发现如何刷新配置信息。](media/Ex15_Autodiscover_Refresh_Flowchart.png)
  
### <a name="connection-related-errors"></a>与连接相关的错误
<a name="bk_ConnectionErrors"> </a>

刷新缓存的配置信息有助于解决一些错误，但并非全部。 
  
**表2。通过刷新缓存解决的错误**

|**Error**|**EWS 托管 API 实现**|**备注**|
|:-----|:-----|:-----|
|DNS 或网络故障错误<br/><br/> 示例：找不到主机名。  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |指示找不到或无法达到服务器的任何错误都可能通过尝试自动发现来解决。 <br/><br/> 缓存的 EWS 终结点可能不再有效，并且自动发现可能会指向新服务器。  <br/> |
|HTTP 状态错误<br/><br/> 示例：503服务不可用  <br/> |[ServiceRemoteException](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.serviceremoteexception?view=exchange-ews-api) <br/> |HTTP 状态错误可能因多种原因而发生。<br/><br/> 但是，最好尝试使用自动发现以查看是否有新的 EWS 终结点可供用户使用。  <br/> |
|EWS 错误代码 <br/><br/> 示例： ErrorConnectionFailed <br/> |[ResponseCodeType](../web-service-reference/responsecode.md) <br/> | 大多数 EWS 错误代码不一定会刷新您的配置信息。<br/><br/> 但是，以下内容特别指出需要更新配置信息：<br/>- **ErrorConnectionFailed** <br/>- **ErrorMailboxMoveInProgress** <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 自动发现](autodiscover-for-exchange.md)  
- [生成自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [使用自动发现从 Exchange 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

