---
title: HasLocationChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fd465b4-6070-4cd0-9ac3-ed9d2bfd5951
description: HasLocationChanged 元素指定会议的 location 属性是否已更改。
ms.openlocfilehash: 4f774adcf4a7666f40524931504f1172e15ba24d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462442"
---
# <a name="haslocationchanged"></a>HasLocationChanged

**HasLocationChanged**元素指定会议的 location 属性是否已更改。 
  
```XML
<HasLocationChanged> true | false </HasLocationChanged>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ChangeHighlights](changehighlights.md) <br/> |指定会议请求邮件的两个版本之间的变化。  <br/> |
   
## <a name="text-value"></a>文本值

如果**HasLocationChanged**元素的文本值为**true** ，则表示会议的 location 属性已更改。 值**为 false**表示会议的 location 属性未发生更改。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |类型 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

