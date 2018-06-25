---
title: UpdateItem 操作 （任务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: UpdateItem 操作用于更新 Exchange 存储中的任务项属性。
ms.openlocfilehash: d6f966fa663300b476383a136d30cf611d6bfb9b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838400"
---
# <a name="updateitem-operation-task"></a>UpdateItem 操作 （任务）

UpdateItem 操作用于更新 Exchange 存储中的任务项属性。
  
## <a name="remarks"></a>注解

您无法使用 Exchange Web 服务发送任务请求。 Exchange Web 服务可以返回由 MicrosoftOfficeOutlook 创建的任务请求。 如果已发送的任务请求，请求更新任务将返回错误。
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a>更新定期任务的当前匹配项

定期任务 UpdateItem 操作的结果与单个、 非定期任务 UpdateItem 操作的结果。 定期任务出现更改导致一次性任务要生成时进行以下更新：
  
1. 重新生成或 nonregenerating 重复性任务的 status 属性设置为**已完成**。
    
2. 更改的开始日期或结束日期 nonregenerating 重复性任务。
    
例如，如果**UpdateItem**请求将定期任务的完成值设置为**true**， **UpdateItemResponse**将包含新 Id 和更改密钥表示新创建的一次性任务。 仍然有效请求中包含的 Id，并由该 Id 定期任务已更新，以表示的下一个匹配项。 包含在请求中更改密钥不再有效，因为已更新周期性任务。 
  
可以使用[GetItem 操作](getitem-operation.md)获取最新**更改密钥**周期性任务。 
  
对于非定期任务或定期任务的最后一个实例，UpdateItem 响应将返回相同的**Id**的已传递给它，并返回关联的更新**更改密钥**。
  
## <a name="see-also"></a>另请参阅



[UpdateItem 操作](updateitem-operation.md)

