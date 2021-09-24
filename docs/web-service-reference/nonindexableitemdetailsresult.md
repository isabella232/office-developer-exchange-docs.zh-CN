---
title: NonIndexableItemDetailsResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7cbdbc21-5405-4cbc-8ca0-d7b0257927aa
description: NonIndexableItemDetailsResult 元素指定 GetNonIndexableItemDetails WSDL 操作的结果。
ms.openlocfilehash: 16f3c8a74f635fdd8204fe207777b4b30bc4d2ed
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539279"
---
# <a name="nonindexableitemdetailsresult"></a>NonIndexableItemDetailsResult

**NonIndexableItemDetailsResult** 元素指定 **GetNonIndexableItemDetails** WSDL 操作的结果。 
  
```XML
<NonIndexableItemDetailsResult>
   <Items/>
   <FailedMailboxes/>
</NonIndexableItemDetailsResult>
```

 **NonIndexableItemDetailResultType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ArrayOfNonIndexableItemDetailsType](items-arrayofnonindexableitemdetailstype.md) ([、FailedMailboxes](failedmailboxes.md)) 项
  
### <a name="parent-elements"></a>父元素

[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) [、GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetNonIndexableItemDetails 操作](getnonindexableitemdetails-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

