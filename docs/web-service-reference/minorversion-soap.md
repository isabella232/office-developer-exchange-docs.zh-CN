---
title: MinorVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 2ef4e181-7324-4c88-94a9-1cffefc8c008
description: MinorVersion元素表示为服务器的版本号。
ms.openlocfilehash: 4518a1cb342187099aefa9ac9d9d5069e51fa9ca
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518195"
---
# <a name="minorversion-soap"></a>MinorVersion (SOAP)

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **MinorVersion** 元素表示为服务器的版本号。 
  
```XML
<MinorVersion/>
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
|[ServerVersionInfo (SOAP)](serverversioninfo-soap.md) <br/> |包含处理请求的服务器的版本。  <br/> |
   
## <a name="text-value"></a>文本值

一个整数值，表示服务器处理该请求的次要版本数。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

