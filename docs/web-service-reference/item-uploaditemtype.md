---
title: Item （UploadItemType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: Item 元素代表要上传到邮箱中的单个项目。
ms.openlocfilehash: 82c0fdf89c06ddfb812c2b2f1899b589eedeb7d8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467548"
---
# <a name="item-uploaditemtype"></a>Item （UploadItemType）

**Item**元素代表要上传到邮箱中的单个项目。 
  
[UploadItems](uploaditems.md)
  
[项目（NonEmptyArrayOfUploadItemsType）](items-nonemptyarrayofuploaditemstype.md)
  
[Item （UploadItemType）](item-uploaditemtype.md)
  
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
|**CreateAction** <br/> |指定用于将项目上载到邮箱的操作。 此特性是必需的。  <br/> |
|**IsAssociated** <br/> |指定上传的项目是否是与文件夹相关联的项目。 此属性是一个布尔值。 **如果值为 true** ，则表示该项目是一个与文件夹相关联的项目。 此特性是可选的。  <br/> |
   
#### <a name="createaction-attribute"></a>CreateAction 属性

|**值**|**说明**|
|:-----|:-----|
|**CreateNew** <br/> |指示将原始项目的新副本上载到邮箱。 如果使用了 CreateNew 值，则必须不存在[ItemId](itemid.md)元素。 在响应中返回新的项目标识符。  <br/> |
|**更新** <br/> |指定由**ItemId**元素指示的项目将更新。 如果**ItemId**元素不存在或项目不存在于由[ParentFolderId](parentfolderid.md)元素标识的文件夹中，则会返回错误。  <br/> |
|**UpdateOrCreate** <br/> |指示第一次尝试更新项目。 如果**ParentFolderId**元素指定的文件夹中不存在该项目，则会创建一个新项目。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[ParentFolderId](parentfolderid.md) <br/> |表示在其中创建新项目或包含要更新的项目的父文件夹的标识符。  <br/> |
|[ItemId](itemid.md) <br/> |包含要在 Exchange 存储中创建或更新的项目的唯一标识符和更改密钥。  <br/> |
|[Data （base64Binary）](data-base64binary.md) <br/> |包含要上传到邮箱中的单个项目的数据。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[项目（NonEmptyArrayOfUploadItemsType）](items-nonemptyarrayofuploaditemstype.md) <br/> |包含要上载到邮箱的项的数组。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

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

