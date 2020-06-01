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
description: Rule 元素包含一个规则并表示用户邮箱中的规则。
ms.openlocfilehash: cdbd21df235a62a9e201e1eaae1d82a8ac10cdd2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465077"
---
# <a name="rule-ruletype"></a>规则 (RuleType)

**Rule**元素包含一个规则并表示用户邮箱中的规则。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[RuleId](ruleid.md) <br/> |指定规则标识符。  <br/> |
|[显示名称 (字符串)](displayname-string.md) <br/> |包含规则的显示名称。  <br/> |
|[Priority](priority.md) <br/> |指示规则的运行顺序。  <br/> |
|[IsEnabled](isenabled.md) <br/> |指示是否已启用该规则。  <br/> |
|[IsNotSupported](isnotsupported.md) <br/> |指示是否不能使用托管代码 Api 修改规则。  <br/> |
|[IsInError](isinerror.md) <br/> |指示规则是否处于错误状态。  <br/> |
|[条件](conditions.md) <br/> |标识在满足时将触发规则的规则操作的条件。  <br/> |
|[异常](exceptions.md) <br/> |标识代表收件箱规则的所有可用的规则例外条件的例外。  <br/> |
|[Actions](actions.md) <br/> |表示在满足条件时对邮件执行的操作。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |表示一个用于创建新规则的操作。  <br/> |
|[InboxRules](inboxrules.md) <br/> |表示用户邮箱中的一组规则。  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |表示用于更新现有规则的操作。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateInboxRules](updateinboxrules.md)
  
[SetRuleOperation](setruleoperation.md)
  
[CreateRuleOperation](createruleoperation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

