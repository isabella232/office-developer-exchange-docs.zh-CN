---
title: ValidationErrors
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ValidationErrors
api_type:
- schema
ms.assetid: 009526aa-22e7-4f5c-be88-079175aa9122
description: ValidationErrors元素表示一个数组的规则上有一个错误的每个规则字段的验证错误。
ms.openlocfilehash: 9b771addfc99a4f7fadebc64aebc484a8ae6060e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522374"
---
# <a name="validationerrors"></a>ValidationErrors

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **ValidationErrors** 元素表示一个数组的规则上有一个错误的每个规则字段的验证错误。 
  
```XML
<VaidationErrors>
   <Error/>
</ValidationErrors>
```

 **ArrayOfRuleValidationErrorsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Error](error.md) <br/> |表示在特定规则属性值、 谓词属性值或操作的属性值的单个验证错误  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RuleOperationError](ruleoperationerror.md) <br/> |表示一个规则操作错误。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

