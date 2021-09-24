---
title: LegacyFreeBusyStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- LegacyFreeBusyStatus
api_type:
- schema
ms.assetid: ee5f3046-b79f-4f68-9455-1a688cee2745
description: LegacyFreeBusyStatus 元素表示日历项目的忙/闲状态。
ms.openlocfilehash: 6bdfca41cd6f0d9304285e1101b6ecc14e2b761e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524894"
---
# <a name="legacyfreebusystatus"></a>LegacyFreeBusyStatus

**LegacyFreeBusyStatus** 元素表示日历项目的忙/闲状态。 
  
```xml
<LegacyFreeBusyStatus/>
```

**LegacyFreeBusyType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
   
## <a name="text-value"></a>文本值

此元素需要文本值。 以下是此元素的可能文本值：
  
- 空闲 
- 暂定
- 忙碌
- OOF
- WorkingElsewhere
- NoData
    
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

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

