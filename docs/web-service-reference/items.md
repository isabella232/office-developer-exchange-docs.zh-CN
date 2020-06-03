---
title: 项目
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: 0811a73e-bf1f-4889-9219-73902dd47639
description: Items 元素包含项的数组。
ms.openlocfilehash: 489e34ad0e4bcc2520febb3c213db970fa496051
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458129"
---
# <a name="items"></a>项目

**Items**元素包含项的数组。 
  
```xml
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <PostItem/>
</Items>
```

 **ArrayOfRealItemsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[项目](item.md) <br/> |表示 Exchange 存储中的项。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议邮件。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[PostItem](postitem.md) <br/> |表示 Exchange 存储中的公告项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |包含[CopyItem 操作](copyitem-operation.md)请求的状态和结果。  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |包含单个[CreateItem 操作](createitem-operation.md)请求的状态和结果。  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |包含[GetItem 操作](getitem-operation.md)请求的状态和结果。  <br/> |
|[GroupedItems](groupeditems.md) <br/> |表示作为分组[FindItem 操作](finditem-operation.md)调用的结果的项的集合。  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |包含[MoveItem 操作](moveitem-operation.md)请求的状态和结果。  <br/> |
|[RootFolder （FindItemResponseMessage）](rootfolder-finditemresponsemessage.md) <br/> |包含在[FindItem 操作](finditem-operation.md)过程中搜索单个根文件夹的结果。  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |包含[UpdateItem 操作](updateitem-operation.md)请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>备注

有关[CreateItem 操作](createitem-operation.md)请求中的项目集的信息，请参阅[items （NonEmptyArrayOfAllItemsType）](items-nonemptyarrayofallitemstype.md)。
  
[Message](message-ex15websvcsotherref.md)元素表示电子邮件以及 Exchange Web 服务（EWS）架构未强类型化的所有其他项目。 项目，如 IPM。共享和 IPM. InfoPath 以**邮件**元素的形式返回。 从 Exchange Server 2010 开始的 Exchange 版本不会在响应中返回基本[项目](item.md)元素。 
  
描述此元素的架构位于运行 Exchange 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange 的 EWS 引用](ews-reference-for-exchange.md)
  
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

