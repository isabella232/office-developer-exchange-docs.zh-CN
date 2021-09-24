---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: UniqueBodyType 元素指定以文本格式还是 HTML 格式返回唯一正文。
ms.openlocfilehash: a0149e41da24646fdf38a465434bfad3557ece22
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520267"
---
# <a name="uniquebodytype"></a>UniqueBodyType

**UniqueBodyType** 元素指定以文本格式还是 HTML 格式返回唯一正文。 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 **BodyTypeResponseType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[ItemShape](itemshape.md)
  
## <a name="text-value"></a>文本值

**UniqueBodyType** 元素的文本值指示返回唯一正文的格式。 下表列出了此元素的可能值。 
  
****

|**值**|**说明**|
|:-----|:-----|
|最好  <br/> |该响应将返回最丰富的正文文本可用内容。 如果内容是文本还是 HTML，这很有用。  <br/> 如果存储的正文是纯文本，则返回的正文将是文本。 否则，如果存储的正文采用 HTML 或 RTF 格式，响应将返回 HTML。  <br/> 此值为默认值。  <br/> |
|HTML  <br/> |该响应将返回 HTML 格式的唯一正文。  <br/> |
|文本  <br/> |响应将返回纯文本格式的唯一正文。  <br/> |
   
## <a name="remarks"></a>说明

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[ItemShape](itemshape.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

