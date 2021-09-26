---
title: ConvertHtmlCodePageToUTF8
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f02c8331-0a4e-4d01-adc2-2b93ed838a42
description: ConvertHtmlCodePageToUTF8 元素指示项目 HTML 正文是否转换为 UTF8。
ms.openlocfilehash: e43de22b6d8050c14eb18d0fdd5a72f463335189
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545571"
---
# <a name="converthtmlcodepagetoutf8"></a>ConvertHtmlCodePageToUTF8

**ConvertHtmlCodePageToUTF8** 元素指示项目 HTML 正文是否转换为 UTF8。 
  
```XML
<ConvertHtmlCodePageToUTF8/>
```

 **xs：boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |标识在响应中返回的一组属性。  <br/> |
   
## <a name="text-value"></a>文本值

**ConvertHtmlCodePageToUTF8** 元素的文本值 **true** 指示 HTML 正文已转换为 UTF8。 文本值为 **false** 表示 HTML 正文未转换为 UTF8。 
  
## <a name="remarks"></a>注解

如果请求中未指定 **ConvertHtmlCodePageToUTF8** 元素，则使用 **默认值 true。** 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

