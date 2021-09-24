---
title: MaxRecipientsPerGetMailTipsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MaxRecipientsPerGetMailTipsRequest
api_type:
- schema
ms.assetid: 8ff5df18-1989-4217-b4c0-599232911d0c
description: MaxRecipientsPerGetMailTipsRequest 元素指示可以传递给 GetMailTips 操作的最大收件人数。
ms.openlocfilehash: 27a67a5ff5a048dbd23bf5dc530a82f82b422e14
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524677"
---
# <a name="maxrecipientspergetmailtipsrequest"></a>MaxRecipientsPerGetMailTipsRequest

**MaxRecipientsPerGetMailTipsRequest** 元素指示可以传递给 [GetMailTips](getmailtips-operation.md)操作的最大收件人数。
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |包含邮件提示服务的服务配置信息。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个整数，表示可以传递给 [GetMailTips](getmailtips-operation.md)操作的最大收件人数。
  
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



[GetMailTips 操作](getmailtips-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

