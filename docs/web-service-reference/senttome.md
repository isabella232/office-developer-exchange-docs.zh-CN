---
title: SentToMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToMe
api_type:
- schema
ms.assetid: f18aecd1-ad33-41c3-b275-4ca648ce1da0
description: SentToMe 元素指示邮箱的所有者是否必须在传入邮件的 ToRecipients 属性中，以便条件或例外情况适用。
ms.openlocfilehash: 830125f03ad91a3e6f2beaf11e41be5e940ed48b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44439922"
---
# <a name="senttome"></a>SentToMe

**SentToMe**元素指示邮箱的所有者是否必须在传入邮件的**ToRecipients**属性中，以便条件或例外情况适用。 
  
```XML
<SentToMe>true | false</SentToMe>
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
|[条件](conditions.md) <br/> |表示履行时将触发规则的规则操作的条件。  <br/> |
|[异常](exceptions.md) <br/> |代表收件箱规则的所有可用的规则例外条件。  <br/> |
   
## <a name="text-value"></a>文本值

如果文本值为**true** ，则表示邮箱的所有者必须位于传入邮件的**ToRecipients**属性中，以便条件或例外情况适用。 如果值为**false** ，则表示邮箱的所有者不得在传入邮件的**ToRecipients**属性中，以便条件或例外情况适用。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

