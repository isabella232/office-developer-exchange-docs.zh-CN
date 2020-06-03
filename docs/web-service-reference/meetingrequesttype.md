---
title: MeetingRequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: MeetingRequestType 元素描述会议请求的类型。
ms.openlocfilehash: e90c44dd4124d698ca5ef7655f6429a7167673e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465784"
---
# <a name="meetingrequesttype"></a>MeetingRequestType

**MeetingRequestType**元素描述会议请求的类型。 
  
```xml
<MeetingRequestType/>
```

 **MeetingRequestTypeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了此元素可能的文本值。
  
|**值**|**说明**|
|:-----|:-----|
|FullUpdate  <br/> |将会议请求标识为对现有请求进行完全更新。 完全更新已更新时间和信息性内容。  <br/> |
|InformationalUpdate  <br/> |仅将会议请求标识为包含更新的信息性内容。  <br/> |
|NewMeetingRequest  <br/> |将会议请求标识为新的会议请求。  <br/> |
|无  <br/> |指示未定义会议请求类型。  <br/> |
|过期  <br/> |将会议请求标识为过期。  <br/> |
|PrincipalWantsCopy  <br/> |指示会议请求属于将会议邮件转发给代理并将其副本标记为信息的主体。  <br/> |
|SilentUpdate  <br/> |将会议请求标识为对现有会议的无提示更新。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

