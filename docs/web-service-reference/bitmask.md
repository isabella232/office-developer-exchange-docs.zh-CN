---
title: Bitmask
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bitmask
api_type:
- schema
ms.assetid: fc7eeac2-555f-4cbc-8b48-26d9ed67748a
description: Bitmask 元素表示要在 不包括 限制操作中使用的十六进制或十进制掩码。
ms.openlocfilehash: f05be466d05b13f8f362afb5fc0552653a532475
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458808"
---
# <a name="bitmask"></a>Bitmask

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Bitmask** 元素表示要在 [不包括](excludes.md) 限制操作中使用的十六进制或十进制掩码。 
  
```xml
<Bitmask Value="" />
```

**ExcludesValueType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**值** | 表示十进制或十六进制位掩码。 由以下正则表达式表示值：<br/>`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.<br/><br/>以下是此属性的十六进制值的示例：<br/>- 0x12AF<br/>- 0X334AE<br/><br/>以下是此属性的十进制值的示例：<br/>- 10<br/>- 255<br/>- 4562 |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[不包括](excludes.md) <br/> |执行这些属性的位掩码。  <br/> |
   
## <a name="remarks"></a>说明

十六进制值必须有 0x 或 0X 的前缀。如果不存在此前缀，则假定该值为十进制数。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

