---
title: PublicFolderInformation （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: PublicFolderInformation 元素包含的信息可供客户端用来发送自动发现请求，以发现用户的公用文件夹信息。
ms.openlocfilehash: e044a1feddfaeb4eb93c289c617dde9adc66f332
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457716"
---
# <a name="publicfolderinformation-pox"></a>PublicFolderInformation （POX）

**PublicFolderInformation**元素包含的信息可供客户端用来发送自动发现请求，以发现用户的公用文件夹信息。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[PublicFolderInformation （POX）](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SmtpAddress （POX）](smtpaddress-pox.md) <br/> |包含分配给为用户配置的公用文件夹邮件存储的 SMTP 地址。 此 SMTP 地址可在自动发现请求的[EMailAddress （POX）](emailaddress-pox.md)元素中使用，以发现公用文件夹设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[帐户（POX）](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
## <a name="remarks"></a>备注

**PublicFolderInformation**元素是**Account**元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

