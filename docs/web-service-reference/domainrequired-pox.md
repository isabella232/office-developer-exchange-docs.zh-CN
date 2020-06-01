---
title: DomainRequired （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: DomainRequired 元素指示是否需要域进行身份验证。
ms.openlocfilehash: 97d602c40b247f9a6650cc4440b53bf23c18482e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461322"
---
# <a name="domainrequired-pox"></a>DomainRequired （POX）

**DomainRequired**元素指示是否需要域进行身份验证。 
  
- [自动发现（POX）](autodiscover-pox.md)  
- [响应（POX）](response-pox.md) 
- [帐户（POX）](account-pox.md)  
- [协议（POX）](protocol-pox.md)  
- [DomainRequired （POX）](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
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

Text 值指示是否需要域进行身份验证。 可能的值为 **"开" 或 "** **关**"。 如果值为 **"开**"，则后续请求必须包含用户帐户的域。
  
## <a name="remarks"></a>备注

如果未在[person.loginname （POX）](loginname-pox.md)元素中指定域，或未指定**person.loginname**元素，则用户必须输入域，然后身份验证才能成功。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

