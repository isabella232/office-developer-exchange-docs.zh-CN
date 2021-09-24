---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: NormalizedBody 元素将项目的 Body 属性的 HTML 表示形式指定为可以插入到其他 HTML 正文中的片段。
ms.openlocfilehash: 9ce7a745cfbe2e08afbe4c83873cb670b6afa571
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515430"
---
# <a name="normalizedbody"></a>NormalizedBody

**NormalizedBody** 元素将项目的 **Body** 属性的 HTML 表示形式指定为可以插入到其他 HTML 正文中的片段。 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|BodyType  <br/> |指示正文类型。 **BodyType** **属性的值 Text** 指示正文为纯文本形式。 **BodyType** **属性的 HTML** 值指示正文为 HTML 格式。 **BodyType** 属性是必需的。  <br/> |
|IsTruncated  <br/> |指示正文内容已被截断。 **IsTruncated** 属性的文本值 **false** 表示尚未截断正文内容。 如果规范化正文长度长于 [MaximumBodySize](maximumbodysize.md) 元素中设置的值，则规范化正文将被截断。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[Item](item.md)  | [邮件](message-ex15websvcsotherref.md)  | [MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [MeetingCancellation](meetingcancellation.md)  | [任务](task.md)  | [PostItem](postitem.md)  | [CalendarItem](calendaritem.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)
  
## <a name="text-value"></a>文本值

**NormalizedBody** 元素的文本值是项目的规范化正文。 
  
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
   

