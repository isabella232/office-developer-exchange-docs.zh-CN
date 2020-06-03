---
title: SuggestionsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsResponse
api_type:
- schema
ms.assetid: d25ca143-f80c-4458-b669-346fda29a5a7
description: SuggestionsResponse 元素包含请求的会议建议的响应状态信息和建议数据。
ms.openlocfilehash: cba344f3f97777580c2cc6d296f110f20b550063
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466652"
---
# <a name="suggestionsresponse"></a>SuggestionsResponse

**SuggestionsResponse**元素包含请求的会议建议的响应状态信息和建议数据。 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
```xml
<SuggestionsResponse>
   <ResponseMessage>...</ResponseMessage>
   <SuggestionDayResultArray>...</SuggestionDayResultArray>
</SuggestionsResponse>
```

 **SuggestionsResponseType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> |提供有关响应状态的描述性信息。  <br/> |
|[SuggestionDayResultArray](suggestiondayresultarray.md) <br/> |包含按日期组织的会议建议的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserAvailabilityResponse](getuseravailabilityresponse.md) <br/> |包含请求的用户的可用性信息。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a>备注

如果 GetUserAvailability 请求消息中未设置[SuggestionsViewOptions](suggestionsviewoptions.md) ，则此元素不包含在 GetUserAvailability 响应中。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserAvailability 操作](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

