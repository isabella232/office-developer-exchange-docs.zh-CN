---
title: AllowNewTimeProposal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowNewTimeProposal
api_type:
- schema
ms.assetid: afdb4ec9-2daf-48a1-a0bb-a7f647f212f2
description: AllowNewTimeProposal 元素指示与会者是否可以为会议建议新会议时间。
ms.openlocfilehash: b3f2c569bced08c66144680a4fddd6e8bac0cecf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464803"
---
# <a name="allownewtimeproposal"></a>AllowNewTimeProposal

**AllowNewTimeProposal**元素指示与会者是否可以为会议建议新会议时间。 
  
```xml
<AllowNewTimeProposal/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
   
## <a name="text-value"></a>文本值

表示一个布尔值的文本值是必需的。 **True**的值表示可以创建会议时间的新建议;**如果值为 false** ，则表示不允许新的时间建议。 组织者在会议请求中设置此值。 
  
## <a name="remarks"></a>备注

对于组织者的日历项目，AllowNewTimeProposal 属性是可读写的。 对于会议请求和与会者的日历项目，它是只读的。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
> [!NOTE]
> Exchange Web 服务不支持新的时间建议消息。 若要获取与新的时间建议邮件相关的属性，请使用扩展属性。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

