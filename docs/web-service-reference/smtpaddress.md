---
title: SmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SmtpAddress
api_type:
- schema
ms.assetid: 779305a6-ad1e-424e-8a69-4e3bef61d787
description: SmtpAddress 元素表示用于模拟的帐户的简单邮件传输协议 (SMTP) 地址或日历或联系人共享请求的简单邮件传输协议 (SMTP) 收件人地址。
ms.openlocfilehash: 39588f0892cdcec819a1972547155730be5785f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827511"
---
# <a name="smtpaddress"></a>SmtpAddress

**SmtpAddress**元素表示用于模拟的帐户的简单邮件传输协议 (SMTP) 地址或日历或联系人共享请求的简单邮件传输协议 (SMTP) 收件人地址。 
  
```xml
<SmtpAddress/>
```

**SmtpAddressType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |代表用于模拟使用 ExchangeImpersonation SOAP 标头时的帐户。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[InvalidRecipient](invalidrecipient.md) <br/> |代表无效收件人的日历共享或共享邮件的联系人。  <br/> |
|[收件人 (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |代表将被授予访问权限的共享文件夹的收件人的集合。  <br/> |
|[GetSharingFolder](getsharingfolder.md) <br/> |定义一个请求以获取指定的共享文件夹的本地文件夹标识符。  <br/> |
   
## <a name="text-value"></a>文本值

需要安装一个代表 SMTP 地址的文本值。
  
## <a name="remarks"></a>备注

描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

