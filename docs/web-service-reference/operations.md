---
title: 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Operations
api_type:
- schema
ms.assetid: d8cd41b1-28ae-4c95-9ff6-8b25c8e18306
description: 操作元素包含可在收件箱中执行的一组规则操作。
ms.openlocfilehash: 4bbec4ad6424f802bb6781a870d65f23705e88c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462484"
---
# <a name="operations"></a>操作

**操作**元素包含可在收件箱中执行的一组规则操作。 
  
[UpdateInboxRules](updateinboxrules.md)
  
```XML
<Operations>
    <CreateRuleOperation/>
    <SetRuleOperation/>
    <DeleteRuleOperation/>
</Operations>
```

 **ArrayOfRuleOperationsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateRuleOperation](createruleoperation.md) <br/> |表示用于创建新的收件箱规则的操作。  <br/> |
|[SetRuleOperation](setruleoperation.md) <br/> |表示更新收件箱规则的操作。  <br/> |
|[DeleteRuleOperation](deleteruleoperation.md) <br/> |表示删除收件箱规则的操作。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UpdateInboxRules](updateinboxrules.md) <br/> |定义更新服务器存储中的邮箱的收件箱规则的请求。  <br/> |
   
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



[UpdateInboxRules 操作](updateinboxrules-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

