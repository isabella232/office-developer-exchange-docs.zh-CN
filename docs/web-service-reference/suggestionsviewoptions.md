---
title: SuggestionsViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: SuggestionsViewOptions 元素包含选项的获取会议建议信息。
ms.openlocfilehash: 09ff317ae0b2ebf1eadc89dc3bb1cf5b3ae19dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838163"
---
# <a name="suggestionsviewoptions"></a>SuggestionsViewOptions

**SuggestionsViewOptions**元素包含选项的获取会议建议信息。 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
```xml
<SuggestionsViewOptions>
   <GoodThreshold>...</GoodThreshold>
   <MaximumResultsByDay>...</MaximumResultsByDay>
   <MaximumNonWorkingHourResultsByDay>...</MaximumNonWorkingHourResultsByDay>
   <MeetingDurationInMinutes>...</MeetingDurationInMinutes>
   <MinimumSuggestionQuality>...</MinimumSuggestionQuality>
   <SuggestionIntervalInMinutes>...</SuggestionIntervalInMinutes>
   <DetailedSuggestionsWindow>...</DetailedSuggestionsWindow>
   <CurrentMeetingTime>...</CurrentMeetingTime>
   <GlobalObjectId>...</GlobalObjectId>
</SuggestionsViewOptions>
```

 **SuggestionsViewOptionsType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[GoodThreshold](goodthreshold.md) <br/> |指定必须打开若要成为合格的良好建议的会议时间的时间段的时间段的与会者的百分比。  <br/> |
|[MaximumResultsByDay](maximumresultsbyday.md) <br/> |指定的每日响应中返回的建议的会议次数。  <br/> |
|[MaximumNonWorkHourResultsByDay](maximumnonworkhourresultsbyday.md) <br/> |指定建议的会议时间每天的正常工作时间以外的结果数。  <br/> |
|[MeetingDurationInMinutes](meetingdurationinminutes.md) <br/> |指定建议会议的时间长度。  <br/> |
|[MinimumSuggestionQuality](minimumsuggestionquality.md) <br/> |指定会议建议的响应中返回的质量。  <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |标识查询建议的会议时间有关的详细信息的时间跨度。  <br/> |
|[CurrentMeetingTime](currentmeetingtime.md) <br/> |代表要更新与建议会议的会议的开始时间的时间结果。  <br/> |
|[GlobalObjectId](globalobjectid.md) <br/> |不使用此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |包含用于获取用户的可用性信息的参数。 这是根元素。  <br/> 以下是此元素的 XPath:  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a>备注

此元素不需要，并且如果使用可以只发生一次。 如果[FreeBusyViewOptions](freebusyviewoptions.md)元素的值不为 null，则此值可以是 null。 
  
> [!NOTE]
> 描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。 
  
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

