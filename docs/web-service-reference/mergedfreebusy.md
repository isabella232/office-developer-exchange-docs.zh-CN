---
title: MergedFreeBusy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusy
api_type:
- schema
ms.assetid: ea45590d-476e-4b68-9fe8-ae392feadfea
description: MergedFreeBusy 元素包含合并的忙/闲数据流。
ms.openlocfilehash: 542b9fae0c36b0236bd806e8a9117753968e812c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826449"
---
# <a name="mergedfreebusy"></a>MergedFreeBusy

**MergedFreeBusy**元素包含合并的忙/闲数据流。 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[MergedFreeBusy](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 **string**
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

如果[FreeBusyViewType](freebusyviewtype.md)元素的值可以是下列选项之一，由服务器提供的文本值： 
  
- DetailedMerged
    
- FreeBusyMerged
    
- MergedOnly
    
忙/闲信息的数据流的文本值。 
  
## <a name="remarks"></a>备注

由的[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)和[TimeWindow](timewindow.md)元素定义此元素提供的数据流。 [TimeWindow](timewindow.md)元素定义查询可用性的时间跨度。 [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义如何从[TimeWindow](timewindow.md)元素所需时间分为**MergedFreeBusy**元素中返回的时间间隔。 **MergedFreeBusy**流中的每个数字代表[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义一个单个时间间隔。 下表列出各个间隔的可能值。 
  
|**数字**|**可用性**|
|:-----|:-----|
|0  <br/> |免费  <br/> |
|1  <br/> |暂定  <br/> |
|2  <br/> |忙碌  <br/> |
|3  <br/> |不在办公室 (OOF)  <br/> |
|4  <br/> |没有数据  <br/> |
   
例如，忙/闲数据的请求包含代表四小时[TimeWindow](timewindow.md)元素和[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素值，该值代表 60 分钟。 如果请求的用户的日历 OOF 前 60 分钟，以下 90 分钟，忙和计划外的最终 90 分钟在时间窗口中， **MergedFreeBusy**流将 3220。 如果间隔包含多个可用性分类，最大数字用于分类的时间间隔。 
  
提供此元素的详细程度取决于所请求者授予的权限。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
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

