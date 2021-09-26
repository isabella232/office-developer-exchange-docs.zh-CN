---
title: 优先级
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Priority
api_type:
- schema
ms.assetid: e1adb8b9-e3d5-469a-b188-822733d2503e
description: Priority 元素指示规则运行的顺序。
ms.openlocfilehash: 6dc31de851d193deea1f47d07590ce21a90fc020
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543000"
---
# <a name="priority"></a>优先级

**Priority** 元素指示规则运行的顺序。 
  
```XML
<Priority/>
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
|[规则 (RuleType)](rule-ruletype.md) <br/> |表示用户的邮箱中的规则。  <br/> |
   
## <a name="text-value"></a>文本值

**Priority** 元素的文本值是一个整数，指示规则的运行顺序。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

