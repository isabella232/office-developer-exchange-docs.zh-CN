---
title: RequestedView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestedView
api_type:
- schema
ms.assetid: e2b4cf8c-5d43-4cd8-b86d-cc27a5d2f095
description: RequestedView 元素定义的客户端请求的日历信息的类型。
ms.openlocfilehash: 7710227720264432c325f95da894cbbbd4748dc0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827145"
---
# <a name="requestedview"></a>RequestedView

**RequestedView**元素定义的客户端请求的日历信息的类型。 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[RequestedView](requestedview.md)
  
```xml
<RequestedView>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</RequestedView>
```

 **FreeBusyViewType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |指定响应中返回的忙/闲信息的类型。  <br/> 以下是此元素的 XPath:  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|无  <br/> |此值的请求无效。 此值是有效的响应。  <br/> |
|MergedOnly  <br/> |表示一个聚合的忙/闲流。 在一个林中的目标用户不具有可用性服务配置跨林方案中，可用性服务请求者的忙/闲信息的公用文件夹中检索目标用户的忙/闲信息。 公用文件夹只将忙/闲信息存储在合并的表单中，因为**MergedOnly**是唯一可用的信息。  <br/> |
|FreeBusy  <br/> |表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF。 这还包括约会的开始/结束的时间。 此视图是更丰富而不是一个聚合的忙/闲流提供比的旧的忙/闲查看，因为单个会议开始和结束时间。  <br/> |
|FreeBusyMerged  <br/> |代表中的所有属性**FreeBusy**与合并忙/闲信息的数据流。  <br/> |
|Detailed  <br/> |表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF;约会; 的开始/结束时间和主题、 位置和重要性如约会的各种属性。 此请求的视图将返回的最大量为其特权发出请求的用户的信息。 如果合并忙/闲信息仅为可用，为与用户的 Microsoft Exchange Server 2003 林请求信息**MergedOnly**将返回。 否则，将返回**FreeBusy**或**Detailed** 。  <br/> |
|DetailedMerged  <br/> |代表中的所有属性**Detailed**与合并忙/闲信息的数据流。 如果合并忙/闲信息仅为可用，则将返回**MergedOnly** 。 否则，将返回**FreeBusyMerged**或**DetailedMerged** 。  <br/> |
   
## <a name="remarks"></a>备注

此元素的设置的值与[FreeBusyViewType](freebusyviewtype.md)元素在响应中返回。 
  
下表显示不同的视图类型和相应的 MAPI 属性返回的内容。 每个视图类型基于以前的视图类型。
  
|**忙/闲视图类型**|**属性**|**MAPI 日历属性**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |古典状态  <br/> |属性标记 (0x80860003)  <br/> |
|**FreeBusy** <br/> |工作时间  <br/> ||
|**FreeBusy** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |古典状态  <br/> |属性标记 (0x80860003)  <br/> |
|**FreeBusyMerged** <br/> |工作时间  <br/> ||
|**FreeBusyMerged** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**详细** <br/> |古典状态  <br/> |属性标记 (0x80860003)  <br/> |
|**详细** <br/> |工作时间  <br/> ||
|**详细** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**详细** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**详细** <br/> |主题  <br/> |PR_SUBJECT  <br/> |
|**详细** <br/> |位置  <br/> |PR_LOCATION  <br/> |
|**详细** <br/> |条目 Id(unless private)  <br/> ||
|**详细** <br/> |私有标志  <br/> ||
|**详细** <br/> |IsMeeting  <br/> ||
|**详细** <br/> |IsRecurring  <br/> ||
|**详细** <br/> |IsException  <br/> ||
|**详细** <br/> |IsReminderSet  <br/> ||
|**DetailedMerged** <br/> |古典状态  <br/> |属性标记 (0x80860003)  <br/> |
|**DetailedMerged** <br/> |工作时间  <br/> ||
|**DetailedMerged** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |主题  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |位置  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |条目 Id(unless private)  <br/> ||
|**DetailedMerged** <br/> |私有标志  <br/> ||
|**DetailedMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**DetailedMerged** <br/> |IsMeeting  <br/> ||
|**DetailedMerged** <br/> |IsRecurring  <br/> ||
|**DetailedMerged** <br/> |IsException  <br/> ||
|**DetailedMerged** <br/> |IsReminderSet  <br/> ||
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserAvailability 操作](getuseravailability-operation.md)


[Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

