---
title: DiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 085384f9-dca4-4534-82e2-dd782471d0da
description: DiscoverySearchConfiguration 元素指定电子数据展示搜索的配置。
ms.openlocfilehash: 4f5f0a5b8e78521302fd136f0a0280aa3ff4e4c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523095"
---
# <a name="discoverysearchconfiguration"></a>DiscoverySearchConfiguration

**DiscoverySearchConfiguration** 元素指定电子数据展示搜索的配置。 
  
```XML
<DiscoverySearchConfiguration>
    <SearchId></SearchId>
    <SearchQuery></SearchQuery>
    <SearchableMailboxes></SearchableMailboxes>
</DiscoverySearchConfiguration>
```

 **DiscoverySearchConfigurationType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SearchId](searchid.md) <br/> |指定搜索的标识符。  <br/> |
|[SearchQuery](searchquery.md) <br/> |指定电子数据展示搜索查询的名称。  <br/> |
|[SearchableMailboxes](searchablemailboxes.md) <br/> |包含从 **GetSearchableMailboxes** 请求返回的邮箱列表。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DiscoverySearchConfigurations](discoverysearchconfigurations.md) <br/> |指定 **DiscoverySearchConfiguration 元素的** 数组。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

