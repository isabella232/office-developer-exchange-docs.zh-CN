---
title: EWS 托管 API 的再分发要求
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8b206274-eaa4-40d3-b504-af27335c8f43
description: 了解如何使用应用程序重新分发 EWS 托管 API 程序集。
ms.openlocfilehash: e64b4cdb8938caa819ba30621112a25946ef0424
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463823"
---
# <a name="redistribution-requirements-for-the-ews-managed-api"></a>EWS 托管 API 的再分发要求

了解如何使用应用程序重新分发 EWS 托管 API 程序集。
  
在设计 EWS 托管 API 应用程序时，您还需要考虑将其发布给用户的方式。 
  
## <a name="redistributing-your-ews-managed-api-application"></a>重新分发您的 EWS 托管 API 应用程序

除非您的应用程序位于 Exchange 服务器上，否则您将需要重新发布 EWS 托管 API 程序集。 EWS 托管 API 下载包含两个可以重新发布的程序集： WebServices 和 WebServices。. "。 在设计如何释放 EWS 托管 API 应用程序时，请记住以下信息：
  
- EWS 托管 API 的设计使您可以下载它，并将其与面向 Exchange server 的应用程序一起分发。 或者，您的应用程序可以下载 EWS 托管 API。
    
- 您可以使用 EWS 托管 API 与运行 Exchange Online 的 Exchange 服务器、作为 Office 365 的一部分的 Exchange Online 或从 Exchange Server 2007 开始的 Exchange 内部部署版本进行通信。
    
- 在从版本2.1 开始的 EWS 托管 API 的各个版本中，您可以在全局程序集缓存（GAC）中安装 API。 MSI 将自动将 DLL 添加到 GAC 中，并且可以在每台计算机上访问，而不是每个用户都可以访问。
    
该许可条款包含在 EWS 托管 API 下载中。 查看有关可以使用 EWS 托管 API 执行的操作的权威信息的术语。
  
## <a name="see-also"></a>另请参阅


- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    
- [EWS 托管 API （下载）](https://aka.ms/ews-managed-api-readme)
    

