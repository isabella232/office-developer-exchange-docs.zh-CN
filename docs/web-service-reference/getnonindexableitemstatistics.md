---
title: GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dd16d1fb-d82d-42e5-b64a-bc6c19c48fa8
description: GetNonIndexableItemStatistics 元素指定检索不可检索的项目统计信息的请求。
ms.openlocfilehash: 7e5b7b586a4fd6a293e62bdc9b7229eeb9f9476f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546201"
---
# <a name="getnonindexableitemstatistics"></a>GetNonIndexableItemStatistics

**GetNonIndexableItemStatistics** 元素指定检索不可检索的项目统计信息的请求。 
  
```XML
<GetNonIndexableItemStatistics>
    <Mailboxes/>
</GetNonIndexableItemStatistics>
```

 **GetNonIndexableItemStatisticsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailboxes (NonEmptyArrayOfLegacyDNsType)](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |指定 Mailbox 元素 **的** 数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
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

