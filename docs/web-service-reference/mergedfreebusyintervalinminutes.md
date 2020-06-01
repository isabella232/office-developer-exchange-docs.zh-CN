---
title: MergedFreeBusyIntervalInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusyIntervalInMinutes
api_type:
- schema
ms.assetid: 481cdbc6-d5aa-49fa-a3fa-9d119d3dca99
description: MergedFreeBusyIntervalInMinutes 元素表示 FreeBusyMerged 视图中两个连续的插槽之间的时间差。
ms.openlocfilehash: 6228ee5b66202634e6bb3b6c1ad6b8897a109d58
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468787"
---
# <a name="mergedfreebusyintervalinminutes"></a>MergedFreeBusyIntervalInMinutes

**MergedFreeBusyIntervalInMinutes**元素表示**FreeBusyMerged**视图中两个连续的插槽之间的时间差。 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)
  
```xml
<MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |指定响应中返回的忙/闲信息的类型。  <br/> 以下是此元素的 XPath：  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 该文本值表示以分钟为单位的时间。 默认值为 30 分钟。 6分钟是最小时间间隔，一天（1440分钟）是此元素的最大时间间隔。
  
## <a name="remarks"></a>备注

仅当[RequestedView](requestedview.md)元素等于**MergedOnly**、 **FreeBusyMerged**或**DetailedMerge**时，才使用此值。 这是 integer 数据类型。 包含此元素定义的间隔的流在[MergedFreeBusy](mergedfreebusy.md)元素中返回。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserAvailability 操作](getuseravailability-operation.md)
  
[GetUserOofSettings 操作](getuseroofsettings-operation.md)


[Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

