---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: MinimumSize 元素表示要应用的条件或例外的邮件必须满足的最小大小。
ms.openlocfilehash: b43a8b5916747c4e3e4ca9b66cf8b9d73f5f8942
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44464201"
---
# <a name="minimumsize"></a>MinimumSize

**MinimumSize**元素表示要应用的条件或例外的邮件必须满足的最小大小。 
  
```XML
<MinimumSize/>
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
|[WithinSizeRange](withinsizerange.md) <br/> |指定传入邮件必须满足的最小和最大大小，以便条件或例外情况适用。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值是一个整数，用于标识邮件的最小大小（以字节为单位）。
  
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



[MaximumSize](maximumsize.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

