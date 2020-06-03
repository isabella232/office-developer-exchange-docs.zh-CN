---
title: GetAppMarketplaceUrlResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc3368ec-78c2-4f8d-8394-4891e90dafd2
description: GetAppMarketplaceUrlResponse 元素指定对 GetAppMarketplaceUrl 请求的响应。
ms.openlocfilehash: 7ff000908a2f73f41575cae8a7795644dd60565d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530851"
---
# <a name="getappmarketplaceurlresponse"></a>GetAppMarketplaceUrlResponse

**GetAppMarketplaceUrlResponse**元素指定对**GetAppMarketplaceUrl**请求的响应。 
  
```XML
<GetAppMarketplaceUrlResponse ResponseClass=" Success | Warning | Error ">
    <AppMarketplaceUrl/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppMarketplaceUrlResponse>
```

 **GetAppMarketplaceUrlResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|ResponseClass  <br/> |指示响应的类。  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**值**|**说明**|
|:-----|:-----|
|成功  <br/> |指示成功。  <br/> |
|警告  <br/> |指示警告。  <br/> |
|错误  <br/> |指示错误。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[AppMarketplaceUrl](appmarketplaceurl.md) <br/> |指定应用程序的 URL。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，并已保留以供将来使用。  <br/> |
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供有关请求的状态信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含 Exchange Web 服务请求的响应消息。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |消息 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

