---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: UniqueBodyType 元素指定是否以文本或 HTML 格式返回唯一正文。
ms.openlocfilehash: 7e6c4631ef589555ce4d5da747c200ffe956f3a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459438"
---
# <a name="uniquebodytype"></a>UniqueBodyType

**UniqueBodyType**元素指定是否以文本或 HTML 格式返回唯一正文。 
  
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

**UniqueBodyType**元素的文本值指示中返回的唯一正文的格式。 下表列出了此元素的可能值。 
  
****

|**值**|**说明**|
|:-----|:-----|
|最好  <br/> |响应将返回正文文本的最丰富的可用内容。 如果不知道内容是文本还是 HTML，这将非常有用。  <br/> 如果存储的正文为纯文本，则返回的正文将为文本。 否则，如果存储的正文是 HTML 格式或 RTF 格式，则响应将返回 HTML。  <br/> 此值为默认值。  <br/> |
|HTML  <br/> |响应将以 HTML 形式返回唯一正文。  <br/> |
|文本  <br/> |响应将以纯文本形式返回唯一正文。  <br/> |
   
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

