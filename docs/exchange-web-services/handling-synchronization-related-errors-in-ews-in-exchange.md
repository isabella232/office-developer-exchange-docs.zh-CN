---
title: 在 Exchange 中处理 EWS 中与同步相关的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: 了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中与同步相关的错误。
ms.openlocfilehash: f62937ec444d64b0b358581371f1260f565215b3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455938"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a>在 Exchange 中处理 EWS 中与同步相关的错误

了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中与同步相关的错误。
  
如果您的应用程序同步项目和文件夹，则您可能需要处理与同步相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。 其中大多数错误是由 EWS 托管 API 中的[ResponseCodeType](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx)枚举和 Exchange Web 服务（EWS）中的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)元素定义的。 
  
**表1。与同步相关的错误及其处理方法**

|**Error**|**当您尝试 .。。**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | 使用无效的同步状态值同步项目或文件夹。  <br/>  如果您的后续请求包含根文件夹，则在初始 SyncFolderHierarchy 请求中排除根文件夹。  <br/>  在后续请求中使用不同的根文件夹。  <br/> | 确保您要发送的同步状态值与上一次同步过程中返回的同步状态值相匹配。  <br/>  确保在尝试同步项目时不会发送文件夹层次结构的同步状态，反之亦然。  <br/>  确保您正在为正确的根文件夹发送同步状态。  <br/>  确保每个请求中指定了相同的根文件夹。  <br/>  确保上一个请求未指定 null 的根文件夹，而当前请求包含根的根文件夹。 Null 和根的处理方式不相同。  <br/> |
|ErrorSyncFolderNotFound  <br/> |同步无法在服务器上找到的文件夹中的子文件夹或项目。  <br/> |确保请求中指定的文件夹 ID 与以前的同步响应中从服务器返回的文件夹 ID 相匹配。  <br/> |
|ErrorTimeoutExpired  <br/> |发送的请求过多。  <br/> |将批处理限制为每个批次的10个项目，以避免受到[限制](ews-throttling-in-exchange.md)。  <br/> |
|[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |当服务器脱机或连接存在问题时连接到 EWS。  <br/> |请检查与服务器的连接并稍后重试请求。 这可能是暂时性的服务错误或网络错误。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 同步文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 同步项目](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

