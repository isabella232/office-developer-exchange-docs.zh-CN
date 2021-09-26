---
title: DisableAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 11ebe618-d759-4f16-be99-eaaa817ba782
description: DisableAppResponse 元素指定对 DisableApp 请求的响应。
ms.openlocfilehash: ee1558dc51a0453b609d595d37a673e9f903ff79
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545298"
---
# <a name="disableappresponse"></a>DisableAppResponse

**DisableAppResponse** 元素指定对 **DisableApp 请求** 的响应。 
  
```XML
<DisableAppResponse>
    <MessageText></MessageText>
    <ResponseCode></ResponeCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</DisableAppResponse>
```

 **DisableAppResponseType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供有关请求的状态信息。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，保留以供将来使用。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

