---
title: UpdateItem
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
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: UpdateItem 元素定义一个请求来更新邮箱中的项。
ms.openlocfilehash: 7b9b5f1dcffb95eb127572cb91f92d961c05a77e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2018
ms.locfileid: "19838405"
---
# <a name="updateitem"></a>UpdateItem

**UpdateItem**元素定义一个请求来更新邮箱中的项。 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 **UpdateItemType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**ConflictResolution** <br/> |标识指定在冲突解决尝试更新期间的类型。 默认值是自动解析。  <br/> |
|**MessageDisposition** <br/> |描述更新后如何处理项目。 对于邮件项，包括会议消息，如会议取消、 会议请求和会议响应需要**MessageDisposition**属性。  <br/> |
|**SendMeetingInvitationsOrCancellations** <br/> |介绍如何更新日历项目后传递会议更新。 此属性是必需的日历项目和日历项发生次数。  <br/> |
|**SuppressReadReceipts** <br/> |指示是否应禁止显示更新项已读的回执。 文本值为**true**指示的 read 应禁止显示回执。 如果值为**false**指示将向发件人发送已读的回执。 此属性是可选的。  <br/> 此属性是在 Exchange Server 2013 SP1 中引入的。  <br/> |
   
#### <a name="conflictresolution-attribute"></a>ConflictResolution 属性

|**值**|**说明**|
|:-----|:-----|
|NeverOverwrite  <br/> |如果没有冲突，更新操作失败，并返回一个错误。  <br/> |
|自动解析  <br/> |更新操作自动解决任何冲突。  <br/> |
|AlwaysOverwrite  <br/> |如果没有冲突，更新操作将覆盖信息。  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition 属性

|**值**|**说明**|
|:-----|:-----|
|SaveOnly  <br/> |项目更新并保存回其当前文件夹。  <br/> |
|SendOnly  <br/> |更新和发送项目，但没有副本保存。  <br/> |
|SendAndSaveCopy  <br/> |副本保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹和更新项目。  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a>SendMeetingInvitationsOrCancellations 属性

|**值**|**说明**|
|:-----|:-----|
|SendToNone  <br/> |更新日历项目，但不是将更新发送给与会者。  <br/> |
|SendOnlyToAll  <br/> |更新日历项和会议更新发送给所有与会者，但不是保存在已发送邮件文件夹中。  <br/> |
|SendOnlyToChanged  <br/> |会议更新仅发送给与会者受影响的会议中的更改和更新的日历项目。  <br/> |
|SendToAllAndSaveCopy  <br/> |更新日历项、 会议更新发送给所有与会者，和副本保存在已发送邮件文件夹。  <br/> |
|SendToChangedAndSaveCopy  <br/> |更新日历项、 会议更新发送到在会议中，更改影响的所有与会者和副本保存在已发送邮件文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |标识用于更新、 发送和在 Exchange 存储中创建项目的操作的目标文件夹。  <br/> |
|[ItemChanges](itemchanges.md) <br/> |包含确定项目和更新以应用于项目的[ItemChange](itemchange.md)元素的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateItem 操作](updateitem-operation.md)

