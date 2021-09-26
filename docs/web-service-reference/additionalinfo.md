---
title: AdditionalInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 50bebbab-2fef-4a27-a5a9-32d7200820b6
description: AdditionalInfo 元素指定有关邮箱的保留状态的其他信息。
ms.openlocfilehash: d8b707fb04ffe91d5c7aa793c6b56c8bb048f160
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544316"
---
# <a name="additionalinfo"></a>AdditionalInfo

**AdditionalInfo** 元素指定有关邮箱的保留状态的其他信息。 
  
```XML
<AdditionalInfo></AdditionalInfo>
```

 **xs：string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MailboxHoldStatus](mailboxholdstatus.md) <br/> |指定邮箱的保留状态。  <br/> |
|[NonIndexableItemDetail](nonindexableitemdetail.md) <br/> |指定无法编制索引的项目的详细信息。  <br/> |
   
## <a name="text-value"></a>文本值

AdditionalInfo 元素的文本值是有关邮箱的保留状态的其他信息。
  
## <a name="remarks"></a>说明

此元素为可选。
  
Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

