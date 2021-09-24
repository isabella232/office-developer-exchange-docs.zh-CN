---
title: GetImItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 455e5709-6c06-49fd-bfb2-403fc912287c
description: GetImItems 请求元素定义一个请求，用于获取有关指定的即时消息组和即时消息联系人角色的信息。
ms.openlocfilehash: 99be8e898623b5bc8c517886132b77da40a7fb1e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513589"
---
# <a name="getimitems"></a>GetImItems

**GetImItems** 请求元素定义一个请求，用于获取有关指定的即时消息组和即时消息联系人角色的信息。 
  
```XML
<GetImItems>
   <ContactIds/>
   <GroupIds/>
   <ExtendedProperties/>
</GetImItems>
```

 **GetImItemsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ContactIds](contactids.md)  | [GroupIds](groupids.md)  | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs) ](extendedproperties-nonemptyarrayofextendedfielduris.md)
  
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
   

