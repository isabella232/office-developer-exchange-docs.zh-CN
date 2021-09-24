---
title: UpdatedItemIds
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: UpdatedItemIds 元素指定更新的提醒项的标识符。
ms.openlocfilehash: 59e17e32d5df3f8a6000b05899f2fe0c5de2ec00
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538609"
---
# <a name="updateditemids"></a>UpdatedItemIds

**UpdatedItemIds** 元素指定更新的提醒项的标识符。 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 **NonEmptyArrayOfItemIdsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ItemId](itemid.md)
  
### <a name="parent-elements"></a>父元素

[PerformReminderActionResponse](performreminderactionresponse.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
如果 [PerformReminderAction](performreminderaction-operation.md) 操作未成功完成，或者服务器上没有进行更改， **则 UpdatedItemIds** 元素将返回为空值。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[PerformReminderActionResponse](performreminderactionresponse.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

