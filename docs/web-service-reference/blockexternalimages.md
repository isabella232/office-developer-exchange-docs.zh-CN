---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: BlockExternalImages 元素指定是否在 HTML 文本正文中阻止外部图像。
ms.openlocfilehash: 73342316024ebe476a0e35f14157befc80edcf83
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527402"
---
# <a name="blockexternalimages"></a>BlockExternalImages

**BlockExternalImages**元素指定是否在 HTML 文本正文中阻止外部图像。 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |标识要包括在 GetFolder、FindFolder 或 SyncFolderHierarchy 响应中的文件夹属性。  <br/> |
|[ItemShape](itemshape.md) <br/> |标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。  <br/> |
   
## <a name="text-value"></a>文本值

**BlockExternalImages**元素的文本值为**true**表示外部图像在 HTML 正文中被阻止。 **如果值为 false** ，则表示允许外部图像。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |类型 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

