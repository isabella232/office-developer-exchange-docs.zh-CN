---
title: SearchMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f1bcbfb-d7f6-4fa0-b6f8-681a0b067007
description: SearchMailboxesResponseMessage 元素指定 SearchMailboxes 请求的响应消息。
ms.openlocfilehash: 342223b9a8cc7e91b97d637cb104f7bb160b7d5a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44448420"
---
# <a name="searchmailboxesresponsemessage"></a>SearchMailboxesResponseMessage

**SearchMailboxesResponseMessage**元素指定**SearchMailboxes**请求的响应消息。 
  
```XML
<SearchMailboxesResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SearchMailboxesResult/>
</SearchMailboxesResponseMessage>
```

 **SearchMailboxesResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [SearchMailboxesResult](searchmailboxesresult.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

