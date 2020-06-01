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
description: 和元素指定所有子元素都必须匹配以求值为 true。
ms.openlocfilehash: ba898ccd77518971afaf713d1c7c7955f46465d5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464733"
---
# <a name="and-protectionruleandtype"></a>和 (ProtectionRuleAndType)

**和**元素指定所有子元素都必须匹配以求值为**true**。
  
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
|[AllInternal](allinternal.md) <br/> |如果电子邮件的所有收件人均为发件人的组织内部，则计算结果为**true** 。  <br/> |
|**And** <br/> |指定所有子元素都必须匹配以使值为 **true**。  <br/> |
|[收件人是](recipientis.md) <br/> |指定电子邮件的任何收件人与子[值（ProtectionRuleValueType）](value-protectionrulevaluetype.md)元素中的任何指定收件人相匹配。  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |指定发件人的部门与子[值（ProtectionRuleValueType）](value-protectionrulevaluetype.md)元素中的任何指定的部门相匹配。  <br/> |
|[True](true.md) <br/> |指定始终匹配的条件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[条件](condition.md) <br/> |确定要执行该规则的操作部分必须满足的条件。  <br/> |
|**And** <br/> |指定所有子元素都必须匹配以使值为 **true**。  <br/> |
   
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
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

