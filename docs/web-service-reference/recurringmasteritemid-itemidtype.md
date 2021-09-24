---
title: RecurringMasterItemId (ItemIdType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: RecurringMasterItemId (ItemIdType) 元素通过标识定期主项目的相关项目之一的标识符来标识定期主项目。
ms.openlocfilehash: 491bb6686ad6cc9ee8169144b659d828e3920e45
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522738"
---
# <a name="recurringmasteritemid-itemidtype"></a>RecurringMasterItemId (ItemIdType)

**RecurringMasterItemId (ItemIdType**) 元素通过标识其某个相关项的标识符来标识定期主项目。 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

****

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |标识定期主项目的单个匹配项。 此特性是必需的。  <br/> |
|ChangeKey  <br/> |标识定期主项目的单个匹配项的特定版本。 此外，还标识了定期主项目，因为它和单个项目将包含相同的更改键。 此特性是可选的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[提醒](reminder.md)
  
## <a name="remarks"></a>说明

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[提醒](reminder.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

