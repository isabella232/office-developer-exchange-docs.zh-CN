---
title: ResolutionSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolutionSet
api_type:
- schema
ms.assetid: 43d5b876-0e87-4414-9b1d-bff1c1ec825c
description: ResolutionSet 元素包含一个不明确名称的分辨率数组。
ms.openlocfilehash: 483a096a7fcedbabe25758ebcaa31c83405a0ad4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467170"
---
# <a name="resolutionset"></a>ResolutionSet

**ResolutionSet**元素包含一个不明确名称的分辨率数组。 
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
  
[ResolutionSet](resolutionset.md)
  
```xml
<ResolutionSet IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Resolution/>
</ResolutionSet>
```

 **ArrayOfResolutionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |表示在使用索引页视图时应用于下一个请求的下一个索引。  <br/> |
|**NumeratorOffset** <br/> |表示在使用分数页面视图时用于下一个请求的新的分子值。  <br/> |
|**AbsoluteDenominator** <br/> |表示使用分数页面视图时用于下一个请求的下一个分母。  <br/> |
|**IncludesLastItemInRange** <br/> |如果当前结果包含查询中的最后一项，因此不需要进行其他分页，则此属性为 true。  <br/> |
|**TotalItemsInView** <br/> |表示视图中的项目总数。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[解决方法](resolution.md) <br/> |包含单个已解析的实体。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |包含 ResolveNames 请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>备注

**ResolutionSet**元素最多可包含100个已解析实体。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ResolveNames](resolvenames.md)
  
[ResolveNamesResponse](resolvenamesresponse.md)
  
[ResolveNames 操作](resolvenames-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

