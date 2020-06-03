---
title: RemoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: RemoveItem 元素表示一个 response 对象，该对象用于在收到 MeetingCancellation 邮件时删除会议项目。
ms.openlocfilehash: c0cd5c1f9894287ee78c2f7a65b8f4d3b943414e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467688"
---
# <a name="removeitem"></a>RemoveItem

**RemoveItem**元素表示一个 response 对象，该对象用于在收到 MeetingCancellation 邮件时删除会议项目。 
  
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
|**ObjectName** <br/> |将 RemoveItem reply 对象类的名称表示为英文字符串。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |标识 RemoveItem 响应对象引用的项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[项目（NonEmptyArrayOfAllItemsType）](items-nonemptyarrayofallitemstype.md) <br/> |包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |包含与 Exchange 存储中的项目关联的所有响应对象的集合。  <br/> |
   
## <a name="remarks"></a>备注

 **RemoveItem**仅对[MeetingCancellation](meetingcancellation.md)有效。 否则，将引发错误。
  
> [!NOTE]
> 会议取消的[ItemClass](itemclass.md)为 IPM。日程安排. 会议. 已取消。 
  
若要删除[MeetingRequest](meetingrequest.md)和关联的[CalendarItem](calendaritem.md)，请使用[DeclineItem](declineitem.md) Response 对象，而不是**RemoveItem**。
  
 代理访问不支持**RemoveItem** 。 
  
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

