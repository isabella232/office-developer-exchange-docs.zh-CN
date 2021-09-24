---
title: 处理 EWS 中与同步相关的错误Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: 了解如何在应用程序中使用 EWS 托管 API 或 EWS 在应用程序中处理与同步Exchange。
ms.openlocfilehash: fd52b54413c6fc791132fb01b47bc9077d0266b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513246"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a>处理 EWS 中与同步相关的错误Exchange

了解如何在应用程序中使用 EWS 托管 API 或 EWS 在应用程序中处理与同步Exchange。
  
如果应用程序同步项目和文件夹，您可能必须处理与同步相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。 这些错误大部分由 EWS 托管 API 中的[ResponseCodeType](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx)枚举和 Exchange Web 服务中的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)元素 (EWS) 。 
  
**表 1.与同步相关的错误以及如何处理这些错误**

|**错误**|**在尝试...**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | 使用无效的同步状态值同步项目或文件夹。  <br/>  如果后续请求包含根文件夹，则排除初始 SyncFolderHierarchy 请求中的根文件夹。  <br/>  在后续请求中使用不同的根文件夹。  <br/> | 确保您发送的同步状态值与上一次同步期间返回的同步状态值匹配。  <br/>  确保在尝试同步项目时不会发送文件夹层次结构的同步状态，反之亦然。  <br/>  确保发送正确根文件夹的同步状态。  <br/>  确保在每个请求中指定相同的根文件夹。  <br/>  确保上一个请求未指定根文件夹 null，而当前请求包含根文件夹。 Null 和 root 不一样。  <br/> |
|ErrorSyncFolderNotFound  <br/> |同步服务器上找不到的文件夹中的子文件夹或项目。  <br/> |确保请求中指定的文件夹 ID 与之前同步响应中从服务器返回的文件夹 ID 相匹配。  <br/> |
|ErrorTimeoutExpired  <br/> |发送的请求过多。  <br/> |将批处理限制到每个批次 10 个项目，以避免 [受限制](ews-throttling-in-exchange.md)。  <br/> |
|[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |连接处于脱机状态或连接出现问题时，将更新为 EWS。  <br/> |检查与服务器的连接，稍后重试请求。 这很可能是暂时性服务错误或网络错误。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [邮箱同步和 Exchange 中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    
- [使用文件夹中的 EWS 同步Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [使用 EWS 同步Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

