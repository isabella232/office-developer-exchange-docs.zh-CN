---
title: MaximumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fb7c3ab3-ef97-44c7-83e0-93cfe8c48e84
description: MaximumSize 元素表示邮件必须达到的最大大小，以便条件或例外情况适用。
ms.openlocfilehash: cfc0e65674fc96e31f3daebe6a6c378309b1aa3f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522642"
---
# <a name="maximumsize"></a>MaximumSize

**MaximumSize** 元素表示邮件必须达到的最大大小，以便条件或例外情况适用。 
  
```XML
<Maximum/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[WithinSizeRange](withinsizerange.md) <br/> |指定传入邮件必须达到的最小和最大大小，以便条件或例外适用。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个整数，用于标识邮件的最大大小（以字节为单位）。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[MinimumSize](minimumsize.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

