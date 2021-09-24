---
title: AttendeeConflictDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttendeeConflictDataArray
api_type:
- schema
ms.assetid: 1d758547-28c5-4649-8334-427480c282d6
description: AttendeeConflictDataArray 元素包含在 GetUserAvailability 操作中标识的已查询与会者的冲突数据数组。
ms.openlocfilehash: 1054fba62c7e0746a13471433d6d619a304ff848
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524356"
---
# <a name="attendeeconflictdataarray"></a>AttendeeConflictDataArray

**AttendeeConflictDataArray** 元素包含在 [GetUserAvailability](getuseravailability-operation.md)操作中标识的已查询与会者的冲突数据数组。
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
- [SuggestionsResponse](suggestionsresponse.md)
  
- [SuggestionDayResultArray](suggestiondayresultarray.md)
  
- [SuggestionDayResult](suggestiondayresult.md)
  
- [SuggestionArray](suggestionarray.md)
  
- [建议](suggestion.md)
  
- [AttendeeConflictDataArray](attendeeconflictdataarray.md)
  
```xml
<ArrayOfAttendeeConflictData>
   <UnknownAttendeeConflictData>...</UnknownAttendeeConflictData>
   <IndividualAttendeeConflictData>...</IndividualAttendeeConflictData>
   <TooBigGroupAttendeeConflictData>...</TooBigGroupAttendeeConflictData>
   <GroupAttendeeConflictData>...</GroupAttendeeConflictData>
</ArrayOfAttendeeConflictData>
```

 **ArrayOfAttendeeConflictData**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UnknownAttendeeConflictData](unknownattendeeconflictdata.md) <br/> |代表无法解析的与会者或不是用户、通讯组列表或联系人的与会者。  <br/> |
|[IndividualAttendeeConflictData](individualattendeeconflictdata.md) <br/> |包含与 [Suggestion](suggestion.md) 元素中标识的建议会议时间同时发生的时间窗口的用户或联系人的忙/闲状态。  <br/> |
|[TooBigGroupAttendeeConflictData](toobiggroupattendeeconflictdata.md) <br/> |表示作为通讯组列表解析为太大而展开的与会者。  <br/> |
|[GroupAttendeeConflictData](groupattendeeconflictdata.md) <br/> |包含有关可用用户数、发生冲突的用户数和在建议的会议时间通讯组列表中没有可用性信息的用户数的聚合冲突信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[建议](suggestion.md) <br/> |表示单个会议时间建议。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a>注解

**AttendeeConflictDataArray** 中每个元素的位置对应于被查询的与会者在 [MailboxDataArray](mailboxdataarray.md)元素中的位置。 每个查询的与会者都必须对应于 **AttendeeConflictDataArray 子** 元素之一。 这些元素表示与 Suggestion 元素中标识的建议会议 [时间存在单个](suggestion.md) 冲突。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md) 
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

