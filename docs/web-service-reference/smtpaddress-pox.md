---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: SmtpAddress 元素包含分配给为用户配置的公用文件夹邮件存储的 SMTP 地址。
ms.openlocfilehash: d257b193a3254afceaa72d396a8c2724bb3165c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546985"
---
# <a name="smtpaddress-pox"></a>SmtpAddress (POX)

**SmtpAddress** 元素包含分配给为用户配置的公用文件夹邮件存储的 SMTP 地址。 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
- [SmtpAddress (POX)](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |包含客户端可用于发送自动发现请求以发现用户的公用文件夹信息的信息。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示分配给为用户配置的公用文件夹存储的 SMTP 地址。 此 SMTP 地址可用于自动发现请求的 [EMailAddress ](emailaddress-pox.md) (POX) 元素，以发现公用文件夹设置。 
  
## <a name="remarks"></a>注解

**SmtpAddress** 元素是 **PublicFolderInformation** 元素的必需子元素。 
  
## <a name="see-also"></a>另请参阅

- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

