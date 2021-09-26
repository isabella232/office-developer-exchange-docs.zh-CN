---
title: RecipientIs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecipientIs
api_type:
- schema
ms.assetid: 5d2fd7ce-6137-4b3c-a716-c0218dcc8a09
description: RecipientIs 元素指定电子邮件的任何收件人与子 Value (ProtectionRuleValueType 元素) 收件人。
ms.openlocfilehash: 0bf9d96469c626ddc223b128a6d7fabebbfebc84
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542895"
---
# <a name="recipientis"></a>RecipientIs

**RecipientIs** 元素指定电子邮件的任何收件人与子 Value ([ProtectionRuleValueType](value-protectionrulevaluetype.md)元素中的指定) 匹配。 
  
```xml
<RecipientIs>   <Value/></RecipientIs>
```

 **ProtectionRuleRecipientIsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Value (ProtectionRuleValueType)](value-protectionrulevaluetype.md) <br/> |标识收件人。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[条件](condition.md) <br/> |确定要执行该规则的操作部分必须满足的条件。  <br/> |
|[和 (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |指示所有子元素都必须匹配，计算结果为 **true**。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

