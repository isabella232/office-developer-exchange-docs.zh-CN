---
title: ContentLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentLocation
api_type:
- schema
ms.assetid: d91cf587-24e3-4c13-8784-5ca29787cca7
description: ContentLocation 元素包含对应于附件的内容的位置的统一资源标识符 (URI)。
ms.openlocfilehash: 060dab2da653637420d5900bad3b95823c2e6ea3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753566"
---
# <a name="contentlocation"></a>ContentLocation

**ContentLocation**元素包含对应于附件的内容的位置的统一资源标识符 (URI)。 
  
```xml
<ContentLocation/>
```

 **字符串**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |代表附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[FileAttachment](fileattachment.md) <br/> |代表附加到 Exchange 存储中的项的文件。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个 string 值，该值代表 URI。
  
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

