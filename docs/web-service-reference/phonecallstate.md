---
title: PhoneCallState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PhoneCallState
api_type:
- schema
ms.assetid: ac009eb3-6334-49ce-82be-48fe83577f9c
description: PhoneCallState 元素指定电话呼叫的当前状态。
ms.openlocfilehash: 8c0b8357b58826f18f05eb0fedc0865be1623c2b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528300"
---
# <a name="phonecallstate"></a>PhoneCallState

**PhoneCallState** 元素指定电话呼叫的当前状态。 
  
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

|**元素**|**说明**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |指定电话呼叫的状态信息。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了 **PhoneCallState** 元素的可能值。 
  
**PhoneCallState 元素值**

|**值**|**说明**|
|:-----|:-----|
|空闲  <br/> |初始呼叫状态。  <br/> |
|正在连接  <br/> |系统正在拨打此呼叫。  <br/> |
|警报  <br/> |呼叫在电话响铃时 (警报) 。  <br/> |
|已连接  <br/> |呼叫已连接。  <br/> |
|已断开连接  <br/> |呼叫已断开连接。  <br/> |
|传入  <br/> |呼叫是入站呼叫。  <br/> |
|正在转移  <br/> |正在将呼叫转接到另一个目标。  <br/> |
|转发  <br/> |呼叫正在被转发到另一个目标。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 /ews/ 目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

