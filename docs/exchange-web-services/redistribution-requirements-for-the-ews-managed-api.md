---
title: EWS 托管 API 的再分发要求
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: 了解如何使用应用程序重新分发 EWS 托管 API 程序集。
ms.openlocfilehash: f43156838c735cfc17106deb7860329d3da6c07a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531328"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a>EWS 托管 API 的再分发要求

了解如何使用应用程序重新分发 EWS 托管 API 程序集。
  
在设计 EWS 托管 API 应用程序时，还需要考虑如何向用户发布它。 
  
## <a name="redistributing-your-ews-managed-api-application"></a>重新分发 EWS 托管 API 应用程序

除非您的应用程序位于 Exchange服务器上，否则您需要重新分发 EWS 托管 API 程序集。 EWS 托管 API 下载包含两个可以重新分发的程序集：Microsoft.Exchange.WebServices.dll 和 Microsoft.Exchange.WebServices.Auth.dll。 在设计发布 EWS 托管 API 应用程序的方式时，请记住以下信息：
  
- EWS 托管 API 的设计使你可以下载它，并将其与面向 Exchange 服务器的应用程序一起分发。 或者，您的应用程序可以下载 EWS 托管 API。
    
- 您可以使用 EWS 托管 API 与运行 Exchange Online 的 Exchange 服务器、作为 Office 365 一部分的 Exchange Online 或本地版本的 Exchange（从 Exchange Server 2007 开始）进行通信。
    
- 在从版本 2.1 开始的版本 EWS 托管 API 中，可以在 GAC (全局程序集缓存中) 。 MSI 会自动将 DLL 添加到 GAC，并且将基于每台计算机（而不是基于每个用户）进行访问。
    
许可条款包含在 EWS 托管 API 下载中。 查看术语，了解可以使用 EWS 托管 API 执行哪些操作的权威信息。
  
## <a name="see-also"></a>另请参阅


- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    
- [EWS 托管 API (下载) ](https://aka.ms/ews-managed-api-readme)
    

