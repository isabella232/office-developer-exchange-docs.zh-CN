---
title: InvalidRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipient
api_type:
- schema
ms.assetid: 9e2d3433-22d7-444b-9883-e5649297d8fe
description: InvalidRecipient 元素包含无效收件人的 SMTP 地址，以及有关收件人无效的原因的信息。
ms.openlocfilehash: f301b31c1054625151ce90e41fca5e3efc21f473
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526548"
---
# <a name="invalidrecipient"></a>InvalidRecipient

**InvalidRecipient**元素包含无效收件人的 SMTP 地址，以及有关收件人无效的原因的信息。 
  
```XML
<InvalidRecipient>
   <SmtpAddress/>
   <ResponseCode/>
   <MessageText/>
</InvalidRecipient>

```

 **InvalidRecipientType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |包含无效收件人的 SMTP 地址。 此元素是必需的。  <br/> |
|[ResponseCode （InvalidRecipientResponseCodeType）](responsecode-invalidrecipientresponsecodetype.md) <br/> |提供用于标识请求遇到的特定错误的错误代码。 此元素是必需的。  <br/> |
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。 此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[InvalidRecipients](invalidrecipients.md) <br/> |表示无效的文件夹共享请求的收件人。  <br/> |
   
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



[GetSharingMetadata 操作](getsharingmetadata-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

