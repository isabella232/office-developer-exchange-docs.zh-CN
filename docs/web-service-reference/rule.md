---
title: Rule
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Rule
api_type:
- schema
ms.assetid: c30f3851-bd56-4473-9106-dc85e9619486
description: Rule 元素包含单个保护规则。
ms.openlocfilehash: 45fb13ae6e1aacb78e7e8520f8678097796e339f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517873"
---
# <a name="rule"></a>Rule

**Rule** 元素包含单个保护规则。 
  
```XML
<Rule Name="" UserOverridable=="" Priority="">
   <Condition/>
   <Action/>
</Rule>
```

 **ProtectionRuleType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**名称** <br/> |标识规则的名称。 字符串类型的必需属性，最小长度为 1。  <br/> |
|**UserOverridable** <br/> |指定规则是否是必需的。 如果该规则是必需的，则此属性值必须为 **false**。 Boolean 类型的必需属性。  <br/> |
|**优先级** <br/> |指定规则优先级。 int 类型的必需属性，最小值为 1。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[条件](condition.md) <br/> |确定要执行该规则的操作部分必须满足的条件。  <br/> |
|[Action (ProtectionRuleActionType)](action-protectionruleactiontype.md) <br/> |标识在规则的条件部分匹配时必须执行的操作。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[规则 ](rules-ex15websvcsotherref.md) <br/> |包含一组保护规则。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

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

