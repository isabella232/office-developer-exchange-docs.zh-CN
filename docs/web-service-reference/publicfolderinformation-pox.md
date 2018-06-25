---
title: PublicFolderInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: PublicFolderInformation 元素包含客户端可以使用发送发现用户的公用文件夹信息的自动发现请求的信息。
ms.openlocfilehash: bb4432a664024c3d1ccb17826948cfe7a1b58cdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826927"
---
# <a name="publicfolderinformation-pox"></a>PublicFolderInformation (POX)

**PublicFolderInformation**元素包含客户端可以使用发送发现用户的公用文件夹信息的自动发现请求的信息。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SmtpAddress (POX)](smtpaddress-pox.md) <br/> |包含分配给公用文件夹消息存储为用户配置的 SMTP 地址。 此 SMTP 地址可以自动发现请求的[电子邮件地址 (POX)](emailaddress-pox.md)元素中，用于发现公用文件夹设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[帐户 (POX)](account-pox.md) <br/> |指定用户帐户的设置。  <br/> |
   
## <a name="remarks"></a>注解

**PublicFolderInformation**元素是**帐户**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

