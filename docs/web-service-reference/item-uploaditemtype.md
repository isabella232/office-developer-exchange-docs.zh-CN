---
title: 项目 (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: Item 元素表示单个项目上载到邮箱。
ms.openlocfilehash: 8fecef9a2368a44e38633eb9fddaa8197620f6a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826138"
---
# <a name="item-uploaditemtype"></a>项目 (UploadItemType)

**Item**元素表示单个项目上载到邮箱。 
  
[UploadItems](uploaditems.md)
  
[项目 (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md)
  
[项目 (UploadItemType)](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 **UploadItemType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**CreateAction** <br/> |指定用于将项目上载到邮箱的操作。 此属性是必需的。  <br/> |
|**IsAssociated** <br/> |指定是否已上载的项目是关联文件夹项。 此属性是一个布尔值。 值为**true**指示项关联的项目的文件夹。 此属性是可选的。  <br/> |
   
#### <a name="createaction-attribute"></a>创建动作属性

|**值**|**说明**|
|:-----|:-----|
|**CreateNew** <br/> |指示原始项目的新副本上载到邮箱。 [ItemId](itemid.md)元素必须存在，如果使用了 CreateNew 值。 在响应中返回新的项标识符。  <br/> |
|**更新** <br/> |指定将由**ItemId**元素指示的项进行了更新。 如果不存在**ItemId**元素或项目中由[ParentFolderId](parentfolderid.md)元素标识的文件夹不存在，则返回错误。  <br/> |
|**UpdateOrCreate** <br/> |指示尝试首先进行更新此项目。 如果项目不存在**ParentFolderId**元素所指定的文件夹中，将创建一个新项。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ParentFolderId](parentfolderid.md) <br/> |表示在其中创建新项目或包含要更新的项的父文件夹的标识符。  <br/> |
|[ItemId](itemid.md) <br/> |包含要创建或更新 Exchange 存储中的项的唯一标识符和更改键。  <br/> |
|[数据 (base64Binary)](data-base64binary.md) <br/> |包含要上载到邮箱的单个项的数据。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[项目 (NonEmptyArrayOfUploadItemsType)](items-nonemptyarrayofuploaditemstype.md) <br/> |包含项目上载到邮箱的数组。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ExportItems 操作](exportitems-operation.md)
  
[UploadItems 操作](uploaditems-operation.md)

