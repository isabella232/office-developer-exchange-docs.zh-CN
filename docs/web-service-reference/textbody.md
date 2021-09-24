---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: TextBody 元素指定文本正文。
ms.openlocfilehash: 5dfc0aa76f0b0778d785e46fe12259c4a226b89f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515178"
---
# <a name="textbody"></a>TextBody

**TextBody** 元素指定文本正文。 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|BodyTypeType  <br/> |指示正文类型。 **BodyTypeType** 属性的值 **Text** 指示正文为纯文本形式。 **BodyTypeType** 属性 **的 HTML** 值指示正文为 HTML 形式。 **BodyTypeType** 属性是必需的。  <br/> |
|IsTruncated  <br/> |指示正文内容已被截断。 **IsTruncated** 属性的文本值 **false** 表示尚未截断正文内容。 如果文本正文长度长于 [MaximumBodySize](maximumbodysize.md) 元素中设置的值，则规范化正文将被截断。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[Item](item.md)  | [联系人](contact.md)  | [邮件](message-ex15websvcsotherref.md)  | [DistributionList](distributionlist.md)  | [CalendarItem](calendaritem.md)  | [PostItem](postitem.md)  | [任务](task.md)
  
## <a name="text-value"></a>文本值

**TextBody** 元素的文本值是项的文本正文。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

