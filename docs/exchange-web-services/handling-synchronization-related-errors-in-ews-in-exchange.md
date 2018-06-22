---
title: 在 Exchange 处理同步相关 EWS 中的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: 了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中同步相关的错误。
ms.openlocfilehash: 6de27d585e467d900941f34b2210877d17205502
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752720"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a>在 Exchange 处理同步相关 EWS 中的错误

了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中同步相关的错误。
  
如果您的应用程序同步项目和文件夹，您可能需要处理与同步相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。 大部分这些错误的[ResponseCodeType](http://msdn.microsoft.com/en-us/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx)枚举中 EWS 托管 API 和[ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)元素中 Exchange Web Services (EWS) 来定义。 
  
**表 1。同步相关错误和如何处理它们**

|**Error**|**您尝试对时发生...**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorInvalidSyncStateData  <br/> | 通过使用无效的同步状态值同步项目或文件夹。  <br/>  当您后续请求执行包含根文件夹排除在初始 SyncFolderHierarchy 请求中，根文件夹。  <br/>  使用在后续请求中的不同的根文件夹。  <br/> | 确保您要发送的匹配项的同步状态值同步状态返回的值以前同步过程中。  <br/>  确保您正在不发送的同步状态的文件夹层次结构当您尝试同步项时，反之亦然。  <br/>  确保您正在发送正确的根文件夹的同步状态。  <br/>  确保每个请求中，指定相同的根文件夹。  <br/>  确保在上一个请求没有当前请求中包括根根文件夹时指定 null、 根文件夹。 Null 和根不是视为相同。  <br/> |
|ErrorSyncFolderNotFound  <br/> |同步子文件夹或找不到的服务器的文件夹中的项目。  <br/> |确保文件夹请求中指定的 ID 匹配从以前的同步响应中的服务器返回文件夹 ID。  <br/> |
|ErrorTimeoutExpired  <br/> |发送太多的请求。  <br/> |限制为 10 个项目，每批次以避免获取[会限制](ews-throttling-in-exchange.md)您批次。  <br/> |
|[ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |连接到 EWS 服务器处于脱机状态或没有连接问题。  <br/> |检查服务器连接和更高版本重试您的请求。 这可能是临时服务错误或网络错误。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    
- [使用 EWS 在 Exchange 同步文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [使用 EWS 在 Exchange 同步的项目](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

