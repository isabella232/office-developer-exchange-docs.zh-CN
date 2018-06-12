---
title: 大化
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fb7c3ab3-ef97-44c7-83e0-93cfe8c48e84
description: 大化元素均表示的条件或例外的顺序应用必须一条消息的最大大小。
ms.openlocfilehash: 37e3d377b105534fe34b54e262bd47bc450706da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826387"
---
# <a name="maximumsize"></a>大化

**大化**元素均表示的条件或例外的顺序应用必须一条消息的最大大小。 
  
```XML
<Maximum/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[WithinSizeRange](withinsizerange.md) <br/> |指定的条件或例外的顺序应用必须传入消息的最小和最大大小。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个整数，标识邮件以字节为单位的最大大小。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[MinimumSize](minimumsize.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

