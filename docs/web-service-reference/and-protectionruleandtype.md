---
title: 和 (ProtectionRuleAndType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 7fafd1c8-cd29-43a0-b383-f6595f934f48
description: And 元素指定所有子元素必须都匹配来计算结果为 true。
ms.openlocfilehash: 9e0128ee3fa2b6ffdc5975946694475afec53c25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753147"
---
# <a name="and-protectionruleandtype"></a>和 (ProtectionRuleAndType)

**和**元素指定的所有子元素必须都匹配计算结果为**true**。
  
```xml
<And>
   <AllInternal/>
   <And/>
   <RecipientIs/>
   <SenderDepartments/>
   <True/>
</And>
```

 **ProtectionRuleAndType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AllInternal](allinternal.md) <br/> |如果所有收件人的电子邮件的发件人的组织内部的计算结果为**true** 。  <br/> |
|**And** <br/> |指定所有子元素都必须匹配以使值为 **true**。  <br/> |
|[RecipientIs](recipientis.md) <br/> |指定任何收件人的电子邮件匹配的任何子[值 (ProtectionRuleValueType)](value-protectionrulevaluetype.md)元素中指定的收件人。  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |指定发件人的部门匹配任何子[值 (ProtectionRuleValueType)](value-protectionrulevaluetype.md)元素中指定的部门。  <br/> |
|[True](true.md) <br/> |指定始终匹配条件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[条件](condition.md) <br/> |确定要执行该规则的操作部分必须满足的条件。  <br/> |
|**And** <br/> |指定所有子元素都必须匹配以使值为 **true**。  <br/> |
   
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
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

