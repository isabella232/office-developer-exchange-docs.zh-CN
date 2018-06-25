---
title: 使用自动发现刷新配置信息
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2f3c6a5-e8ea-4375-b41a-686a6f238d33
description: 了解如何以及何时使用自动发现刷新 Exchange 连接的配置信息。
ms.openlocfilehash: ef3b61781cbafa6e7b873336a050c0b8c33a28ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752896"
---
# <a name="refresh-configuration-information-by-using-autodiscover"></a>使用自动发现刷新配置信息

了解如何以及何时使用自动发现刷新 Exchange 连接的配置信息。
  
EWS 应用程序在首次运行时自动发现提供好方法，用于收集需要连接到用户的 Exchange 邮箱的信息。 但不只是为了第一次使用的自动发现。 使用自动发现定期有助于保护您的应用程序通过使其连接响应 Exchange 部署中的更改。
  
## <a name="cache-autodiscover-endpoint-and-ews-settings"></a>缓存自动发现终结点和 EWS 设置
<a name="bk_CacheSettings"> </a>

尽管我们建议使用自动发现定期，您需要经常如何使用它需要一些注意事项。 理想情况下，您可以平衡快速响应针对生成不必要的网络流量过大环境中的更改。 当您的应用程序获取第一次成功的自动发现响应时，您应保存的以下信息，以便没有重复的自动发现过程，每次发送 EWS 请求。
  
**表 1。为缓存的自动发现请求的信息**

|**缓存设置**|**供...**|**详细信息**|
|:-----|:-----|:-----|
|自动发现终结点  <br/> |只要及其工作方式  <br/> |保存时返回成功响应的自动发现终结点，您不必重复此过程的[生成的自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)和试用它们，直到您到达成功响应。<br/><br/> **注意**： EWS 托管 API 不支持缓存的自动发现终结点。           |
|从自动发现响应检索 EWS URL 和任何其他设置  <br/> |24 小时制  <br/> |通过将保存的 EWS URL 和其他相关的设置，您没有要为每个 EWS 请求[发送一个新的自动发现请求](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)，或者如果您的应用程序重新启动。 但是，即使 EWS URL 适用于您的用户，服务器可能可用的更佳。<br/><br/> 例如，可能已经用户的邮箱移到新的邮箱服务器，从而导致一个新的首选 EWS 终结点。 我们建议您通过以来最后一个自动发现请求过去 24 小时后发送的新的自动发现请求刷新您的用户设置。 这次可以调整以满足您的应用程序的要求。  <br/> |
   
## <a name="refresh-cached-configuration-information"></a>刷新缓存的配置信息
<a name="bk_RefreshConfig"> </a>

既然您已经缓存的信息，让我们看一下如何保留该缓存刷新。 我们建议您刷新缓存的信息时：
  
- 信息的有效期过期。
    
- [与连接相关的错误](#bk_ConnectionErrors)，发生此事件。 
    
若要刷新缓存的信息，请将自动发现请求发送到缓存的自动发现终结点，并执行下列操作：
  
- 如果请求成功，比较的响应中的 EWS 终结点与缓存 EWS 终结点，并执行下列操作：
    
  - 如果不一致，使用新的 EWS 终结点。 如果刷新从错误中恢复，请重试的新的终结点的失败的请求。
    
  - 如果它们是相同的继续使用原始 EWS 终结点。 如果您是刷新从错误中恢复，处理根据错误。
    
- 如果请求失败，从头开始[自动发现过程](autodiscover-for-exchange.md)。 获得成功响应后，替换成功并继续使用新的 EWS 终结点的自动发现终结点的缓存的自动发现终结点。 如果您没有得到成功的响应，继续使用的原始自动发现终结点和 EWS 终结点。 如果您是刷新从错误中恢复，处理根据错误。 
    
下图提供了此过程的直观表示形式。
  
**图 1。通过使用自动发现刷新配置信息的过程**

![此示意图说明自动发现如何刷新配置信息。](media/Ex15_Autodiscover_Refresh_Flowchart.png)
  
### <a name="connection-related-errors"></a>与连接相关的错误
<a name="bk_ConnectionErrors"> </a>

刷新缓存的配置信息可帮助进行一些错误，而不是所有。 
  
**表 2。错误由刷新缓存**

|**Error**|**EWS 托管 API 实现**|**备注**|
|:-----|:-----|:-----|
|DNS 或网络失败错误<br/><br/> 示例： 找不到主机名。  <br/> |[ServiceRemoteException](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ServiceRemoteException.aspx) <br/> |可能通过尝试自动发现解决任何错误，指示服务器无法找到或无法联系。 <br/><br/> 您缓存的 EWS 终结点可能不再有效，并且自动发现可能能够您指向新的服务器。  <br/> |
|HTTP 状态错误<br/><br/> 示例： 503 服务不可用  <br/> |[ServiceRemoteException](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ServiceRemoteException.aspx) <br/> |HTTP 状态错误可能不同的原因。<br/><br/> 但是，最好尝试自动发现新的 EWS 终结点可供用户。  <br/> |
|EWS 错误代码 <br/><br/> 示例： ErrorConnectionFailed <br/> |[ResponseCodeType](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ResponseCodeType.aspx) <br/> | 大多数 EWS 错误代码不保证刷新配置信息。<br/><br/> 但是，以下专门指示需要更新的配置信息：<br/>- **ErrorConnectionFailed** <br/>- **ErrorMailboxMoveInProgress** <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 自动发现](autodiscover-for-exchange.md)  
- [生成自动发现终结点的列表](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [通过使用自动发现 Exchange 中获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

