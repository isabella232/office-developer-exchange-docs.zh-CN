---
title: Language (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: DiscoverySearchConfigurationType (的 Language) 元素标识要用于日期范围的区域性特定格式的区域性。 它还指定搜索查询中使用的语言。
ms.openlocfilehash: 5d51960aa00b2c47d96972abc05e4d6027eeecb3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540893"
---
# <a name="language-discoverysearchconfigurationtype"></a>Language (DiscoverySearchConfigurationType)

**DiscoverySearchConfigurationType** (的 Language) 元素标识要用于日期范围的区域性特定格式的区域性。 它还指定搜索查询中使用的语言。 
  
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

**DiscoverySearchConfigurationType ()** Language 元素的文本值是区域性或语言。 
  
## <a name="remarks"></a>注解

此元素指定 [SearchMailboxes](searchmailboxes-operation.md) 操作或 [SetHoldOnMailboxes](setholdonmailboxes-operation.md)操作中指定的日期范围的格式。
  
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

