---
title: GroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GroupAttendeeConflictData
api_type:
- schema
ms.assetid: fd8bf19a-298b-4135-93e8-ead3db7e1142
description: GroupAttendeeConflictData 元素包含有关可用用户数、发生冲突的用户数和在建议的会议时间通讯组列表中没有可用性信息的用户数的聚合冲突信息。
ms.openlocfilehash: 19ac366da5ad48cbc6c9e2aaa710a8c5f00e1151
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519553"
---
# <a name="groupattendeeconflictdata"></a>GroupAttendeeConflictData

**GroupAttendeeConflictData** 元素包含有关可用用户数、发生冲突的用户数和在建议的会议时间通讯组列表中没有可用性信息的用户数的聚合冲突信息。 
  
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
|[NumberOfMembersAvailable](numberofmembersavailable.md) <br/> |表示可用于建议的会议时间通讯组列表成员的数量。 此元素表示其状态为 Free **的成员**。  <br/> |
|[NumberOfMembersWithConflict](numberofmemberswithconflict.md) <br/> |表示与建议的会议时间发生冲突的通讯组列表成员的数量。 此元素表示具有忙碌 **、OOF 或****暂定状态** 的成员。  <br/> |
|[NumberOfMembersWithNoData](numberofmemberswithnodata.md) <br/> |表示未发布忙/闲数据以与建议的会议时间进行比较的组的成员数。 此元素表示过大的通讯组列表的成员或具有"无 **数据"状态** 的成员。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |包含 [GetUserAvailability](getuseravailability-operation.md)操作中标识的已查询与会者的冲突数据数组。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>注解

当 [GetUserAvailabilityRequest](getuseravailabilityrequest.md)中的参与者解析为通讯组列表时，响应中将显示 **GroupAttendeeConflictData** 元素。 **GroupAttendeeConflictData** 元素标识通讯组列表成员的三种状态：可用、冲突或无数据。 通讯组列表扩展最多支持 100 个成员。 因此 [，NumberOfMembers](numberofmembers.md) 元素最多可包含 100 个成员。 通讯组列表扩展是递归的。 如果通讯组列表包含的子通讯组列表将总父成员身份扩展到超过 100 个成员，则子通讯组列表将不会展开，并且将算作 [NumberOfMembersWithNoData](numberofmemberswithnodata.md) 元素计数的单个条目。 如果可以展开子通讯组列表，并且父成员总数没有扩展到超过 100 个成员，则扩展其成员身份，并且成员计数将添加到 **GroupAttendeeConflictData** 元素的子元素中。 
  
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

