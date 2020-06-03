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
description: UpdateItem 元素定义一个请求以更新邮箱中的项目。
ms.openlocfilehash: 43821db58457ffce22be918a7ba6427f57230010
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466568"
---
# <a name="updateitem"></a>UpdateItem

**UpdateItem**元素定义一个请求以更新邮箱中的项目。 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 **UpdateItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ConflictResolution** <br/> |标识在更新过程中要尝试的冲突解决的类型。 默认值为 "自动解析"。  <br/> |
|**MessageDisposition** <br/> |介绍如何在更新项目后对其进行处理。 邮件项目（包括会议邮件（如会议取消、会议请求和会议响应）需要**MessageDisposition**属性。  <br/> |
|**SendMeetingInvitationsOrCancellations** <br/> |介绍如何在更新日历项目后传达会议更新。 此属性是日历项目和日历项目发生的必要条件。  <br/> |
|**SuppressReadReceipts** <br/> |指示是否应禁止显示已更新项目的已读回执。 如果文本值**为 true，则**表示应禁止显示已读回执。 **如果值为 false** ，则表示已将已读回执发送给发件人。 此特性是可选的。  <br/> 此属性是在 Exchange Server 2013 SP1 中引入的。  <br/> |
   
#### <a name="conflictresolution-attribute"></a>ConflictResolution 属性

|**值**|**说明**|
|:-----|:-----|
|NeverOverwrite  <br/> |如果存在冲突，更新操作将失败并返回错误。  <br/> |
|解决  <br/> |更新操作将自动解决任何冲突。  <br/> |
|AlwaysOverwrite  <br/> |如果存在冲突，更新操作将覆盖信息。  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition 属性

|**值**|**说明**|
|:-----|:-----|
|SaveOnly  <br/> |更新项目并将其保存回其当前文件夹。  <br/> |
|SendOnly  <br/> |更新并发送项目，但不保存副本。  <br/> |
|SendAndSaveCopy  <br/> |更新项目并将副本保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a>SendMeetingInvitationsOrCancellations 属性

|**值**|**说明**|
|:-----|:-----|
|SendToNone  <br/> |日历项目已更新，但未将更新发送给与会者。  <br/> |
|SendOnlyToAll  <br/> |将更新日历项目并将会议更新发送给所有与会者，但不会将其保存在 "已发送邮件" 文件夹中。  <br/> |
|SendOnlyToChanged  <br/> |将更新日历项目，并且仅向受会议更改影响的与会者发送会议更新。  <br/> |
|SendToAllAndSaveCopy  <br/> |更新日历项目，将会议更新发送给所有与会者，并将副本保存在 "已发送邮件" 文件夹中。  <br/> |
|SendToChangedAndSaveCopy  <br/> |更新日历项目，将会议更新发送给受会议更改影响的所有与会者，并将副本保存在 "已发送邮件" 文件夹中。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |标识在 Exchange 存储中更新、发送和创建项目的操作的目标文件夹。  <br/> |
|[ItemChanges](itemchanges.md) <br/> |包含标识项目和要应用于项目的更新的[ItemChange](itemchange.md)元素的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateItem 操作](updateitem-operation.md)

