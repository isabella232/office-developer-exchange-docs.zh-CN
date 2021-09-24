---
title: Suggestion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Suggestion
api_type:
- schema
ms.assetid: 040a5c8f-b62f-4d1d-9d2c-dc3c5e01481f
description: Suggestion 元素表示单个会议建议。
ms.openlocfilehash: 8fe9500e0a822fc635e9c57c48d1778509963244
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524439"
---
# <a name="suggestion"></a>Suggestion

Suggestion 元素表示单个会议建议。 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
[SuggestionDayResultArray](suggestiondayresultarray.md)
  
[SuggestionDayResult](suggestiondayresult.md)
  
[SuggestionArray](suggestionarray.md)
  
[建议](suggestion.md)
  
```xml
<Suggestion>
   <MeetingTime>...</MeetingTime>
   <IsWorkTime>...</IsWorkTime>
   <SuggestionQuality>...</SuggestionQuality>
   <AttendeeConflictDataArray>...</AttendeeConflictDataArray>
</Suggestion>
```

 **建议**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MeetingTime](meetingtime.md) <br/> |表示建议的会议时间。  <br/> |
|[IsWorkTime](isworktime.md) <br/> |表示建议的会议时间是否发生在计划的工作时间。  <br/> |
|[SuggestionQuality](suggestionquality.md) <br/> |表示建议的会议时间的质量。  <br/> |
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |包含描述用户和资源之间冲突以及建议的会议时间的信息数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SuggestionArray](suggestionarray.md) <br/> |包含建议的会议时间数组。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray` <br/> |
   
## <a name="remarks"></a>说明

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

