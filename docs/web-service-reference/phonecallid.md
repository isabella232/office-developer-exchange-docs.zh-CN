---
title: PhoneCallId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PhoneCallId
api_type:
- schema
ms.assetid: 79e31a4c-fc84-4802-8761-470df8d63694
description: PhoneCallId 元素指定电话呼叫的标识符。 此元素是必需的。
ms.openlocfilehash: 00b23c8b4023a6fef9c27295c8e023e5324b7026
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528317"
---
# <a name="phonecallid"></a>PhoneCallId

**PhoneCallId** 元素指定电话呼叫的标识符。 此元素是必需的。 
  
```xml
<PhoneCallId Id="" />
```

 **PhoneCallIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |标识要断开连接的电话呼叫。 此特性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DisconnectPhoneCall](disconnectphonecall.md) <br/> |表示断开呼叫连接的请求。  <br/> |
|[GetPhoneCallInformation](getphonecallinformation.md) <br/> |表示获取电话呼叫信息的请求。  <br/> |
|[PlayOnPhoneResponse (Exchange Web 服务) ](playonphoneresponse-exchange-web-services.md) <br/> |定义对 PlayOnPhone 请求的响应。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行 Microsoft Exchange Server 2010（已安装客户端访问服务器角色）的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

