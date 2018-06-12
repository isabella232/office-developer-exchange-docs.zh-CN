---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: SmtpAddress 元素包含分配给公用文件夹消息存储为用户配置的 SMTP 地址。
ms.openlocfilehash: 43ebb328e31cdec11412e80b743d4d4393b7960a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827507"
---
# <a name="smtpaddress-pox"></a>SmtpAddress (POX)

**SmtpAddress**元素包含分配给公用文件夹消息存储为用户配置的 SMTP 地址。 
  
- [自动发现 (POX)](autodiscover-pox.md)
  
- [响应 (POX)](response-pox.md)
  
- [帐户 (POX)](account-pox.md)
  
- [PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
- [SmtpAddress (POX)](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |包含客户端可以使用发送发现用户的公用文件夹信息的自动发现请求的信息。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示分配给公用文件夹存储为用户配置的 SMTP 地址。 此 SMTP 地址可以自动发现请求的[电子邮件地址 (POX)](emailaddress-pox.md)元素中，用于发现公用文件夹设置。 
  
## <a name="remarks"></a>备注

**SmtpAddress**元素是**PublicFolderInformation**元素的必需的子元素。 
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

