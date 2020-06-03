---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: ConnectionFailureCause 元素指定从电话呼叫断开连接的原因。
ms.openlocfilehash: 6385641eaee140a114906703232974d51d5ce344
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529446"
---
# <a name="connectionfailurecause"></a>ConnectionFailureCause

**ConnectionFailureCause**元素指定从电话呼叫断开连接的原因。 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 **ConnectionFailureCauseType**
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

下表列出了**ConnectionFailureCause**元素的可能值。 
  
**ConnectionFailureCause 元素值**

|**值**|**说明**|
|:-----|:-----|
|无  <br/> |呼叫状态不会断开连接，或者断开连接的原因未知。  <br/> |
|UserBusy  <br/> |呼叫方线路正忙。  <br/> |
|NoAnswer  <br/> |被叫方没有应答。  <br/> |
|才  <br/> |被叫方号码不可用。  <br/> |
|其他  <br/> |捕捉-all 用于其他断开连接的原因。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

