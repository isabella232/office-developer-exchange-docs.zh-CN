---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: ReturnNewItemIds 元素指示是否在响应中返回新项的项目标识符。
ms.openlocfilehash: 93ff4e37c56c3583e81711ba7e3582706d9ef940
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512378"
---
# <a name="returnnewitemids"></a>ReturnNewItemIds

**ReturnNewItemIds** 元素指示是否在响应中返回新项的项目标识符。 
  
```XML
<ReturnNewItemIds/>
```

 **xs：boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopyItem](copyitem.md) <br/> |定义复制邮件存储中邮箱中的Exchange请求。  <br/> |
|[MoveItem](moveitem.md) <br/> |定义在项目存储中移动Exchange请求。  <br/> |
   
## <a name="text-value"></a>文本值

**ReturnNewItemIds** 元素的文本值 **true** 指示在响应中返回新的项标识符。 false **值表示** 未在响应中返回新项标识符。 
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

