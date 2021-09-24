---
title: MergedFreeBusy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MergedFreeBusy
api_type:
- schema
ms.assetid: ea45590d-476e-4b68-9fe8-ae392feadfea
description: MergedFreeBusy 元素包含合并的忙/闲数据流。
ms.openlocfilehash: db451d6b2e67313836771604fae57b14b6b3db10
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511028"
---
# <a name="mergedfreebusy"></a>MergedFreeBusy

**MergedFreeBusy** 元素包含合并的忙/闲数据流。 
  
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

如果 [FreeBusyViewType](freebusyviewtype.md) 元素的值为下列值之一，则服务器会提供文本值： 
  
- DetailedMerged
    
- FreeBusyMerged
    
- MergedOnly
    
文本值是一个忙/闲信息流。 
  
## <a name="remarks"></a>注解

此元素提供的数据流由 [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) 和 [TimeWindow 元素](timewindow.md) 定义。 [TimeWindow](timewindow.md)元素定义查询可用性的时间跨度。 [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义如何将 [TimeWindow](timewindow.md)元素的时间分解为 **MergedFreeBusy** 元素中返回的时间间隔。 **MergedFreeBusy** 流中的每个数字代表 [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义的单个间隔。 下表列出了单个间隔的可能值。 
  
|**数字**|**可用性**|
|:-----|:-----|
|0  <br/> |空闲  <br/> |
|1  <br/> |暂定  <br/> |
|2  <br/> |忙碌  <br/> |
|3  <br/> |外出 (OOF)  <br/> |
|4   <br/> |无数据  <br/> |
   
例如，对忙/闲数据的请求包括一个表示四小时的 [TimeWindow](timewindow.md) 元素和一个表示 60 分钟的 [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) 元素。 如果请求的用户的日历是前 60 分钟的 OOF，忙碌了 90 分钟，在时间窗口的最后 90 分钟内未计划， **则 MergedFreeBusy** 流将为 3220。 如果一个间隔包含多个可用性分类，则使用最高的数字来分类该间隔。 
  
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

