---
title: ResolutionSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolutionSet
api_type:
- schema
ms.assetid: 43d5b876-0e87-4414-9b1d-bff1c1ec825c
description: ResolutionSet 元素包含一组用于不明确名称的分辨率。
ms.openlocfilehash: f77b8a94871aa7827c98a3bb15fdf4a3a35c7c55
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521744"
---
# <a name="resolutionset"></a>ResolutionSet

**ResolutionSet** 元素包含一组用于不明确名称的分辨率。 
  
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
|**IndexedPagingOffset** <br/> |表示应在使用索引页面视图时用于下一个请求的下一个索引。  <br/> |
|**NumeratorOffset** <br/> |表示使用分数页面视图时用于下一个请求的新分子值。  <br/> |
|**AbsoluteDenominator** <br/> |表示在使用分数页面视图时用于下一个请求的下一个分母。  <br/> |
|**IncludesLastItemInRange** <br/> |如果当前结果包含查询中的最后一项，则此属性将为 true，因此不需要进行其他分页。  <br/> |
|**TotalItemsInView** <br/> |表示视图中的项目总数。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[解决方法](resolution.md) <br/> |包含单个已解析的实体。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResolveNamesResponseMessage](resolvenamesresponsemessage.md) <br/> |包含 ResolveNames 请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>注解

**ResolutionSet** 元素最多可包含 100 个已解析实体。 
  
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

