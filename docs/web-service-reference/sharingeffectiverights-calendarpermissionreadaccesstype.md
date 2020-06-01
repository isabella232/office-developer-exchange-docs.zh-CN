---
title: SharingEffectiveRights (CalendarPermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: b519f642-a9ef-4300-92e6-ed8202855fde
description: SharingEffectiveRights 元素指示用户对要共享的日历数据所具有的权限。
ms.openlocfilehash: 5581e9cc001608a124ae94e69eba836f6fd98520
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458577"
---
# <a name="sharingeffectiverights-calendarpermissionreadaccesstype"></a>SharingEffectiveRights (CalendarPermissionReadAccessType)

**SharingEffectiveRights**元素指示用户对要共享的日历数据所具有的权限。 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 **CalendarPermissionReadAccessType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |代表主要包含日历项目的文件夹。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**SharingEffectiveRights**元素的可能值。 
  
|**值**|**说明**|
|:-----|:-----|
|无  <br/> |指示用户不具有查看日历中的项目的权限。  <br/> |
|TimeOnly  <br/> |指示用户具有仅查看日历中的忙/闲时间的权限。  <br/> |
|TimeAndSubjectAndLocation  <br/> |指示用户有权查看日历中的忙/闲时间以及约会的主题和位置。  <br/> |
|FullDetails  <br/> |指示用户有权查看日历中的所有项目，包括忙/闲时间、主题、位置和约会的详细信息。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

