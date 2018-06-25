---
title: EWS 托管 API 的重新分发要求
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: 了解如何在应用程序再发行 EWS 托管 API 程序集。
ms.openlocfilehash: d8fc57c4a2b3ed7d6218aeeed0fe88c2d3e0fbe0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753004"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a>EWS 托管 API 的重新分发要求

了解如何在应用程序再发行 EWS 托管 API 程序集。
  
在设计 EWS 托管 API 应用程序时，您还需要考虑如何您将其释放到您的用户。 
  
## <a name="redistributing-your-ews-managed-api-application"></a>重新分发 EWS 托管 API 应用程序

除非您的应用程序位于 Exchange 服务器上，您将需要重新分发本 EWS 托管 API 的程序集。 EWS 托管 API 下载包含两个程序集，您可以重新分发本： Microsoft.Exchange.WebServices.dll 和 Microsoft.Exchange.WebServices.Auth.dll。 如何将发布 EWS 托管 API 应用程序在设计时，请牢记以下信息：
  
- EWS 托管 API 旨在以便您可以下载它并将其与您的 Exchange 服务器的应用程序。 此外，您的应用程序可以下载 EWS 托管 API。
    
- EWS 托管 API 可用于与运行 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 开头 Exchange Server 2007 的本地版本的 Exchange 服务器进行通信。
    
- EWS 托管 API 开头 2.1 版的版本中，您可以安装在全局程序集缓存 (GAC) 中的 API。 MSI 将自动添加到 GAC DLL，并将访问每个计算机为基础，而不上每个用户分别。
    
许可条款都包含在 EWS 托管 API 下载。 查看有关如何使用 EWS 托管 API 的权威信息条款。
  
## <a name="see-also"></a>另请参阅


- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    
- [EWS 托管 API （下载）](http://aka.ms/ews-managed-api-readme)
    

