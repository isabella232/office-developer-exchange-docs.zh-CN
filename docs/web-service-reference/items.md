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
description: 项目元素包含数组的项目。
ms.openlocfilehash: 241a56ee23e87d6a4320b93cc65b1f5aa1f60120
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826163"
---
# <a name="items"></a>项目

**项目**元素包含数组的项目。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Item](item.md) <br/> |表示 Exchange 存储中的项。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[日历项目](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[联系人](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |代表 Exchange 存储中的会议消息。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[PostItem](postitem.md) <br/> |代表一个 Exchange 存储中的公告项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |包含状态和[CopyItem 操作](copyitem-operation.md)请求的结果。  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |包含状态和的单个结果[CreateItem operation，](createitem-operation.md)请求。  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |包含状态和[GetItem operation，](getitem-operation.md)请求的结果。  <br/> |
|[GroupedItems](groupeditems.md) <br/> |调用表示项的组合[FindItem 操作](finditem-operation.md)的结果的集合。  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |包含状态和[MoveItem 操作](moveitem-operation.md)请求的结果。  <br/> |
|[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md) <br/> |[FindItem 操作](finditem-operation.md)过程中包含单个根文件夹的搜索的结果。  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |包含状态和[UpdateItem 操作](updateitem-operation.md)请求的结果。  <br/> |
   
## <a name="remarks"></a>备注

有关组[CreateItem operation，](createitem-operation.md)请求中的项的信息，请参阅[项目 (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md)。
  
[消息](message-ex15websvcsotherref.md)元素表示电子邮件和非 Exchange Web Services (EWS) 架构的强类型的所有其他项目。 如 IPM 的项目。共享和**消息**元素以返回 IPM.InfoPath。 启动 Exchange Server 2010 与 Exchange 版本不在响应中返回基本的[Item](item.md)元素。 
  
描述此元素的架构位于运行 Exchange 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[Exchange 的 EWS 引用](ews-reference-for-exchange.md)
  
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

