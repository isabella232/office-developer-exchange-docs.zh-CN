---
title: ArchiveItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2ac58d6f-e019-4352-b82f-8ac67a171e63
description: ArchiveItemResponseMessage 元素指定对 ArchiveItem 请求的响应邮件。
ms.openlocfilehash: c0d816039ea0ab9d69d04d979a9dad973e4278b8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525258"
---
# <a name="archiveitemresponsemessage"></a>ArchiveItemResponseMessage

**ArchiveItemResponseMessage** 元素指定对 **ArchiveItem** 请求的响应邮件。 
  
```XML
<ArchiveItemResponseMessage ResponseClass="">
    <MessageText></MessageText>
    <ResponseCode></ResponseCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
    <Items></Items>
</ArchiveItemResponseMessage>
```

 **ItemInfoResponseMessageType**
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

|**元素**|**说明**|
|:-----|:-----|
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，保留以供将来使用。  <br/> |
|[Items](items.md) <br/> |包含项目数组。  <br/> |
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供有关请求的状态信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |包含 Web 服务请求Exchange消息。  <br/> |
   
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

