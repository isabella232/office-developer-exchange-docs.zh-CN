---
title: RemoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: RemoveItem 元素表示响应对象，该对象用于接收 MeetingCancellation 消息时删除会议项目。
ms.openlocfilehash: 4dbe9ede36bf6e3c008a2186cfe617519ecfae1f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517957"
---
# <a name="removeitem"></a>RemoveItem

**RemoveItem** 元素表示响应对象，该对象用于接收 MeetingCancellation 消息时删除会议项目。 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 **RemoveItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ObjectName** <br/> |以英语字符串形式表示 RemoveItem 答复对象类的名称。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |标识 RemoveItem 响应对象引用的项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |包含在由 [TargetFolderIdType 元素的 ParentFolderId ](parentfolderid-targetfolderidtype.md) (标识的文件夹中) 数组。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与项目存储中的项目关联的所有响应Exchange的集合。  <br/> |
   
## <a name="remarks"></a>注解

 **RemoveItem** 仅对 [MeetingCancellation 有效](meetingcancellation.md)。 否则，将引发错误。
  
> [!NOTE]
> 会议 [取消的 ItemClass](itemclass.md) 为 IPM。Schedule.Meeting.Canceled。 
  
若要删除 [MeetingRequest](meetingrequest.md) 和关联的 [CalendarItem](calendaritem.md)，请使用 [DeclineItem](declineitem.md) 响应对象，而不是 **RemoveItem**。
  
 **委派访问不支持 RemoveItem。** 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

