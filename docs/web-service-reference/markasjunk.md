---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: MarkAsJunk 元素指定的请求将项目移动到垃圾邮件文件夹并将发件人添加到阻止发件人列表。
ms.openlocfilehash: fbb3eee7ce350954888931ca55b27f596656b161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826350"
---
# <a name="markasjunk"></a>MarkAsJunk

**MarkAsJunk**元素指定的请求将项目移动到垃圾邮件文件夹并将发件人添加到阻止发件人列表。 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 **MarkAsJunkType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|IsJunk  <br/> |文本值为**true**的**IsJunk**属性指示将电子邮件发件人添加到阻止发件人列表。 如果值为**false**指示电子邮件发件人已从阻止发件人列表中，如果电子邮件发件人已在列表。  <br/> |
|MoveItem  <br/> |文本值为**true**的**MoveItem**属性指示的项目将被移动到默认的垃圾邮件文件夹。 如果值为**false**指示项目也不会移动至默认垃圾邮件文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

[ItemIds](itemids.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> ||
   

