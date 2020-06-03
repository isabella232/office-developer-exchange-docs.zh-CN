---
title: DeleteItem
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
description: DeleteItem 元素定义一个请求，以从 Exchange 存储中的邮箱中删除项目。
ms.openlocfilehash: ed13ee32b487f49740aed80e8705257d3e2e6938
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529201"
---
# <a name="deleteitem"></a>DeleteItem

**DeleteItem**元素定义一个请求，以从 Exchange 存储中的邮箱中删除项目。 
  
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
|**SendMeetingCancellations** <br/> |描述是否将日历项目删除操作传递给与会者。 删除日历项目时，此属性是必需的。 如果删除非日历项目，则此属性是可选的。  <br/> |
|**AffectedTaskOccurrences** <br/> |描述任务实例或任务主控形状是否由[DeleteItem 操作](deleteitem-operation.md)删除。 删除任务时，此属性是必需的。 当非任务项目被删除时，此属性是可选的。  <br/> |
|**SuppressReadReceipts** <br/> |指示是否禁止显示已删除项目的已读回执。 如果文本值为**true**，则表示已取消阅读回执。 **如果值为 false** ，则表示已将已读回执发送到发件人。 此特性是可选的。  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType 属性

|**值**|**说明**|
|:-----|:-----|
|HardDelete  <br/> |项目已从存储区中永久删除。  <br/> |
|SoftDelete  <br/> |如果启用了转储程序，则会将项目移动到转储程序。  <br/> |
|MoveToDeletedItems  <br/> |将项目移动到"已删除邮件"文件夹中。  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a>SendMeetingCancellations 属性

|**值**|**说明**|
|:-----|:-----|
|SendToNone  <br/> |删除日历项目，但不发送取消邮件。  <br/> |
|SendOnlyToAll  <br/> |删除日历项目并向所有与会者发送取消邮件。  <br/> |
|SendToAllAndSaveCopy  <br/> |删除日历项目并向所有与会者发送取消邮件。 取消邮件的副本保存在 "已发送邮件" 文件夹中。  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a>AffectedTaskOccurrences 属性

|**值**|**说明**|
|:-----|:-----|
|AllOccurrences  <br/> |"删除项目" 请求会删除主任务，从而删除与主任务相关联的所有定期任务。  <br/> |
|SpecifiedOccurrenceOnly  <br/> |"删除项目" 请求仅删除任务的特定事件。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |包含要从 Exchange 存储中的邮箱中删除的项、具体值项和定期主项目的数组。 可以对任何项目类型执行[DeleteItem 操作](deleteitem-operation.md)。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

**MoveToDeletedItems** 和 **HardDelete** 选项是事务性的这意味着，Web 服务调用完成时，数据库将邮件移至已删除邮件文件夹或从Exchange数据库中永久删除该项目。这种行为是相同的MicrosoftExchange Server 2007和Exchange Server 2010。 
  
Exchange 的不同目标版本的**SoftDelete**选项的工作方式不同。 **SoftDelete** for exchange 2007 在项目中设置一个位，以指示 exchange 数据库，该项目将在将来的不确定时间移动到转储程序文件夹中。 **SoftDelete** for Exchange 2010 立即将项目移动到转储程序。 **SoftDelete**不是文件夹删除的选项。 **SoftDelete**遍历项目和文件夹的搜索不会返回任何结果。 
  
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

