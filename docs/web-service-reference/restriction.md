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
description: 限制元素均表示的限制或用于筛选项目或 FindItem/FindFolder 和搜索文件夹操作中的文件夹的查询。
ms.openlocfilehash: 6b5702696db29910ae476a370bf362fe6a036ae7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827213"
---
# <a name="restriction"></a>限制

**限制**元素均表示的限制或用于筛选项目或 FindItem/FindFolder 和搜索文件夹操作中的文件夹的查询。 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[And](and.md) <br/> |代表一个搜索表达式，使您可以执行两个或多个搜索表达式之间的布尔**和**操作。  <br/> |
|[Contains](contains.md) <br/> |代表一个搜索表达式，确定给定的属性是否包含提供常量的字符串值。  <br/> |
|[不包括](excludes.md) <br/> |执行这些属性的位掩码。  <br/> |
|[Exists](exists.md) <br/> |代表返回**true**如果所提供的属性存在项目的搜索表达式。  <br/> |
|[IsEqualTo](isequalto.md) <br/> |代表一个搜索表达式的比较一个常数值的属性或另一个属性，并计算结果为**true** ，如果二者相等。  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |代表一个搜索表达式，如果第一个属性大于属性的值比较常量值或另一个属性，返回**true**的属性。  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |代表一个搜索表达式，如果第一个属性是大于或等于或属性的值比较常量值或另一个属性，返回**true**的属性。  <br/> |
|[IsLessThan](islessthan.md) <br/> |代表一个搜索表达式，如果第一个属性或属性的值小于比较常量值或另一个属性，返回**true**的属性。  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |代表一个搜索表达式，如果第一个属性小于或等于或属性的值比较常量值或另一个属性，返回**true**的属性。  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |表示搜索表达式的比较常量值或另一个属性，返回**true**的属性，如果值不相同。  <br/> |
|[not](not.md) <br/> |代表一个搜索表达式，它包含的搜索表达式的布尔值求非。  <br/> |
|[或](or.md) <br/> |代表搜索表达式执行逻辑**OR**运算上包含的搜索表达式。 如果任何其子返回**true**，则将返回**true** **或**元素。  <br/> |
|[SearchExpression](searchexpression.md) <br/> |代表限制中的替代的元素。 XML 实例文档中不使用此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义一个请求，以确定邮箱中的文件夹。  <br/> |
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。  <br/> |
|[SearchParameters](searchparameters.md) <br/> |表示定义搜索文件夹的参数。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

