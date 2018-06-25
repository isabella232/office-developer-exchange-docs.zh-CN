---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: TextBody 元素指定的文本正文。
ms.openlocfilehash: 78b18b27891d571605d2eeeeffb5c252cc790c11
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838200"
---
# <a name="textbody"></a>TextBody

**TextBody**元素指定的文本正文。 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|BodyTypeType  <br/> |指示将正文类型。 **Text** **BodyTypeType**属性的值指示正文采用纯文本形式。 **BodyTypeType**属性的值的**HTML**指示正文采用 HTML 窗体。 **BodyTypeType**属性是必需的。  <br/> |
|IsTruncated  <br/> |指示正文内容已被截断。 文本值为**false**的**IsTruncated**属性指示正文内容不被截断。 如果文本正文长度超过[MaximumBodySize](maximumbodysize.md)元素中设置的值，则将截断规范化的正文。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[项目](item.md) | [联系人](contact.md) | [消息](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [日历项目](calendaritem.md) | [PostItem](postitem.md) | [任务](task.md)
  
## <a name="text-value"></a>文本值

项目的文本正文的**TextBody**元素的文本值。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

