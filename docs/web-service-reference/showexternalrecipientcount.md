---
title: ShowExternalRecipientCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ShowExternalRecipientCount
api_type:
- schema
ms.assetid: db28dbcb-d051-4e5c-a9c2-4b8d5149b4e1
description: ShowExternalRecipientCount 元素指示 GetMailTips 操作使用者是否必须显示邮件提示，以指示邮件要发送到的外部收件人的数量。
ms.openlocfilehash: 30615dcb1091dff01cf13679e3e1ed68c8b25af9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539098"
---
# <a name="showexternalrecipientcount"></a>ShowExternalRecipientCount

**ShowExternalRecipientCount** 元素指示 [GetMailTips](getmailtips-operation.md)操作使用者是否必须显示邮件提示，以指示邮件要发送到的外部收件人的数量。 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
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
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |包含邮件提示服务的服务配置信息。  <br/> |
   
## <a name="text-value"></a>文本值

如果[GetMailTips](getmailtips-operation.md) 操作使用者必须显示指示邮件所寻址的外部收件人数的邮件提示，则此元素的文本值为 true。 如果 [GetMailTips](getmailtips-operation.md)操作使用者无需显示指示邮件所寻址的外部收件人数的邮件提示，则值为 **false。** 
  
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

