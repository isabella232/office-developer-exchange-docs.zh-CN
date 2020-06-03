---
title: ItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- ItemId
api_type:
- schema
ms.assetid: 3350b597-57a0-4961-8f44-8624946719b4
description: ItemId 元素包含 Exchange 存储中项的唯一标识符和更改键。
localization_priority: Priority
ms.openlocfilehash: d5931702225c6864b1ca60a6f0753b65f65aca30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44441560"
---
# <a name="itemid"></a>ItemId

**ItemId**元素包含 Exchange 存储中项的唯一标识符和更改键。 
  
```XML
<ItemId Id="" ChangeKey="" />
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |标识 Exchange 存储中的特定项目。 **Id**区分大小写;因此， **id**之间的比较必须区分大小写或二进制。  <br/> |
|**ChangeKey** <br/> | 标识项目的特定版本。 <br/><br/>在以下情况下， **ChangeKey**是必需的： <br/> <br/>-如果**ConflictResolution**属性设置为 "自动解析"，则[UpdateItem](updateitem.md)元素需要**ChangeKey** 。 "自动解析" 是默认值。 如果不包含**ChangeKey**属性，则响应将返回一个等于**ErrorChangeKeyRequired**的[ResponseCode](responsecode.md)值。  <br/><br/>- [SendItem](senditem.md)元素需要**ChangeKey**以测试尝试的操作是否将对项目的最新版本进行操作。 如果**ChangeKey**属性未包含在**ItemId**中，或者如果**ChangeKey**为空，响应将返回一个等于**ErrorStaleObject**的[ResponseCode](responsecode.md)值。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |代表复制项目或文件夹时的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |表示创建项或文件夹时的事件。  <br/> |
|[Delete （ItemSync）](delete-itemsync.md) <br/> |标识要在本地客户端存储中删除的单个项。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示在删除项或文件夹时的事件。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |包含导出单个邮箱项目的请求的状态和结果。  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |表示定期日历项目的第一个匹配项。  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |包含邮箱中所有会话项目的项标识符的集合。  <br/> |
|[忽略](ignore.md) <br/> |确定在同步过程中要跳过的项。  <br/> |
|[项](item.md) <br/> |表示通用 Exchange 项。  <br/> |
|[Item （UploadItemType）](item-uploaditemtype.md) <br/> |代表要上传到邮箱中的单个项目。  <br/> |
|[ItemChange](itemchange.md) <br/> |包含项目标识符和要应用于项目的更新。  <br/><br/> 下面是此元素的 XPath 表达式：  <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | 包含项目、具体值项目和定期主项目的唯一标识，用于删除、发送、获取、移动或复制 Exchange 存储中的项目。 <br/> <br/>  下面是此元素的 XPath 表达式： <br/> <br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
|[ItemIds (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md) <br/> |包含项标识符的数组，这些标识符标识要从邮箱中导出的项。  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |表示定期日历项目的最后一个事件。  <br/> |
|[Mailbox](mailbox.md) <br/> |标识已启用邮件的Active Directory目录服务对象。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |代表修改项目时发生的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示在将项目从一个父文件夹移动到另一个父文件夹时发生的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |代表由邮箱中的新邮件项目触发的事件。  <br/> |
|[重复](occurrence.md) <br/> |代表定期日历项目的单个修改事件。  <br/> |
|[PlayOnPhone （Exchange Web 服务）](playonphone-exchange-web-services.md) <br/> |表示在电话上读取项目的请求。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[RoomList](roomlist.md) <br/> |代表标识会议室列表的电子邮件地址。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |包含上载单个邮箱项目的请求的状态和结果。  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |定义单个用户配置对象。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ExportItems 操作](exportitems-operation.md)
- [UploadItems 操作](uploaditems-operation.md) 
- [FindConversation 操作](findconversation-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

