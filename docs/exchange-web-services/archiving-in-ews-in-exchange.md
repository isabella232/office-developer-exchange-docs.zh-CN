---
title: 在 Exchange 存档中的 ews
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: 了解有关在 Exchange 存档中的 ews。
ms.openlocfilehash: bc282a7774bb74e57550bc663512987839324b83
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752697"
---
# <a name="archiving-in-ews-in-exchange"></a>在 Exchange 存档中的 ews

了解有关在 Exchange 存档中的 ews。
  
存档邮箱的第二与用户关联的邮箱。 存档邮箱通常用于管理电子邮件存储限制。 例如，旧的电子邮件项可能会定期从移收件箱到存档邮箱。 
  
Exchange Online、 Exchange Online 作为 Office 365 和 Exchange Server 2013 的一部分介绍可用于存档的一组从主邮箱的邮件项目的两个新的 Exchange Web Services (EWS) 操作。 这种方式的收件箱项目存档保留的项目的文件夹层次结构。 此外，现在可以在客户端，本地或是大多数情况下不透明给用户，通过使用文件夹路径指向存档的内容的方式在远程存储存档邮箱。
  
## <a name="archiving-operations-in-ews"></a>存档中的 ews 操作

下表列出了 Exchange 2013 中引入的存档操作。 
  
|**操作名称**|**说明**|
|:-----|:-----|
|[ArchiveItem](http://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |将项目从主邮箱移动到存档邮箱。  <br/> |
|[CreateFolderPath](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |创建指向的存档邮箱的存储位置的 URI。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

