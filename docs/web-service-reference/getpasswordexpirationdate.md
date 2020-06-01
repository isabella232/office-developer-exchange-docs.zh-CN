---
title: GetPasswordExpirationDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4f958ed-9cf4-4ebf-9b01-e2df9a7cbd63
description: GetPasswordExpirationDate 元素定义一个请求，以获取电子邮件帐户的密码到期日期。 此元素是 GetPasswordExpirationDate 操作操作的基本元素。
ms.openlocfilehash: ececbf51f71c7d87705d727229fce2314d922efb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456491"
---
# <a name="getpasswordexpirationdate"></a>GetPasswordExpirationDate

**GetPasswordExpirationDate**元素定义一个请求，以获取电子邮件帐户的密码到期日期。 此元素是[GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md)操作的基本元素。 
  
```XML
<GetPasswordExpirationDate>
    <MailboxSmtpAddress/>
</GetPasswordExpirationDate>
```

 **GetPasswordExpirationDateType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素名**|**说明**|
|:-----|:-----|
|[MailboxSmtpAddress](mailboxsmtpaddress.md) <br/> |表示要为其返回密码到期日期的电子邮件帐户的电子邮件地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

