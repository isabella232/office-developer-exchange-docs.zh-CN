---
title: MovedItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: MovedItemId 元素指定 MarkAsJunk 操作移动的项目的标识符。
ms.openlocfilehash: 0775aaed119242fc2a2057fb20807d5be30692e5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509593"
---
# <a name="moveditemid"></a>MovedItemId

**MovedItemId** 元素指定 **MarkAsJunk** 操作移动的项目的标识符。 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |**Id** 属性的值是由 **MarkAsJunk** 操作移动的项目的项目标识符。 项目标识符在移动后保持不变。  <br/> |
|ChangeKey  <br/> |**ChangeKey** 属性的值为已移动项目的更改键。 更改键在 **MarkAsJunk** 操作移动项目后更改。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> ||
   

