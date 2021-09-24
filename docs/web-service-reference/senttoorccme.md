---
title: SentToOrCcMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SentToOrCcMe
api_type:
- schema
ms.assetid: ca43e05d-df37-485b-9276-34678025f2b7
description: SentToOrCcMe 元素指示邮箱所有者是否必须拥有传入邮件的 ToRecipients 或 CcRecipients 属性，以便条件或例外情况适用。
ms.openlocfilehash: 0e9dddf53c2b671613a5a4c20e3b845a5d38c247
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510888"
---
# <a name="senttoorccme"></a>SentToOrCcMe

**SentToOrCcMe** 元素指示邮箱所有者是否必须拥有传入邮件的 **ToRecipients** 或 **CcRecipients** 属性，以便条件或例外情况适用。 
  
```XML
<SentToOrCcMe>true | false</SentToOrCcMe>
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
|[异常](exceptions.md) <br/> |代表收件箱规则的所有可用规则例外条件。  <br/> |
   
## <a name="text-value"></a>文本值

如果文本值为 **true，** 则表明邮箱所有者必须在传入邮件的 **ToRecipients** 或 **CcRecipients** 属性中，以便条件或例外情况适用。 false **值指示** 邮箱的所有者不得在传入邮件的 **ToRecipients** 或 **CcRecipients** 属性中，以便条件或例外情况适用。 
  
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

