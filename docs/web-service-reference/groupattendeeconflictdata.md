---
title: GroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupAttendeeConflictData
api_type:
- schema
ms.assetid: fd8bf19a-298b-4135-93e8-ead3db7e1142
description: GroupAttendeeConflictData 元素包含聚合冲突信息均可用、 存在冲突，用户数量和分布中没有可用性信息的用户数列出的用户数量建议的会议时间。
ms.openlocfilehash: 382b4d866c95de98bd444cd6226d71813889d4f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825757"
---
# <a name="groupattendeeconflictdata"></a>GroupAttendeeConflictData

**GroupAttendeeConflictData**元素包含聚合冲突有关可用的用户数、 用户拥有冲突，数和通讯组列表中没有可用性信息的用户数在建议的会议的时间。 
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [SuggestionsResponse](suggestionsresponse.md)
- [SuggestionDayResultArray](suggestiondayresultarray.md)
- [SuggestionDayResult](suggestiondayresult.md)
- [SuggestionArray](suggestionarray.md)
- [建议](suggestion.md)
- [AttendeeConflictDataArray](attendeeconflictdataarray.md)
- [GroupAttendeeConflictData](groupattendeeconflictdata.md)
  
```xml
<GroupAttendeeConflictData>
   <NumberOfMembers>...</NumberOfMembers>
   <NumberOfMembersAvailable>...</NumberOfMembersAvailable>
   <NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
   <NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
</GroupAttendeeConflictData>
```

**GroupAttendeeConflictData**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[NumberOfMembers](numberofmembers.md) <br/> |代表用户、 资源和通讯组列表中的聊天室的数量。  <br/> |
|[NumberOfMembersAvailable](numberofmembersavailable.md) <br/> |代表建议的会议的时间可用的通讯组列表成员的数量。 此元素表示为其状态是**免费**的成员。  <br/> |
|[NumberOfMembersWithConflict](numberofmemberswithconflict.md) <br/> |代表拥有建议的会议时间冲突的通讯组列表成员的数量。 此元素表示具有**忙碌**、 **OOF**，或**暂定**状态的成员。  <br/> |
|[NumberOfMembersWithNoData](numberofmemberswithnodata.md) <br/> |表示没有已发布忙/闲数据到建议的会议的时间比较组成员的数目。 此元素表示太大通讯组列表的成员或拥有**无数据**状态的成员。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |包含标识[GetUserAvailability 操作](getuseravailability-operation.md)中的查询与会者冲突数据的数组。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>注解

[GetUserAvailabilityRequest](getuseravailabilityrequest.md)中的与会者解析为通讯组列表时，可以在响应中存在的**GroupAttendeeConflictData**元素。 **GroupAttendeeConflictData**元素标识三种状态的通讯组列表的成员： 可用、 冲突，或没有数据。 通讯组列表扩展将支持多达 100 个成员。 因此， [NumberOfMembers](numberofmembers.md)元素可以包含 100 个成员的最大值。 通讯组列表扩展是递归。 如果通讯组列表中包含子通讯组列表扩展到超过 100 个成员的总父成员资格，子通讯组列表不会被展开，并将计数为一个条目的[NumberOfMembersWithNoData](numberofmemberswithnodata.md)元素计数。 如果可以展开子通讯组列表，并且总父成员资格不会展开到超过 100 个成员，扩展其成员资格和成员计数添加到**GroupAttendeeConflictData**元素的子元素。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

