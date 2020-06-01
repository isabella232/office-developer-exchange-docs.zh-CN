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
description: GroupAttendeeConflictData 元素包含有关可用用户数的聚合冲突信息、有冲突的用户数以及在通讯组列表中没有可用性信息的用户数，以获取建议的会议时间。
ms.openlocfilehash: c75a4e6f8fdff7fb2514f448350fee9f1acb9775
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462927"
---
# <a name="groupattendeeconflictdata"></a>GroupAttendeeConflictData

**GroupAttendeeConflictData**元素包含有关可用用户数的聚合冲突信息、有冲突的用户数以及在通讯组列表中没有可用性信息的用户数，以获取建议的会议时间。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[NumberOfMembers](numberofmembers.md) <br/> |表示通讯组列表中的用户、资源和会议室的数量。  <br/> |
|[NumberOfMembersAvailable](numberofmembersavailable.md) <br/> |表示可用于建议会议时间的通讯组列表成员的数量。 此元素表示其状态为 "**空闲**" 的成员。  <br/> |
|[NumberOfMembersWithConflict](numberofmemberswithconflict.md) <br/> |表示与建议的会议时间有冲突的通讯组列表成员的数量。 此元素表示具有 "**忙碌**"、" **OOF**" 或 "**暂定**" 状态的成员。  <br/> |
|[NumberOfMembersWithNoData](numberofmemberswithnodata.md) <br/> |表示没有发布的忙/闲数据以与建议的会议时间进行比较的组成员的数量。 此元素表示通讯组列表的成员过大或没有**数据**状态的成员。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |包含在[GetUserAvailability 操作](getuseravailability-operation.md)中标识的被查询的与会者的冲突数据数组。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>备注

将[GetUserAvailabilityRequest](getuseravailabilityrequest.md)中的与会者解析为通讯组列表时，响应中存在**GroupAttendeeConflictData**元素。 **GroupAttendeeConflictData**元素标识通讯组列表成员的三种状态：可用、冲突或无数据。 通讯组列表扩展将最长支持100个成员。 因此， [NumberOfMembers](numberofmembers.md)元素最多可包含100个成员。 通讯组列表展开是递归的。 如果通讯组列表包含将总父成员资格扩展到超过100个成员的子通讯组列表，则子通讯组列表将不会展开，并将作为[NumberOfMembersWithNoData](numberofmemberswithnodata.md)元素计数的单个条目进行计数。 如果可以扩展子通讯组列表，并且总父成员资格不会扩展到超过100个成员，则将展开其成员资格，并将成员计数添加到**GroupAttendeeConflictData**元素的子元素中。 
  
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

