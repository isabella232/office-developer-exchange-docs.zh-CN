---
title: ExportItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItems
api_type:
- schema
ms.assetid: bbbc56e4-8cc1-43ae-b70a-9a8d6bb0f399
description: ExportItems 元素表示从邮箱导出项目的请求。
ms.openlocfilehash: 6e4996f62ea5051e6dc235ee7255057f16b3855b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457268"
---
# <a name="exportitems"></a>ExportItems

**ExportItems**元素表示从邮箱导出项目的请求。 
  
[ExportItems](exportitems.md)
  
```XML
<ExportItems>
   <ItemIds/>
</ExportItems>
```

 **ExportItemsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemIds (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md) <br/> |包含项标识符的数组，这些标识符标识要从邮箱中导出的项。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ExportItems 操作](exportitems-operation.md)
  
[UploadItems 操作](uploaditems-operation.md)

