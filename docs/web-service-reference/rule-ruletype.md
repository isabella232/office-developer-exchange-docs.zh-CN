---
title: 规则 (RuleType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rule
api_type:
- schema
ms.assetid: 259a1f62-b235-4964-88bf-2d1f1c05a563
description: Rule 元素包含单一规则并代表用户的邮箱中的规则。
ms.openlocfilehash: b1f9f058213543633335db11f03729964baf98ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827259"
---
# <a name="rule-ruletype"></a>规则 (RuleType)

**Rule**元素包含单一规则并代表用户的邮箱中的规则。 
  
```XML
<Rule>
    <RuleId>
    <DisplayName>
    <Priority>
    <IsEnabled>
    <IsNotSupported>
    <IsInError>
    <Conditions>
    <Exceptions>
    <Actions>
</Rule>
```

 **RuleType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[规则 Id](ruleid.md) <br/> |指定规则标识符。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |包含规则的显示名称。  <br/> |
|[Priority](priority.md) <br/> |指示是用来运行规则的顺序。  <br/> |
|[IsEnabled](isenabled.md) <br/> |指示是否启用规则。  <br/> |
|[IsNotSupported](isnotsupported.md) <br/> |指示是否无法使用 Api 的托管代码修改该规则。  <br/> |
|[IsInError](isinerror.md) <br/> |指示规则是否处于错误状态。  <br/> |
|[条件](conditions.md) <br/> |标识条件，履行时, 将触发规则的规则操作。  <br/> |
|[异常](exceptions.md) <br/> |标识表示收件箱规则的所有可用规则例外条件的例外。  <br/> |
|[Actions](actions.md) <br/> |表示当满足条件时要采取的上一条消息的操作。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |代表要创建新的规则操作。  <br/> |
|[InboxRules](inboxrules.md) <br/> |代表规则在用户的邮箱中的数组。  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |代表要更新现有规则的操作。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateInboxRules](updateinboxrules.md)
  
[SetRuleOperation](setruleoperation.md)
  
[CreateRuleOperation](createruleoperation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

