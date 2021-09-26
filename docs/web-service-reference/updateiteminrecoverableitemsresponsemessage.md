---
title: UpdateItemInRecoverableItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 96259756-322e-4c24-ac76-0cd9c32e0d6d
description: UpdateItemInRecoverableItemsResponseMessage 元素指定对 UpdateItemInRecoverableItems 请求的响应。
ms.openlocfilehash: 10112245b27acd736d7985b5cd46944486c7e006
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542776"
---
# <a name="updateiteminrecoverableitemsresponsemessage"></a>UpdateItemInRecoverableItemsResponseMessage

**UpdateItemInRecoverableItemsResponseMessage** 元素指定 **对 UpdateItemInRecoverableItems** 请求的响应。 
  
```XML
<UpdateItemInRecoverableItemsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKet/>
   <MessageXml/>
   <Items/>
   <Attachments/>
   <ConflictResults/>
</UpdateItemInRecoverableItemsResponseMessage>
```

 **UpdateItemInRecoverableItemsResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [Items](items.md)  | [附件](attachments-ex15websvcsotherref.md)  | [ConflictResults](conflictresults.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Message.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

