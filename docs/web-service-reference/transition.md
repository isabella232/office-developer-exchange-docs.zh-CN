---
title: 移交
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transition
api_type:
- schema
ms.assetid: 23ce171a-a9c9-47ed-a366-822777048eea
description: 转换元素表示时区转换。
ms.openlocfilehash: 05495eb4a493feedc88532cc4bc8b949493481f5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467492"
---
# <a name="transition"></a>移交

**转换**元素表示时区转换。 
  
```xml
<Transition>
   <To/>
</Transition>
```

 **TransitionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[To](to.md) <br/> |指定作为时区转换目标的[时间段](period.md)或[TransitionsGroup](transitionsgroup.md) 。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[移交](transitions.md) <br/> |表示时区转换的集合。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

