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
description: RequestedView 元素定义客户端请求的日历信息的类型。
ms.openlocfilehash: bc4f863841fc5a7d1d23f0bd4c7c2895d2593a2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459158"
---
# <a name="requestedview"></a>RequestedView

**RequestedView**元素定义客户端请求的日历信息的类型。 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[RequestedView](requestedview.md)
  
```xml
<RequestedView>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</RequestedView>
```

 **FreeBusyViewType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |指定响应中返回的忙/闲信息的类型。  <br/> 以下是此元素的 XPath：  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|无  <br/> |对于请求，此值无效。 此值对响应有效。  <br/> |
|MergedOnly  <br/> |表示聚合的忙/闲流。 在跨林方案中，在一个林中的目标用户未配置可用性服务的情况下，请求者的可用性服务将从忙/闲公用文件夹中检索目标用户的忙/闲信息。 由于公用文件夹仅将忙/闲信息存储在合并表单中，因此**MergedOnly**是唯一可用的信息。  <br/> |
|FreeBusy  <br/> |代表旧状态信息：闲、忙、暂定和 OOF。 这还包括约会的开始/结束时间。 此视图比旧版的忙/闲视图更丰富，因为提供了单个会议开始和结束时间，而不是聚合的忙/闲流。  <br/> |
|FreeBusyMerged  <br/> |表示包含合并的忙/闲信息流的**FreeBusy**中的所有属性。  <br/> |
|具体  <br/> |代表旧状态信息：闲、忙、暂定和 OOF;约会的开始/结束时间;以及约会的各种属性，如主题、位置和重要性。 此请求的视图将返回请求用户有权限的最大信息量。 如果只提供了合并的忙/闲信息，就像 Microsoft Exchange Server 2003 林中的用户请求信息一样，将返回**MergedOnly** 。 否则，将返回**FreeBusy**或**详细信息**。  <br/> |
|DetailedMerged  <br/> |表示与合并的忙/闲信息流**详细**的所有属性。 如果仅提供了合并的忙/闲信息，将返回**MergedOnly** 。 否则，将返回**FreeBusyMerged**或**DetailedMerged** 。  <br/> |
   
## <a name="remarks"></a>备注

此元素设置的值随响应中的[FreeBusyViewType](freebusyviewtype.md)元素一起返回。 
  
下表显示了为不同的视图类型和相应的 MAPI 属性返回的内容。 每个视图类型都基于以前的视图类型。
  
|**忙/闲视图类型**|**属性**|**MAPI 日历属性**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |古典状态  <br/> |属性标记（0x80860003）  <br/> |
|**FreeBusy** <br/> |工作时间  <br/> ||
|**FreeBusy** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |古典状态  <br/> |属性标记（0x80860003）  <br/> |
|**FreeBusyMerged** <br/> |工作时间  <br/> ||
|**FreeBusyMerged** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**具体** <br/> |古典状态  <br/> |属性标记（0x80860003）  <br/> |
|**具体** <br/> |工作时间  <br/> ||
|**具体** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**具体** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**具体** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**具体** <br/> |位置  <br/> |PR_LOCATION  <br/> |
|**具体** <br/> |条目 Id （除非是私有）  <br/> ||
|**具体** <br/> |私有标志  <br/> ||
|**具体** <br/> |IsMeeting  <br/> ||
|**具体** <br/> |IsRecurring  <br/> ||
|**具体** <br/> |IsException  <br/> ||
|**具体** <br/> |IsReminderSet  <br/> ||
|**DetailedMerged** <br/> |古典状态  <br/> |属性标记（0x80860003）  <br/> |
|**DetailedMerged** <br/> |工作时间  <br/> ||
|**DetailedMerged** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |位置  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |条目 Id （除非是私有）  <br/> ||
|**DetailedMerged** <br/> |私有标志  <br/> ||
|**DetailedMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**DetailedMerged** <br/> |IsMeeting  <br/> ||
|**DetailedMerged** <br/> |IsRecurring  <br/> ||
|**DetailedMerged** <br/> |IsException  <br/> ||
|**DetailedMerged** <br/> |IsReminderSet  <br/> ||
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserAvailability 操作](getuseravailability-operation.md)


[获取用户可用性](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

