---
title: 删除项
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: 删除项元素定义从 Exchange 存储中的邮箱中删除项目的请求。
ms.openlocfilehash: de64787750c88c8a47bb69daddc0a1d2ebe8bde9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753816"
---
# <a name="deleteitem"></a>删除项

**删除项**元素定义从 Exchange 存储中的邮箱中删除项目的请求。 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 **DeleteItemType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**DeleteType** <br/> |介绍如何删除项目。 此属性是必需的。  <br/> |
|**SendMeetingCancellations** <br/> |描述是否将日历项删除传送给与会者。 删除日历项目时，此属性是必需的。 此属性是可选的如果删除非日历项目。  <br/> |
|**AffectedTaskOccurrences** <br/> |描述是否通过[删除项操作](deleteitem-operation.md)删除任务实例或任务主控形状。 在删除任务时，此属性是必需的。 非任务项将被删除时，此属性是可选的。  <br/> |
|**SuppressReadReceipts** <br/> |指示是否将禁止显示已删除项已读的回执。 文本值为**true**，指示已读的回执被禁止。 如果值为**false**指示已读的回执，会向发件人发送。 此属性是可选的。  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType 属性

|**值**|**说明**|
|:-----|:-----|
|HardDelete  <br/> |从存储永久删除项目。  <br/> |
|SoftDelete  <br/> |将项目移动到转储程序如果转储程序已启用。  <br/> |
|MoveToDeletedItems  <br/> |将项目移动到已删除邮件文件夹。  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a>SendMeetingCancellations 属性

|**值**|**说明**|
|:-----|:-----|
|SendToNone  <br/> |日历项目而不发送取消邮件中删除。  <br/> |
|SendOnlyToAll  <br/> |日历项目被删除，取消邮件发送给所有与会者。  <br/> |
|SendToAllAndSaveCopy  <br/> |日历项目被删除，取消邮件发送给所有与会者。 在已发送邮件文件夹中保存一份取消邮件。  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a>AffectedTaskOccurrences 属性

|**值**|**说明**|
|:-----|:-----|
|AllOccurrences  <br/> |删除项目请求删除主控形状的任务中，，因此所有定期任务的与主任务关联。  <br/> |
|SpecifiedOccurrenceOnly  <br/> |删除项目请求删除任务的仅特定事件。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |包含项目、 匹配项和定期主项目以从 Exchange 存储的邮箱中删除一个数组。 可以在任何项类型上执行[删除项操作](deleteitem-operation.md)。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

**MoveToDeletedItems** 和 **HardDelete** 选项是事务性的这意味着，Web 服务调用完成时，数据库将邮件移至已删除邮件文件夹或从Exchange数据库中永久删除该项目。这种行为是相同的MicrosoftExchange Server 2007和Exchange Server 2010。 
  
**SoftDelete**选项不同的目标版本的 Exchange 的工作方式。 Exchange 2007 **SoftDelete**在表示项目将移至 Exchange 数据库的项目上设置位转储程序文件夹的将来确定的时间。 对于 Exchange 2010 **SoftDelete**立即移动到的项转储程序。 **SoftDelete**不为文件夹删除选项。 项目和文件夹的**SoftDelete**遍历搜索不会返回任何结果。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [DeleteItemResponse](deleteitemresponse.md)  
- [删除项操作](deleteitem-operation.md)

