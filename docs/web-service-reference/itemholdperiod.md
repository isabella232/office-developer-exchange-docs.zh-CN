---
title: ItemHoldPeriod
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30369db5-4d45-40e8-bc83-3236667fc404
description: ItemHoldPeriod 元素指定保留与邮箱查询匹配的内容的时间长度。
ms.openlocfilehash: 185666b72cc96dd88605b7baa6433d070e7ebc91
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452284"
---
# <a name="itemholdperiod"></a>ItemHoldPeriod

**ItemHoldPeriod**元素指定保留与邮箱查询匹配的内容的时间长度。 
  
```XML
<ItemHoldPeriod/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[SetHoldOnMailboxes](setholdonmailboxes.md)
  
## <a name="text-value"></a>文本值

文本值可以是 "无限制"，也可以是任何[Timespan](https://msdn.microsoft.com/library/1ecy8h51%28v=vs.110%29.aspx)值的字符串值。 
  
## <a name="remarks"></a>说明

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[SetHoldOnMailboxes](setholdonmailboxes.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

