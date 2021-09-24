---
title: UpdateItem 操作（任务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: UpdateItem 操作用于更新任务项存储中Exchange属性。
ms.openlocfilehash: a268b4b281f149f14bc6c48a774fc9071093ebb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510748"
---
# <a name="updateitem-operation-task"></a>UpdateItem 操作（任务）

UpdateItem 操作用于更新任务项存储中Exchange属性。
  
## <a name="remarks"></a>注解

不能使用 Exchange Web 服务发送任务请求。 ExchangeWeb 服务可以返回由 MicrosoftOfficeOutlook 创建的任务请求。 如果已发送任务请求，则更新任务的请求将返回错误。
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a>更新定期任务的当前事件

对定期任务执行 UpdateItem 操作的结果与单个非定期任务的 UpdateItem 操作结果不同。 对定期任务的发生所做的更改将导致在进行以下更新时生成一次性任务：
  
1. 重新生成的重复任务或非重生成重复任务的 status 属性设置为 **Completed**。
    
2. 更改非定期定期任务的开始日期或结束日期。
    
例如，如果 **UpdateItem** 请求将定期任务的 Completed 值设置为 **true，****则 UpdateItemResponse** 将包含一个新 Id 和 ChangeKey，分别代表新创建的一次性任务。 请求中包含的 ID 仍然有效，并且由该 ID 表示的定期任务已更新为表示下一个事件。 请求中包含的 ChangeKey 不再有效，因为定期任务已更新。 
  
可以使用 [GetItem 操作](getitem-operation.md)获取定期任务的最新 **ChangeKey。** 
  
对于非定期任务或最后一次出现的定期任务，UpdateItem 响应返回传递给它的同一 **ID，** 并返回关联的更新 **的 ChangeKey**。
  
## <a name="see-also"></a>另请参阅



[UpdateItem 操作](updateitem-operation.md)

