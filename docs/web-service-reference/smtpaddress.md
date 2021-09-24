---
title: SmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SmtpAddress
api_type:
- schema
ms.assetid: 779305a6-ad1e-424e-8a69-4e3bef61d787
description: SmtpAddress 元素表示要用于模拟的帐户的简单邮件传输协议 (SMTP) 地址或日历或联系人共享请求的简单邮件传输协议 (SMTP) 收件人地址。
ms.openlocfilehash: c10e18ce77a1002a9c7a94718e8e9a2bd3877d8d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539085"
---
# <a name="smtpaddress"></a>SmtpAddress

**SmtpAddress** 元素表示要用于模拟的帐户的简单邮件传输协议 (SMTP) 地址或日历或联系人共享请求的简单邮件传输协议 (SMTP) 收件人地址。 
  
```xml
<SmtpAddress/>
```

**SmtpAddressType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |表示在使用 ExchangeImpersonation SOAP 标头时要模拟的帐户。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[InvalidRecipient](invalidrecipient.md) <br/> |表示日历共享或联系人共享邮件的无效收件人。  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |表示将被授予共享文件夹访问权限的收件人的集合。  <br/> |
|[GetSharingFolder](getsharingfolder.md) <br/> |定义获取指定共享文件夹的本地文件夹标识符的请求。  <br/> |
   
## <a name="text-value"></a>文本值

需要一个代表 SMTP 地址的文本值。
  
## <a name="remarks"></a>说明

描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

