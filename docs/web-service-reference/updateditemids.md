---
title: UpdatedItemIds
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: UpdatedItemIds 元素指定更新的提醒项目的标识符。
ms.openlocfilehash: b95ebb20823706e68b1fd66dc64f756808bb7375
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838371"
---
# <a name="updateditemids"></a>UpdatedItemIds

**UpdatedItemIds**元素指定更新的提醒项目的标识符。 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 **NonEmptyArrayOfItemIdsType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

[ItemId](itemid.md)
  
### <a name="parent-elements"></a>父元素

[PerformReminderActionResponse](performreminderactionresponse.md)
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
如果[PerformReminderAction](performreminderaction-operation.md)操作未成功完成或未在服务器上进行任何更改，则为空值返回**UpdatedItemIds**元素。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[PerformReminderActionResponse](performreminderactionresponse.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

