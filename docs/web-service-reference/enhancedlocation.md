---
title: EnhancedLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdfb74f-f33c-46ae-a7c7-451a5b0c6a59
description: EnhancedLocation 元素指定位置信息，如名称、地址和关于某个位置的可选注释。
ms.openlocfilehash: 06ec800b763ef61af51da03ca8a340f6ac4d2a8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462955"
---
# <a name="enhancedlocation"></a>EnhancedLocation

**EnhancedLocation**元素指定位置信息，如名称、地址和关于某个位置的可选注释。 
  
```XML
<EnhancedLocation>
    <DisplayName/>
    <Annotation/>
    <PostalAddress/>
</EnhancedLocation>
```

 **EnhancedLocationType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[显示名称 (字符串)](displayname-string.md) <br/> |定义文件夹、联系人、通讯组列表、代理用户、位置或规则的显示名称。  <br/> |
|[Annotation](annotation.md) <br/> |包含用户添加的可选注释。  <br/> |
|[省略（PersonaPostalAddressType）](postaladdress-personapostaladdresstype.md) <br/> |指定角色的邮政地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |类型 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

