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
ms.openlocfilehash: 7269587e2fa72aeb9070a7b53ee9215829729329
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826432"
---
# <a name="meetingrequesttype"></a>MeetingRequestType

**MeetingRequestType**元素描述会议请求的类型。 
  
```xml
<MeetingRequestType/>
```

 **MeetingRequestTypeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 下表列出了此元素的可能的文本值。
  
|**值**|**说明**|
|:-----|:-----|
|FullUpdate  <br/> |标识为完全更新现有请求的会议请求。 完全更新具有更新时间和信息性内容。  <br/> |
|InformationalUpdate  <br/> |标识会议请求，如仅包含更新的信息性内容。  <br/> |
|NewMeetingRequest  <br/> |标识为新的会议请求的会议请求。  <br/> |
|无  <br/> |指示会议请求类型未定义。  <br/> |
|过时  <br/> |标识为过时的会议请求。  <br/> |
|PrincipalWantsCopy  <br/> |指示会议请求所属的主体用户已将会议邮件转发给代理人，并且包含标记，信息性其副本。  <br/> |
|SilentUpdate  <br/> |标识为向现有会议的无提示更新会议请求。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

