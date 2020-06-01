---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: TextBody 元素指定文本正文。
ms.openlocfilehash: c0002785fb990a251267218f7a5f232e521db41a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459481"
---
# <a name="textbody"></a>TextBody

**TextBody**元素指定文本正文。 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|BodyTypeType  <br/> |指示正文类型。 **BodyTypeType**属性的**文本**值表示正文是纯文本格式。 **BodyTypeType**属性的**HTML**值表示正文是 HTML 格式。 **BodyTypeType**属性是必需的。  <br/> |
|IsTruncated  <br/> |指示正文内容已被截断。 **IsTruncated**属性的文本值为**false**表示正文内容尚未被截断。 如果文本正文长度长于在[MaximumBodySize](maximumbodysize.md)元素中设置的值，则将截断正常化正文。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[项](item.md)  | [联系人](contact.md)  | [邮件](message-ex15websvcsotherref.md)  | [DistributionList](distributionlist.md)  | [CalendarItem](calendaritem.md)  | [PostItem](postitem.md)  | [任务](task.md)
  
## <a name="text-value"></a>文本值

**TextBody**元素的文本值是项目的文本正文。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

