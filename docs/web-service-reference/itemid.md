---
title: ItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemId
api_type:
- schema
ms.assetid: 3350b597-57a0-4961-8f44-8624946719b4
description: ItemId 元素包含在 Exchange 存储中的项目的唯一标识符和更改的键。
ms.openlocfilehash: 9c5d71a23e1e4b77d2a50016aa4d765d872d04cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826157"
---
# <a name="itemid"></a>ItemId

**ItemId**元素包含在 Exchange 存储中的项目的唯一标识符和更改的键。 
  
```XML
<ItemId Id="" ChangeKey="" />
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|
  **Id** <br/> |标识 Exchange 存储中的特定项目。 **Id**是区分大小写。因此， **Id**之间的比较必须区分大小写或二进制。  <br/> |
|**更改密钥** <br/> | 标识项目的特定版本。 <br/><br/>**更改密钥**时，需要以下方案： <br/> <br/>如果**ConflictResolution**属性设置为自动解析，- [UpdateItem](updateitem.md)元素将需要**更改密钥**。 自动解析为默认值。 如果不包括**更改密钥**属性，则响应将返回[ResponseCode](responsecode.md)值等于**ErrorChangeKeyRequired**。  <br/><br/>- [SendItem](senditem.md)元素需要**更改密钥**来测试是否尝试的操作将作用于项目的最新版本。 如果**更改密钥**属性不包括在**ItemId**或**更改密钥**为空，响应将返回[ResponseCode](responsecode.md)值等于**ErrorStaleObject**。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[日历项目](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[联系人](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示复制的项或文件夹时的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |表示在创建项目或文件夹时的事件。  <br/> |
|[删除 (ItemSync)](delete-itemsync.md) <br/> |标识要删除在本地客户端库中的单个项。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示删除项目或文件夹时的事件。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |包含状态和请求导出的单个邮箱项目的结果。  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |代表定期日历项目的第一个匹配项。  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |包含的项标识符的邮箱中的所有对话项的集合。  <br/> |
|[忽略](ignore.md) <br/> |标识同步过程中跳过的项目。  <br/> |
|[Item](item.md) <br/> |表示的泛型 Exchange 项目。  <br/> |
|[项目 (UploadItemType)](item-uploaditemtype.md) <br/> |代表单个项目上载到邮箱。  <br/> |
|[ItemChange](itemchange.md) <br/> |包含项标识符和更新应用到的项。  <br/><br/> 以下是此元素的 XPath 表达式： <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | 包含唯一标识的项目、 匹配项和删除、 发送、 获取、 移动或在 Exchange 存储中复制项所用于的定期主项目。 <br/> <br/>  下面是此元素的 XPath 表达式： <br/> <br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
|[ItemIds (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md) <br/> |包含确定要导出邮箱中的项的项标识符的数组。  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |代表定期日历项目的最后一个实例。  <br/> |
|[Mailbox](mailbox.md) <br/> |标识已启用邮件的Active Directory目录服务对象。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示修改项目时发生的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示项目从一个父文件夹移动到另一个父文件夹时发生的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |表示由邮箱中的一个新的邮件项目触发的事件。  <br/> |
|[匹配项](occurrence.md) <br/> |代表定期日历项目的一个已修改匹配项。  <br/> |
|[PlayOnPhone （Exchange Web 服务）](playonphone-exchange-web-services.md) <br/> |表示读取电话上的项的请求。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[RoomList](roomlist.md) <br/> |表示标识的会议室列表的电子邮件地址。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |包含状态和请求上载单个邮箱项目的结果。  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |定义单个用户配置对象。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ExportItems 操作](exportitems-operation.md)
- [UploadItems 操作](uploaditems-operation.md) 
- [FindConversation Operation](findconversation-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

