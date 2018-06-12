---
title: 转换
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
description: 转换元素均表示所在的时区转换。
ms.openlocfilehash: 5dcd2f0dae7c3df2dcf660d6fe1a41b216c67b59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838287"
---
# <a name="transition"></a>转换

**转换**元素均表示所在的时区转换。 
  
```xml
<Transition>
   <To/>
</Transition>
```

 **TransitionType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[To](to.md) <br/> |指定[时段](period.md)或[TransitionsGroup](transitionsgroup.md)所在的时区转换的目标。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[切换](transitions.md) <br/> |表示所在的时区转换的集合。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

