---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: DisableReason 元素指定禁用应用的原因。
ms.openlocfilehash: 8156dac17e81dd1c3f49575491924185b04d53e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528834"
---
# <a name="disablereason"></a>DisableReason

**DisableReason** 元素指定禁用应用的原因。 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 **DisableReasonType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DisableApp](disableapp.md) <br/> |指定禁用应用的请求。  <br/> |
   
## <a name="text-value"></a>文本值

**DisableReason 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|NoReason  <br/> |无原因给定  <br/> |
|OutlookClientPerformance  <br/> |提高电子邮件客户端性能。  <br/> |
|OWAClientPerformance  <br/> |提高 Web 应用客户端性能。  <br/> |
|MobileClientPerformance  <br/> |提高移动客户端性能。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

