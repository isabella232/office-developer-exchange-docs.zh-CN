---
title: DomainName （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2b4af2b2-58b5-4f28-9cb3-c07a11377747
description: DomainName 元素指定用户的域。
ms.openlocfilehash: ff38d6a876e396317dedece0a81a9f9f0db0f587
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458423"
---
# <a name="domainname-pox"></a>DomainName （POX）

**DomainName**元素指定用户的域。 
  
- [自动发现（POX）](autodiscover-pox.md)  
- [响应（POX）](response-pox.md)  
- [帐户（POX）](account-pox.md) 
- [协议（POX）](protocol-pox.md) 
- [DomainName （POX）](domainname-pox.md)
  
```xml
<DomainName/>
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
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值指定用户的域。
  
## <a name="remarks"></a>备注

如果未指定任何值，则默认身份验证是将电子邮件地址用作用户主体名称（UPN）格式。 例如： \<Username\> @ \<Domain\> 。
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

