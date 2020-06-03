---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: NormalizedBody 元素将项的 Body 属性的 HTML 表示形式指定为可以插入到另一个 HTML 正文中的片段。
ms.openlocfilehash: fb249794bccfeed198e7a3230ab53c66893dcf96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462666"
---
# <a name="normalizedbody"></a>NormalizedBody

**NormalizedBody**元素将项的**BODY**属性的 HTML 表示形式指定为可以插入到另一个 HTML 正文中的片段。 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|BodyType  <br/> |指示正文类型。 **Office.mailboxenums.bodytype**属性的**文本**值表示正文是纯文本格式。 **Office.mailboxenums.bodytype**属性的**HTML**值表示正文是 HTML 格式。 **Office.mailboxenums.bodytype**属性是必需的。  <br/> |
|IsTruncated  <br/> |指示正文内容已被截断。 **IsTruncated**属性的文本值为**false**表示正文内容尚未被截断。 如果正常化的正文长度长于[MaximumBodySize](maximumbodysize.md)元素中设置的值，则将截断正常化的正文。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[项](item.md)  | [邮件](message-ex15websvcsotherref.md)  | [MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [MeetingCancellation](meetingcancellation.md)  | [任务](task.md)  | [PostItem](postitem.md)  | [CalendarItem](calendaritem.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)
  
## <a name="text-value"></a>文本值

**NormalizedBody**元素的文本值是项目的规范化正文。 
  
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
   

