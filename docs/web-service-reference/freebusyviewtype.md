---
title: FreeBusyViewType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyViewType
api_type:
- schema
ms.assetid: 7c7f82ba-fa52-4a3e-bec7-39d373c66fc7
description: FreeBusyViewType 元素表示的响应中返回的忙/闲信息的类型。
ms.openlocfilehash: fe965d062f72d99dff7148f4d00b12fd8c4e1366
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754443"
---
# <a name="freebusyviewtype"></a>FreeBusyViewType

**FreeBusyViewType**元素表示的响应中返回的忙/闲信息的类型。 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[FreeBusyViewType](freebusyviewtype.md)
  
```xml
<FreeBusyViewType>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</FreeBusyViewType>
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
|[FreeBusyView](freebusyview.md) <br/> |包含特定用户的可用性信息。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|无  <br/> |此值的请求无效。 此值是有效的响应。  <br/> |
|MergedOnly  <br/> |表示一个聚合的忙/闲流。 在一个林中的目标用户不具有可用性服务配置跨林方案中，可用性服务请求者的忙/闲信息的公用文件夹中检索目标用户的忙/闲信息。 公用文件夹只将忙/闲信息存储在合并的表单中，因为**MergedOnly**是唯一可用的信息。  <br/> |
|FreeBusy  <br/> |表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF。 这还包括约会的开始/结束的时间。 此视图是更丰富而不是一个聚合的忙/闲流提供比的旧的忙/闲查看，因为单个会议开始和结束时间。  <br/> |
|FreeBusyMerged  <br/> |代表中的所有属性**FreeBusy**与合并闲/忙时间信息的数据流。  <br/> |
|Detailed  <br/> |表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF;约会; 的开始/结束时间和主题、 位置和重要性如约会的各种属性。 此请求的视图将返回的最大量为其特权发出请求的用户的信息。 如果合并忙/闲信息仅为可用，为与用户的 Microsoft Exchange Server 2003 林请求信息**MergedOnly**将返回。 否则，将返回**FreeBusy**或**Detailed** 。  <br/> 如果通讯组列表指定**Detailed** ，则列表的成员的忙/闲信息合并，并返回**MergedOnly** 。  <br/> |
|DetailedMerged  <br/> |代表中的所有属性**Detailed**与合并闲/忙时间信息的数据流。 如果只有合并忙/闲信息可用，例如，如果该邮箱存在运行 Exchange 2003 的计算机上，将返回**MergedOnly** 。 否则，将返回**FreeBusyMerged**或**DetailedMerged** 。  <br/> |
   
## <a name="remarks"></a>备注

如果使用[FreeBusyView](freebusyview.md)元素，此元素是必需的。 [RequestedView](requestedview.md)元素中指定返回的忙/闲信息的类型。 描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。 
  
下表显示不同的视图类型和相应的 MAPI 属性返回的内容。 每个视图类型基于以前的视图类型。
  
|**FreeBusyViewType**|**属性**|**MAPI 日历属性**|
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
|**详细** <br/> |利用 Office 邮件 （如果请求）  <br/> ||
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
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

