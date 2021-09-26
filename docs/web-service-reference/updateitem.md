---
title: UpdateItem
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
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: UpdateItem 元素定义更新邮箱中的项目的请求。
ms.openlocfilehash: 544ccfb8c42b2a4d4f69ae04d383233203c235b8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542785"
---
# <a name="updateitem"></a>UpdateItem

**UpdateItem** 元素定义更新邮箱中的项目的请求。 
  
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
|**ConflictResolution** <br/> |标识在更新期间尝试解决冲突的类型。 默认值为 AutoResolve。  <br/> |
|**MessageDisposition** <br/> |描述更新项目后如何处理该项目。 **MessageDisposition** 属性是邮件项目（包括会议取消、会议请求和会议响应等会议消息）的必需属性。  <br/> |
|**SendMeetingInvitationsOrCancellations** <br/> |描述更新日历项目后如何传达会议更新。 此属性是日历项目和日历项目出现次数的必需属性。  <br/> |
|**SuppressReadReceipts** <br/> |指示是否应该禁止显示已更新项目的已读回执。 如果文本值为 **true，** 则指示应禁止显示已读回执。 false **值表示** 将已读回执发送给发件人。 此特性是可选的。  <br/> 此属性是在 2013 SP1 Exchange Server引入的。  <br/> |
   
#### <a name="conflictresolution-attribute"></a>ConflictResolution 属性

|**值**|**说明**|
|:-----|:-----|
|NeverOverwrite  <br/> |如果存在冲突，则更新操作将失败并返回错误。  <br/> |
|AutoResolve  <br/> |更新操作会自动解决任何冲突。  <br/> |
|AlwaysOverwrite  <br/> |如果存在冲突，更新操作将覆盖信息。  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition 属性

|**值**|**说明**|
|:-----|:-----|
|SaveOnly  <br/> |项目已更新并保存回其当前文件夹。  <br/> |
|SendOnly  <br/> |更新并发送项目，但不保存任何副本。  <br/> |
|SendAndSaveCopy  <br/> |项目会更新，副本将保存在 [SavedItemFolderId](saveditemfolderid.md) 元素标识的文件夹中。  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a>SendMeetingInvitationsOrCancellations 属性

|**值**|**说明**|
|:-----|:-----|
|SendToNone  <br/> |日历项目已更新，但不向与会者发送更新。  <br/> |
|SendOnlyToAll  <br/> |日历项目已更新，会议更新将发送给所有与会者，但不保存在"已发送的项目"文件夹中。  <br/> |
|SendOnlyToChanged  <br/> |日历项目将更新，并且会议更新仅发送给受会议更改影响的与会者。  <br/> |
|SendToAllAndSaveCopy  <br/> |日历项目会更新，会议更新将发送给所有与会者，副本将保存在"已发送项目"文件夹中。  <br/> |
|SendToChangedAndSaveCopy  <br/> |日历项目会更新，会议更新将发送给受会议更改影响的所有与会者，并且副本将保存在"已发送的项目"文件夹中。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |标识用于更新、发送和创建邮件存储中项目的操作Exchange文件夹。  <br/> |
|[ItemChanges](itemchanges.md) <br/> |包含一个 [ItemChange](itemchange.md) 元素数组，用于标识项目以及要应用于项目的更新。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

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

