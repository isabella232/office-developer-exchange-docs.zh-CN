---
title: And
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
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: And 元素表示允许您在两个或多个搜索表达式之间执行布尔 AND 操作的搜索表达式。如果 And 元素中包含的所有搜索表达式为 true，则 AND 操作的结果为 true。
ms.openlocfilehash: f5239f19c2b5a931eefa9ff4a9dd8ed9d775bae2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464719"
---
# <a name="and"></a>和

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **And** 元素表示允许您在两个或多个搜索表达式之间执行布尔 **AND** 操作的搜索表达式。如果 **And** 元素中包含的所有搜索表达式为 **true**，则 **AND** 操作的结果为 **true**。
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 **AndType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> | 表示某个限制范围内表达式的基类。And 操作中必须有两个或多个搜索表达式。  <br/><br/>  必须将以下元素之一替换为 **SearchExpression** 元素：<ul><li> [Exists](exists.md)</li><li>[不包括](excludes.md)</li><li>[IsEqualTo](isequalto.md)</li><li>[IsNotEqualTo](isnotequalto.md)</li><li>[IsGreaterThan](isgreaterthan.md)</li><li>[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</li><li>[IsLessThan](islessthan.md)</li><li>[IsLessThanOrEqualTo](islessthanorequalto.md)</li><li>[Contains](contains.md)</li><li>[Not](not.md)</li><li>**And**</li><li>[或](or.md) </li></ul> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[限制](restriction.md) <br/> |表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。  <br/> |
|[not](not.md) <br/> |表示对其包含的搜索表达式的布尔值求反的搜索表达式。  <br/> |
|**And** <br/> |表示允许您在两个或多个搜索表达式之间执行布尔 **AND** 操作的搜索表达式。如果 **And** 元素中包含的所有搜索表达式为 **true**，则 **AND** 操作的结果为 **true**。  <br/> |
|[或](or.md) <br/> |表示在其包含的搜索表达式上执行逻辑 **OR** 操作的搜索表达式。如果其任何子级返回 **true**，则 **Or** 将返回 **true**。 **Or** 必须有两个或多个子级。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

