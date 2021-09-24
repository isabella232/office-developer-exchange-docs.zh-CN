---
title: RequestedView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RequestedView
api_type:
- schema
ms.assetid: e2b4cf8c-5d43-4cd8-b86d-cc27a5d2f095
description: RequestedView 元素定义客户端请求的日历信息的类型。
ms.openlocfilehash: 350922a7fef90c26ace0ef8be07ebb866d304eb3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509474"
---
# <a name="requestedview"></a>RequestedView

**RequestedView** 元素定义客户端请求的日历信息的类型。 
  
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

|**元素**|**说明**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |指定响应中返回的忙/闲信息的类型。  <br/> 下面是此元素的 XPath：  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|无  <br/> |对于请求无效此值。 此值对响应有效。  <br/> |
|MergedOnly  <br/> |表示聚合的忙/闲流。 在一个林中的目标用户未配置可用性服务的跨林方案中，请求者的可用性服务从忙/闲公用文件夹中检索目标用户的忙/闲信息。 由于公用文件夹仅存储合并表单中的忙/闲信息， **因此 MergedOnly** 是唯一可用的信息。  <br/> |
|FreeBusy  <br/> |表示旧状态信息：忙、闲、暂定和 OOF。 这还包括约会的开始/结束时间。 此视图比旧忙/闲视图更丰富，因为提供了单独的会议开始时间和结束时间，而不是聚合的忙/闲流。  <br/> |
|FreeBusyMerged  <br/> |表示 **FreeBusy 中具有** 合并的忙/闲信息流的所有属性。  <br/> |
|详细  <br/> |表示旧状态信息：忙、闲、暂定和 OOF;约会的开始/结束时间;以及约会的各种属性，如主题、位置和重要性。 此请求的视图将返回请求用户具有特权的最大信息量。 如果只有合并的忙/闲信息可用，与请求 Microsoft Exchange Server 2003 林中的用户信息一样，将返回 **MergedOnly。** 否则，**将返回 FreeBusy** **或 Detailed。**  <br/> |
|DetailedMerged  <br/> |代表"详细 **"中具有** 合并的忙/闲信息流的所有属性。 如果只有合并的忙/闲信息可用，将返回 **MergedOnly。** 否则，**将返回 FreeBusyMerged** 或 **DetailedMerged。**  <br/> |
   
## <a name="remarks"></a>注解

此元素设置的值在响应中返回 [FreeBusyViewType](freebusyviewtype.md) 元素。 
  
下表显示了为不同的视图类型和相应的 MAPI 属性返回的值。 每个视图类型都基于以前的视图类型构建。
  
|**忙/闲视图类型**|**属性**|**MAPI Calendar 属性**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |经典状态  <br/> |PropTag (0x80860003)   <br/> |
|**FreeBusy** <br/> |工作时间  <br/> ||
|**FreeBusy** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |经典状态  <br/> |PropTag (0x80860003)   <br/> |
|**FreeBusyMerged** <br/> |工作时间  <br/> ||
|**FreeBusyMerged** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**详细** <br/> |经典状态  <br/> |PropTag (0x80860003)   <br/> |
|**详细** <br/> |工作时间  <br/> ||
|**详细** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**详细** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**详细** <br/> |主题  <br/> |PR_SUBJECT  <br/> |
|**详细** <br/> |位置  <br/> |PR_LOCATION  <br/> |
|**详细** <br/> |Entry-Id (，除非私有)   <br/> ||
|**详细** <br/> |私有标志  <br/> ||
|**详细** <br/> |IsMeeting  <br/> ||
|**详细** <br/> |IsRecurring  <br/> ||
|**详细** <br/> |IsException  <br/> ||
|**详细** <br/> |IsReminderSet  <br/> ||
|**DetailedMerged** <br/> |经典状态  <br/> |PropTag (0x80860003)   <br/> |
|**DetailedMerged** <br/> |工作时间  <br/> ||
|**DetailedMerged** <br/> |开始时间  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |结束时间  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |主题  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |位置  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |Entry-Id (，除非私有)   <br/> ||
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

