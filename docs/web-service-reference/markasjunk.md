---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: MarkAsJunk 元素指定将项目移动到 "垃圾邮件" 文件夹，并将发件人添加到 "阻止的发件人" 列表中的请求。
ms.openlocfilehash: 99adc423864f3096772394ef290df20e158e457d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467079"
---
# <a name="markasjunk"></a>MarkAsJunk

**MarkAsJunk**元素指定将项目移动到 "垃圾邮件" 文件夹，并将发件人添加到 "阻止的发件人" 列表中的请求。 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 **MarkAsJunkType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|IsJunk  <br/> |**IsJunk**属性的文本值为**true**表示将电子邮件发件人添加到 "阻止的发件人" 列表中。 如果值为**false** ，则表示电子邮件发件人已从阻止的发件人列表中删除（如果该电子邮件发件人已在列表中）。  <br/> |
|MoveItem  <br/> |**MoveItem**属性的文本值为**true**表示将项目移动到默认的 "垃圾邮件" 文件夹。 **如果值为 false** ，则表示项目不会移动到默认的垃圾邮件文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

[ItemIds](itemids.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |消息 .xsd  <br/> |
|可以为空  <br/> ||
   

