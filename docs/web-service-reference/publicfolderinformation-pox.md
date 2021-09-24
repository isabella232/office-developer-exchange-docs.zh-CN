---
title: PublicFolderInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: PublicFolderInformation 元素包含客户端可用于发送自动发现请求以发现用户的公用文件夹信息的信息。
ms.openlocfilehash: d77ea350f05c5d6137d3b67cfd49119bf9590e53
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540620"
---
# <a name="publicfolderinformation-pox"></a>PublicFolderInformation (POX)

**PublicFolderInformation** 元素包含客户端可用于发送自动发现请求以发现用户的公用文件夹信息的信息。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[PublicFolderInformation (POX)](publicfolderinformation-pox.md)
  
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
|[SmtpAddress (POX)](smtpaddress-pox.md) <br/> |包含分配给为用户配置的公用文件夹邮件存储的 SMTP 地址。 此 SMTP 地址可用于自动发现请求的 [EMailAddress ](emailaddress-pox.md) (POX) 元素，以发现公用文件夹设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Account (POX)](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
## <a name="remarks"></a>注解

**PublicFolderInformation** 元素是 **Account** 元素的可选子元素。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

