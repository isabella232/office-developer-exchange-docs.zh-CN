---
title: NormalizedBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c6973aee-ec7b-44c1-b328-f2204d9de5d1
description: NormalizedBodyType 元素指定是否以文本或 HTML 格式返回规范化的正文。
ms.openlocfilehash: 33575594b22f972a9eb762dfac884fa91459f04a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826554"
---
# <a name="normalizedbodytype"></a>NormalizedBodyType

**NormalizedBodyType**元素指定是否以文本或 HTML 格式返回规范化的正文。 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
```

 **BodyTypeResponseType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[ItemShape](itemshape.md)
  
## <a name="text-value"></a>文本值

**NormalizedBodyType**元素的文本值指示规范化的正文格式返回中。 下表列出了此元素的可能值。 
  
****

|**值**|**说明**|
|:-----|:-----|
|最佳  <br/> |响应将返回正文文本的丰富的可用内容。 这很有用，如果不知道的内容是否是文本或 HTML。  <br/> 返回的正文将文本，如果存储的正文采用纯文本。 否则，如果存储的正文采用 HTML 或 RTF 格式响应将返回 HTML。  <br/> 这是默认值。  <br/> |
|HTML  <br/> |响应将以 HTML 形式返回规范化的正文。  <br/> |
|Text  <br/> |响应将以纯文本形式返回规范化的正文。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[ItemShape](itemshape.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

