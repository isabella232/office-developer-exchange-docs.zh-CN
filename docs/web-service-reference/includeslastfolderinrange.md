---
title: IncludesLastFolderInRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludesLastFolderInRange
api_type:
- schema
ms.assetid: 95837904-17be-49b7-831c-de4fb20fccfb
description: IncludesLastFolderInRange 元素指示是否已在响应中包含要同步的最后一个项目。
ms.openlocfilehash: 9ba401cf639ef7988fa7a1437a64d09ff54c5960
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466449"
---
# <a name="includeslastfolderinrange"></a>IncludesLastFolderInRange

**IncludesLastFolderInRange**元素指示是否已在响应中包含要同步的最后一个项目。 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[IncludesLastFolderInRange](includeslastfolderinrange.md)
  
```xml
<IncludesLastFolderInRange/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |包含 SyncFolderHierarchy 请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

表示一个布尔值的文本值是必需的。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderHierarchy 操作](syncfolderhierarchy-operation.md)


[Exchange 的 EWS 引用](ews-reference-for-exchange.md)
  
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

