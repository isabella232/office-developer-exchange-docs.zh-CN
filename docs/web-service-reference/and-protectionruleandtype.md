---
title: And (ProtectionRuleAndType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- And
api_type:
- schema
ms.assetid: 7fafd1c8-cd29-43a0-b383-f6595f934f48
description: And 元素指定所有子元素都必须匹配，计算结果为 true。
ms.openlocfilehash: 01721b460d87d3282a1a793966b0259e0f1342dd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518936"
---
# <a name="and-protectionruleandtype"></a>And (ProtectionRuleAndType)

And 元素指定所有子元素都必须匹配，计算结果为 **true**。
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AllInternal](allinternal.md) <br/> |如果电子邮件的所有收件人都是发件人组织内部的，则计算结果为 **true。**  <br/> |
|**And** <br/> |指定所有子元素都必须匹配以使值为 **true**。  <br/> |
|[RecipientIs](recipientis.md) <br/> |指定电子邮件的任何收件人与 [ProtectionRuleValueType ](value-protectionrulevaluetype.md) 元素中的子 Value (任何) 匹配。  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |指定发件人的部门与 [ProtectionRuleValueType ](value-protectionrulevaluetype.md) 元素的子 Value (中) 部门。  <br/> |
|[True](true.md) <br/> |指定始终匹配的条件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[条件](condition.md) <br/> |确定要执行该规则的操作部分必须满足的条件。  <br/> |
|**And** <br/> |指定所有子元素都必须匹配以使值为 **true**。  <br/> |
   
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

