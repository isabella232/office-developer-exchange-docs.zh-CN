---
title: DeleteItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: DeleteItem 元素定义从邮件存储中的邮箱删除Exchange请求。
ms.openlocfilehash: aa421de447126a22c1f01b3a0dc7498ff5b74a65
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528885"
---
# <a name="deleteitem"></a>DeleteItem

**DeleteItem** 元素定义从邮件存储中的邮箱中删除Exchange请求。 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 **DeleteItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**DeleteType** <br/> |介绍如何删除项目。 此特性是必需的。  <br/> |
|**SendMeetingCancellations** <br/> |描述是否向与会者传达日历项目删除。 删除日历项目时，此属性是必需的。 如果删除非日历项目，则此属性是可选的。  <br/> |
|**AffectedTaskOccurrences** <br/> |描述任务实例或任务母版是否被 [DeleteItem](deleteitem-operation.md)操作删除。 删除任务时，此属性是必需的。 当删除非任务项目时，此属性是可选的。  <br/> |
|**SuppressReadReceipts** <br/> |指示是否抑制已删除项目的已读回执。 文本值为 **true**，表示已读回执被抑制。 false **值表示** 将已读回执发送给发件人。 此特性是可选的。  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType 属性

|**值**|**说明**|
|:-----|:-----|
|HardDelete  <br/> |从存储区中永久删除项目。  <br/> |
|SoftDelete  <br/> |如果启用了垃圾站，项将移动到垃圾站。  <br/> |
|MoveToDeletedItems  <br/> |将项目移动到"已删除邮件"文件夹中。  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a>SendMeetingCancellations 属性

|**值**|**说明**|
|:-----|:-----|
|SendToNone  <br/> |在不发送取消消息的情况下删除日历项目。  <br/> |
|SendOnlyToAll  <br/> |日历项目将被删除，并且会向所有与会者发送取消邮件。  <br/> |
|SendToAllAndSaveCopy  <br/> |日历项目将被删除，并且会向所有与会者发送取消邮件。 取消邮件的副本保存在"已发送项目"文件夹中。  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a>AffectedTaskOccurrences 属性

|**值**|**说明**|
|:-----|:-----|
|AllOccurrences  <br/> |删除项目请求将删除主任务，因此删除与主任务关联的所有定期任务。  <br/> |
|SpecifiedOccurrenceOnly  <br/> |删除项目请求仅删除任务的特定匹配项。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |包含从邮件存储中的邮箱中删除的项目、事件项目和定期Exchange数组。 [DeleteItem 操作](deleteitem-operation.md)可以在任何项目类型上执行。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

**MoveToDeletedItems** 和 **HardDelete** 选项是事务性的这意味着，Web 服务调用完成时，数据库将邮件移至已删除邮件文件夹或从Exchange数据库中永久删除该项目。这种行为是相同的MicrosoftExchange Server 2007和Exchange Server 2010。 
  
**SoftDelete** 选项对不同目标版本的 Exchange。 Exchange 2007 的 **SoftDelete** 对项目设置一个位，以指示项目将在不确定的时间移动到 Exchange 数据库。 **SoftDelete** for Exchange 2010 immediately moves the item to the dumpster. **SoftDelete** 不是用于删除文件夹的选项。 **SoftDelete** 遍历项目和文件夹的搜索不会返回任何结果。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [DeleteItemResponse](deleteitemresponse.md)  
- [DeleteItem 操作](deleteitem-operation.md)

