---
title: 限制
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Restriction
api_type:
- schema
ms.assetid: 77f19014-d112-4999-8e83-ecc32a117a73
description: 限制元素表示用于筛选 FindItem/FindFolder 中的项或文件夹以及搜索文件夹操作的限制或查询。
ms.openlocfilehash: 6037ba15417d67d393ca70f3edf2248749c396e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465287"
---
# <a name="restriction"></a>限制

**限制**元素表示用于筛选 FindItem/FindFolder 中的项或文件夹以及搜索文件夹操作的限制或查询。 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[And](and.md) <br/> |表示允许您在两个或多个搜索表达式之间执行布尔**AND**运算的搜索表达式。  <br/> |
|[Contains](contains.md) <br/> |表示一个搜索表达式，该表达式确定给定属性是否包含提供的常量字符串值。  <br/> |
|[不包括](excludes.md) <br/> |执行这些属性的位掩码。  <br/> |
|[Exists](exists.md) <br/> |表示在项上存在提供的属性时返回**true**的搜索表达式。  <br/> |
|[IsEqualTo](isequalto.md) <br/> |表示搜索表达式，该表达式将属性与常数值或其他属性进行比较，如果它们相等，则计算结果为**true** 。  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性大于值或属性，**则返回 true** 。  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性大于或等于 value 或属性，**则返回 true** 。  <br/> |
|[IsLessThan](islessthan.md) <br/> |表示用于将属性与常量值或其他属性进行比较的搜索表达式，如果第一个属性小于值或属性，**则返回 true** 。  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性小于或等于 value 或属性，**则返回 true** 。  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |表示用于将属性与常量值或其他属性进行比较的搜索表达式，如果值不相同，**则返回 true** 。  <br/> |
|[Not](not.md) <br/> |表示对其包含的搜索表达式的布尔值求反的搜索表达式。  <br/> |
|[或](or.md) <br/> |表示在其包含的搜索表达式上执行逻辑**OR**运算的搜索表达式。 如果其任何子级返回**true**，则**或**元素将返回**true** 。  <br/> |
|[SearchExpression](searchexpression.md) <br/> |表示限制中的替代元素。 XML 实例文档中不使用此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义用于标识邮箱中的文件夹的请求。  <br/> |
|[FindItem](finditem.md) <br/> |定义在邮箱中查找项目的请求。  <br/> |
|[SearchParameters](searchparameters.md) <br/> |表示用于定义搜索文件夹的参数。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

