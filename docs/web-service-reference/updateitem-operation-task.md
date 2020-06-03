---
title: UpdateItem 操作（任务）
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
ms.openlocfilehash: 0041af114d11fd9577037dd154e40b84e8483c35
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459803"
---
# <a name="updateitem-operation-task"></a>UpdateItem 操作（任务）

UpdateItem 操作用于更新 Exchange 存储中的任务项属性。
  
## <a name="remarks"></a>备注

不能使用 Exchange Web 服务发送任务请求。 Exchange Web 服务可以返回由 MicrosoftOfficeOutlook 创建的任务请求。 如果已发送任务请求，则更新该任务的请求将返回错误。
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a>更新定期任务的当前事件

定期任务的 UpdateItem 操作的结果与单个非定期任务上的 UpdateItem 操作的结果不同。 在进行以下更新时，对定期任务的发生所做的更改会导致生成一次性任务：
  
1. 将重新生成或 nonregenerating 重复性任务的 status 属性设置为 "**已完成**"。
    
2. Nonregenerating 重复性任务的开始日期或结束日期已更改。
    
例如，如果**UpdateItem**请求将定期任务的已完成值设置为**True**，则**UpdateItemResponse**将包含一个新的 Id 和 ChangeKey，表示新创建的一次性任务。 请求中包含的 Id 仍有效，并且该 Id 表示的定期任务已更新，以表示下一个事件。 由于定期任务已更新，因此请求中包含的 ChangeKey 已不再有效。 
  
您可以使用[GetItem 操作](getitem-operation.md)获取定期任务的最新**ChangeKey** 。 
  
对于非定期任务或定期任务的最后一次发生，UpdateItem 响应将返回传递给它的同一**Id** ，并返回关联的更新的**ChangeKey**。
  
## <a name="see-also"></a>另请参阅



[UpdateItem 操作](updateitem-operation.md)

