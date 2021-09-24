---
title: 在 Exchange 中 EWS 存档
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: 了解 EWS 中Exchange。
ms.openlocfilehash: f2ca4cc783556b089b732c75d166b77c0dcd891c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520225"
---
# <a name="archiving-in-ews-in-exchange"></a>在 Exchange 中 EWS 存档

了解 EWS 中Exchange。
  
存档邮箱是与用户关联的辅助邮箱。 存档邮箱通常用于管理电子邮件存储限制。 例如，较旧的电子邮件项目可能会定期从收件箱移动到存档邮箱。 
  
Exchange Online，Exchange Online Office 365 的一部分，Exchange Server 2013 引入了两个新的 Exchange Web 服务 (EWS) 操作，您可以使用这些操作存档主邮箱中的一组邮件项目。 这样存档收件箱项目将保留项目的文件夹层次结构。 此外，通过使用文件夹路径指向存档的内容，存档邮箱现在可以本地存储在客户端上，也可以远程存储，方式对于用户来说主要是不透明的。
  
## <a name="archiving-operations-in-ews"></a>EWS 中的存档操作

下表列出了 2013 年 3 月引入Exchange操作。 
  
|**操作名称**|**说明**|
|:-----|:-----|
|[ArchiveItem](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |将项目从主邮箱移动到存档邮箱。  <br/> |
|[CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |创建指向存档邮箱的存储位置的 URI。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

