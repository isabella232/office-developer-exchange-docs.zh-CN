---
title: 语言 (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: Language (DiscoverySearchConfigurationType) 元素标识要区域性特定格式的日期范围使用的区域性。 它还指定搜索查询中使用的语言。
ms.openlocfilehash: 1e904ac4d7f525b2d12cfe83f0da33b9ed474066
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826197"
---
# <a name="language-discoverysearchconfigurationtype"></a>语言 (DiscoverySearchConfigurationType)

**Language (DiscoverySearchConfigurationType)** 元素标识要区域性特定格式的日期范围使用的区域性。 它还指定搜索查询中使用的语言。 
  
```XML
<Language />
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>文本值

区域性或语言的**语言 (DiscoverySearchConfigurationType)** 元素的文本值。 
  
## <a name="remarks"></a>备注

此元素指定[SearchMailboxes 操作](searchmailboxes-operation.md)或[SetHoldOnMailboxes 操作](setholdonmailboxes-operation.md)中指定的日期范围的格式。
  
Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[DiscoverySearchConfiguration](discoverysearchconfiguration.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

