---
title: SuggestionsViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: SuggestionsViewOptions 元素包含用于获取会议建议信息的选项。
ms.openlocfilehash: ba3591b88e581d45c811100a53b0a74e4bb8e010
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522612"
---
# <a name="suggestionsviewoptions"></a>SuggestionsViewOptions

**SuggestionsViewOptions** 元素包含用于获取会议建议信息的选项。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[GoodThreshold](goodthreshold.md) <br/> |指定必须打开时间段才能限定为建议的会议时间与会者的百分比。  <br/> |
|[MaximumResultsByDay](maximumresultsbyday.md) <br/> |指定响应中每天返回的建议会议时间数。  <br/> |
|[MaximumNonWorkHourResultsByDay](maximumnonworkhourresultsbyday.md) <br/> |指定每天常规工作时间以外的会议时间的建议结果数。  <br/> |
|[MeetingDurationInMinutes](meetingdurationinminutes.md) <br/> |指定要建议的会议长度。  <br/> |
|[MinimumSuggestionQuality](minimumsuggestionquality.md) <br/> |指定响应中要返回的会议建议的质量。  <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |标识查询有关建议的会议时间的详细信息的时间跨度。  <br/> |
|[CurrentMeetingTime](currentmeetingtime.md) <br/> |表示您想要使用建议的会议时间结果更新的会议的开始时间。  <br/> |
|[GlobalObjectId](globalobjectid.md) <br/> |此元素未使用。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |包含用于获取用户可用性信息的参数。 这是根元素。  <br/> 下面是此元素的 XPath：  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a>注解

此元素不是必需的，如果使用，则只能出现一次。 如果 [FreeBusyViewOptions](freebusyviewoptions.md) 元素的值不为 null，则此值可能为 null。 
  
> [!NOTE]
> 描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。 
  
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

