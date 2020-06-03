---
title: Action （ProtectionRuleActionType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: ca090dec-e2c5-49c8-a057-8d1f2409147f
description: Action 元素标识当规则的条件部分匹配时，必须执行的操作。
ms.openlocfilehash: 220a6fea16abb9ea823ae6239537b8c121702589
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527507"
---
# <a name="action-protectionruleactiontype"></a>Action （ProtectionRuleActionType）

**Action**元素标识当规则的条件部分匹配时，必须执行的操作。 
  
```xml
<Action Name="">
   <Argument/>
</Action>

```

 **ProtectionRuleActionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**名称** <br/> |标识操作的名称。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[参数](argument.md) <br/> |指定操作的参数。 如果指定的操作不需要指定参数，则不会出现此元素。 如果操作需要一个或多个参数，则此元素可能出现一次或多次。 **RightsProtectMessage**操作将包含单个参数。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Rule](rule.md) <br/> |包含一个保护规则。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

