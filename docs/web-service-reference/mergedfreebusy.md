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
ms.openlocfilehash: a1483449534f0d886e3c97a23d28c5d78f865042
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468724"
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |包含特定用户的可用性信息。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>文本值

如果[FreeBusyViewType](freebusyviewtype.md)元素的值是下列值之一，则由服务器提供一个文本值： 
  
- DetailedMerged
    
- FreeBusyMerged
    
- MergedOnly
    
该文本值是一种忙/闲信息流。 
  
## <a name="remarks"></a>备注

此元素提供的数据流由[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)和[TimeWindow](timewindow.md)元素定义。 [TimeWindow](timewindow.md)元素定义查询可用性的时间跨度。 [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义如何将[TimeWindow](timewindow.md)元素中的时间分成**MergedFreeBusy**元素中返回的间隔。 **MergedFreeBusy**流中的每个数字表示一个由[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义的间隔。 下表列出了单个间隔的可能值。 
  
|**数字**|**可用性**|
|:-----|:-----|
|0  <br/> |空闲  <br/> |
|1   <br/> |暂  <br/> |
|双面  <br/> |忙碌  <br/> |
|第三章  <br/> |外出 (OOF)  <br/> |
|4   <br/> |无数据  <br/> |
   
例如，忙/闲数据的请求包含一个[TimeWindow](timewindow.md)元素，该元素表示四个小时，一个[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素表示60分钟。 如果请求的用户的日历为前60分钟的 OOF，在时间窗口中等待以下90分钟，并对最后的90分钟进行了非计划，则**MergedFreeBusy**流将为3220。 如果某个间隔包含多个可用性分类，则将使用最大数量对该间隔进行分类。 
  
此元素提供的详细信息级别取决于授予请求者的权限。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserAvailability 操作](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

