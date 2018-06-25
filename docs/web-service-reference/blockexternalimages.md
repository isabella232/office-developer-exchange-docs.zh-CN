---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: BlockExternalImages 元素指定的 HTML 文本正文中是否阻止外部图像。
ms.openlocfilehash: 41ab2ec7ec1c24ccbbef037ef1e27431c1fe6811
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753330"
---
# <a name="blockexternalimages"></a>BlockExternalImages

**BlockExternalImages**元素指定的 HTML 文本正文中是否阻止外部图像。 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |标识要在 GetFolder、 FindFolder 或 SyncFolderHierarchy 响应中包含的文件夹属性。  <br/> |
|[ItemShape](itemshape.md) <br/> |标识项目属性和 GetItem、 FindItem 或 SyncFolderItems 响应中包括的内容。  <br/> |
   
## <a name="text-value"></a>文本值

文本值为**true** **BlockExternalImages**元素表示外部图像表单 HTML 正文中被阻止。 如果值为**false**指示允许外部图像。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

