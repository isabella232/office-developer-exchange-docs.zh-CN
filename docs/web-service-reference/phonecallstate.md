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
description: PhoneCallState 元素指定的电话呼叫的当前状态。
ms.openlocfilehash: 184a7400810711442e565d1ef37094bd63b00914
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826761"
---
# <a name="phonecallstate"></a>PhoneCallState

**PhoneCallState**元素指定的电话呼叫的当前状态。 
  
```xml
<PhoneCallState>Idle or Connecting or Alerted or Connected or Disconnected or Incoming or Transferring or Forwarding</PhoneCallState>
```

 **PhoneCallStateType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PhoneCallInformation](phonecallinformation.md) <br/> |指定的电话的状态信息。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**PhoneCallState**元素的可能值。 
  
**PhoneCallState 元素的值**

|**值**|**说明**|
|:-----|:-----|
|空闲时间  <br/> |初始呼叫状态。  <br/> |
|正在连接  <br/> |系统为拨打此呼叫。  <br/> |
|收到通知  <br/> |警报状态正在呼叫 （电话响铃）。  <br/> |
|已连接  <br/> |呼叫处于连接状态。  <br/> |
|已断开连接  <br/> |将断开呼叫。  <br/> |
|传入  <br/> |入站呼叫。  <br/> |
|转接  <br/> |呼叫被转接至其他目标。  <br/> |
|转接  <br/> |是要将呼叫转接至其他目标。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 /ews/ 目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

