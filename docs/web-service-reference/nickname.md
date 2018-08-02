---
title: Nickname
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Nickname
api_type:
- schema
ms.assetid: 3d35b207-d28c-4f3f-8b00-55339d30d19a
description: Nickname 元素表示联系人昵称。
ms.openlocfilehash: 0328ea80725f81dce81e5a7730046e3978ae6df1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826533"
---
# <a name="nickname"></a>Nickname

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Nickname** 元素表示联系人昵称。 
  
```xml
<Nickname/>
```

**string**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CompleteName](completename.md) <br/> |表示某个联系人的完整名称。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
   
## <a name="text-value"></a>文本值

**Nickname** 元素采用字符串值。、 
  
## <a name="remarks"></a>说明

此元素为可选。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [创建联系人（Exchange Web 服务）](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

