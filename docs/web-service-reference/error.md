---
title: Error
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Error
api_type:
- schema
ms.assetid: b1f54673-578a-496b-99f5-0fde2c669278
description: Error 元素表示特定规则属性值、谓词属性值或操作属性值上的单一验证错误。
ms.openlocfilehash: aeeda25ccc3e657e99bd6f2fea12322fdd3e720d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530859"
---
# <a name="error"></a>错误

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Error** 元素表示特定规则属性值、谓词属性值或操作属性值上的单一验证错误。 
  
```XML
<Error>
   <FieldUri/>
   <ErrorCode/>
   <ErrorMessage/>
   <FieldValue/>
</Error>
```

 **RuleValidationErrorType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FieldUri (规则)](fielduri-rule.md) <br/> |指定指向导致验证错误的规则字段的 URI。  <br/> |
|[ErrorCode](errorcode.md) <br/> |表示规则验证错误代码，该代码描述是什么造成了每个规则谓词或操作验证失败。  <br/> |
|[ErrorMessage](errormessage.md) <br/> |表示验证错误的原因。  <br/> |
|[FieldValue](fieldvalue.md) <br/> |表示导致验证错误的字段值。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ValidationErrors](validationerrors.md) <br/> |表示每个出错的规则字段上的规则验证错误数组。  <br/> |
   
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

