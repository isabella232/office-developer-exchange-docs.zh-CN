---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: MarkAsJunk 元素指定将项目移动到垃圾邮件文件夹以及将发件人添加到阻止发件人列表的请求。
ms.openlocfilehash: 252c36b8bb3662ffd6c0fe470a81b6f0b55acb69
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544085"
---
# <a name="markasjunk"></a>MarkAsJunk

**MarkAsJunk** 元素指定将项目移动到垃圾邮件文件夹以及将发件人添加到阻止发件人列表的请求。 
  
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
|IsJunk  <br/> |**IsJunk** 属性的文本值 **true** 指示电子邮件发件人已添加到阻止的发件人列表。 false **值表示** 电子邮件发件人已从阻止的发件人列表中删除（如果电子邮件发件人已位于列表中）。  <br/> |
|MoveItem  <br/> |**MoveItem** 属性的文本值 **true** 指示项目已移动到默认垃圾邮件文件夹。 false **值表示** 项目未移动到默认垃圾邮件文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

[ItemIds](itemids.md)
  
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
   

