---
title: HiddenRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HiddenRecipient
api_type:
- schema
ms.assetid: a8209f75-0070-4424-8dcd-273cfd192728
description: HiddenRecipient 元素指示收件人是由应对非特权用户隐藏的组织策略添加的。
ms.openlocfilehash: bfe57fabc02ff00c801672b71ccdb0bf1b916bd9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457639"
---
# <a name="hiddenrecipient"></a>HiddenRecipient

**HiddenRecipient**元素指示收件人是由应对非特权用户隐藏的组织策略添加的。 
  
```XML
<HiddenRecipient>true | false</HiddenRecipient>
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
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |包含收件人的单个事件的信息。  <br/> |
   
## <a name="text-value"></a>文本值

此元素可以是**true** ，也可以是**false**。 **如果值为 true** ，则表示用户是由组织策略添加的;**如果值为 false** ，则表示组织策略未添加用户。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

