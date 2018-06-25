---
title: GetClientAccessTokenResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45ca2500-ceab-4c98-9576-cb9e158e5896
description: GetClientAccessTokenResponseMessage 元素指定 GetClientAccessToken 请求的响应消息。
ms.openlocfilehash: 16fe684dd48f77156ed88d02a6ae7b8f3312cd87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754482"
---
# <a name="getclientaccesstokenresponsemessage"></a>GetClientAccessTokenResponseMessage

**GetClientAccessTokenResponseMessage**元素指定**GetClientAccessToken**请求的响应消息。 
  
```XML
<GetClientAccessTokenResponseMessage ResponseClass=" Success | Warning | Error ">
    <Token/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetClientAccessTokenResponseMessage>
```

 **GetClientAccessTokenResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

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

|**元素**|**说明**|
|:-----|:-----|
|[令牌 (ClientAccessTokenType)](token-clientaccesstokentype.md) <br/> |指定客户端访问令牌。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，保留以供将来使用。  <br/> |
|[MessageText](messagetext.md) <br/> |提供的响应状态的文本说明。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供了其他错误响应信息。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供有关请求的状态信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含为 Exchange Web Services (EWS) 请求的响应消息。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

