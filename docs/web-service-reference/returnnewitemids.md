---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: ReturnNewItemIds 元素指示是否在响应中返回新项的项标识符。
ms.openlocfilehash: 003676c4c034454aa551e42bf3af976183117b8c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465112"
---
# <a name="returnnewitemids"></a>ReturnNewItemIds

**ReturnNewItemIds**元素指示是否在响应中返回新项的项标识符。 
  
```XML
<ReturnNewItemIds/>
```

 **xs： boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopyItem](copyitem.md) <br/> |定义对 Exchange 存储中的邮箱中的项目进行复制的请求。  <br/> |
|[MoveItem](moveitem.md) <br/> |定义在 Exchange 存储中移动项目的请求。  <br/> |
   
## <a name="text-value"></a>文本值

如果**ReturnNewItemIds**元素的文本值为**true** ，则表示在响应中返回新的项目标识符。 **如果值为 false** ，则表示响应中不返回新的项目标识符。 
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

