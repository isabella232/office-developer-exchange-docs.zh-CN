---
title: PhoneCallState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: PhoneCallState 元素指定电话呼叫的当前状态。
ms.openlocfilehash: d2088b9b2811befe80684188d49c8034c577cc55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468528"
---
# <a name="phonecallstate"></a>PhoneCallState

**PhoneCallState**元素指定电话呼叫的当前状态。 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 **PhoneCallStateType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |指定电话呼叫的状态信息。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**PhoneCallState**元素的可能值。 
  
**PhoneCallState 元素值**

|**值**|**说明**|
|:-----|:-----|
|待机  <br/> |初始呼叫状态。  <br/> |
|正在连接  <br/> |系统正在拨打此呼叫。  <br/> |
|收到  <br/> |呼叫处于 "警报" 状态（电话正在响铃）。  <br/> |
|已连接  <br/> |该呼叫处于 "已连接" 状态。  <br/> |
|已断开连接  <br/> |呼叫已断开连接。  <br/> |
|即将  <br/> |呼叫为入站。  <br/> |
|传输  <br/> |正在将呼叫转接到另一个目的地。  <br/> |
|发送  <br/> |将呼叫转接到另一个目的地。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的/ews/目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

