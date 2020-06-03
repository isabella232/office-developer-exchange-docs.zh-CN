---
title: 语言（DiscoverySearchConfigurationType）
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: Language （DiscoverySearchConfigurationType）元素标识要用于特定于区域的日期范围格式的区域性。 它还指定在搜索查询中使用的语言。
ms.openlocfilehash: 3cf85525147bec5d6dfc6fe2b2af5916d42c44be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463284"
---
# <a name="language-discoverysearchconfigurationtype"></a>语言（DiscoverySearchConfigurationType）

**Language （DiscoverySearchConfigurationType）** 元素标识要用于特定于区域的日期范围格式的区域性。 它还指定在搜索查询中使用的语言。 
  
```XML
<Language />
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>文本值

**Language （DiscoverySearchConfigurationType）** 元素的文本值是一种区域性或语言。 
  
## <a name="remarks"></a>备注

此元素指定在[SearchMailboxes 操作](searchmailboxes-operation.md)或[SetHoldOnMailboxes 操作](setholdonmailboxes-operation.md)中指定的日期范围的格式。
  
Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[DiscoverySearchConfiguration](discoverysearchconfiguration.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

