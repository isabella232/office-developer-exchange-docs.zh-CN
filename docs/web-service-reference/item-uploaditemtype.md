---
title: Item (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: Item 元素表示要上载到邮箱中的单个项目。
ms.openlocfilehash: bd4681a19df2018db9e54ee39095cd602662650a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514443"
---
# <a name="item-uploaditemtype"></a>Item (UploadItemType)

**Item** 元素表示要上载到邮箱中的单个项目。 
  
[UploadItems](uploaditems.md)
  
[Items (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
[Item (UploadItemType)](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 **UploadItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**CreateAction** <br/> |指定将项目上载到邮箱的操作。 此特性是必需的。  <br/> |
|**IsAssociated** <br/> |指定上载的项目是否是文件夹关联的项目。 此属性是一个布尔值。 true **值表示** 项目是文件夹关联的项目。 此特性是可选的。  <br/> |
   
#### <a name="createaction-attribute"></a>CreateAction 属性

|**值**|**说明**|
|:-----|:-----|
|**CreateNew** <br/> |指示原始项目的新副本已上载到邮箱。 如果使用 CreateNew 值，则 [ItemId](itemid.md) 元素不能存在。 在响应中返回新的项标识符。  <br/> |
|**更新** <br/> |指定将更新 **ItemId** 元素指示的项。 如果 **ItemId** 元素不存在或项目不存在于 [ParentFolderId](parentfolderid.md) 元素标识的文件夹中，则返回错误。  <br/> |
|**UpdateOrCreate** <br/> |指示首先尝试更新项目。 如果项目不存在于 **ParentFolderId** 元素指定的文件夹中，将创建一个新项。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ParentFolderId](parentfolderid.md) <br/> |表示创建新项或包含要更新的项的父文件夹的标识符。  <br/> |
|[ItemId](itemid.md) <br/> |包含要创建或更新的项的唯一标识符和更改Exchange项。  <br/> |
|[Data (base64Binary)](data-base64binary.md) <br/> |包含要上载到邮箱中的单个项目的数据。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Items (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md) <br/> |包含要上载到邮箱中的项目的数组。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ExportItems 操作](exportitems-operation.md)
  
[UploadItems 操作](uploaditems-operation.md)

