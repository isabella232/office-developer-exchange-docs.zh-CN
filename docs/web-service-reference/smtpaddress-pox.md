---
title: SmtpAddress （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: SmtpAddress 元素包含分配给为用户配置的公用文件夹邮件存储的 SMTP 地址。
ms.openlocfilehash: 48703a11fb056967c6c76073c2e928d5f6efa264
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468640"
---
# <a name="smtpaddress-pox"></a>SmtpAddress （POX）

**SmtpAddress**元素包含分配给为用户配置的公用文件夹邮件存储的 SMTP 地址。 
  
- [自动发现（POX）](autodiscover-pox.md)
  
- [响应（POX）](response-pox.md)
  
- [帐户（POX）](account-pox.md)
  
- [PublicFolderInformation （POX）](publicfolderinformation-pox.md)
  
- [SmtpAddress （POX）](smtpaddress-pox.md)
  
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
|[PublicFolderInformation （POX）](publicfolderinformation-pox.md) <br/> |包含客户端可用于发送自动发现请求以发现用户公用文件夹信息的信息。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值表示分配给为用户配置的公用文件夹存储的 SMTP 地址。 此 SMTP 地址可在自动发现请求的[EMailAddress （POX）](emailaddress-pox.md)元素中使用，以发现公用文件夹设置。 
  
## <a name="remarks"></a>备注

**SmtpAddress**元素是**PublicFolderInformation**元素所需的子元素。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

