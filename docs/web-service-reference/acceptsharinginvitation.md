---
title: AcceptSharingInvitation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AcceptSharingInvitation
api_type:
- schema
ms.assetid: 3c2a47d6-490d-425b-8893-089a4f8882cd
description: AcceptSharingInvitation 元素用于接受允许访问其他用户的日历或联系人数据的邀请。
ms.openlocfilehash: 76b7bedccb4135a51104bea99d3844f384870db0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525433"
---
# <a name="acceptsharinginvitation"></a>AcceptSharingInvitation

**AcceptSharingInvitation** 元素用于接受允许访问其他用户的日历或联系人数据的邀请。 
  
```xml
<AcceptSharingInvitation>
   <ReferenceItemId/>
</AcceptSharingInvitation>
```

 **AcceptSharingInvitationType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |标识响应对象引用的项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseObjects](responseobjects.md) <br/> |包含与项目存储中的项目关联的所有响应Exchange的集合。  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |包含在由 [TargetFolderIdType 元素的 ParentFolderId ](parentfolderid-targetfolderidtype.md) (文件夹中) 数组。  <br/> |
   
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

- [CreateItem (AcceptSharingInvitation)](createitem-acceptsharinginvitation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

