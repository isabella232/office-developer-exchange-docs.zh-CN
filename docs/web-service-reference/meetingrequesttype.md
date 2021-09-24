---
title: MeetingRequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: MeetingRequestType 元素描述会议请求的类型。
ms.openlocfilehash: 1a8371331691bb9dee5595b0130ec0c3c75c47c5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539372"
---
# <a name="meetingrequesttype"></a>MeetingRequestType

**MeetingRequestType** 元素描述会议请求的类型。 
  
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

|**元素**|**说明**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了此元素的可能文本值。
  
|**值**|**说明**|
|:-----|:-----|
|FullUpdate  <br/> |将会议请求标识为对现有请求的完整更新。 完整更新包含更新的时间和信息性内容。  <br/> |
|InformationalUpdate  <br/> |将会议请求标识为仅包含更新的信息内容。  <br/> |
|NewMeetingRequest  <br/> |将会议请求标识为新的会议请求。  <br/> |
|无  <br/> |指示未定义会议请求类型。  <br/> |
|过时  <br/> |将会议请求标识为过时。  <br/> |
|PrincipalWantsCopy  <br/> |指示会议请求属于一个主体，该主体已经将会议消息转发给代理人，并且其副本被标记为信息性。  <br/> |
|SilentUpdate  <br/> |将会议请求标识为对现有会议进行无提示更新。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

