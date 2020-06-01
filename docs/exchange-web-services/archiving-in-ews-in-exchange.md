---
title: 在 Exchange 中 EWS 存档
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: 了解 Exchange 中 EWS 的存档。
ms.openlocfilehash: b433b9f88905ee255720e8b341d560fa0e464975
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456211"
---
# <a name="archiving-in-ews-in-exchange"></a>在 Exchange 中 EWS 存档

了解 Exchange 中 EWS 的存档。
  
存档邮箱是与用户相关联的辅助邮箱。 存档邮箱通常用于管理电子邮件存储限制。 例如，较旧的电子邮件项目可能会定期从收件箱移动到存档邮箱。 
  
Exchange Online，Exchange Online 作为 Office 365 的一部分，Exchange Server 2013 介绍了两种新的 Exchange Web 服务（EWS）操作，可用于存档主邮箱中的一组邮件项目。 以这种方式存档收件箱项目可保留项目的文件夹层次结构。 此外，存档邮箱现在可以本地存储在客户端上，也可以远程存储为用户对用户不透明的方式，方法是使用文件夹路径指向存档的内容。
  
## <a name="archiving-operations-in-ews"></a>在 EWS 中存档操作

下表列出了在 Exchange 2013 中引入的存档操作。 
  
|**操作名称**|**说明**|
|:-----|:-----|
|[ArchiveItem](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |将项目从主邮箱移动到存档邮箱。  <br/> |
|[CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |创建指向存档邮箱的存储位置的 URI。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

