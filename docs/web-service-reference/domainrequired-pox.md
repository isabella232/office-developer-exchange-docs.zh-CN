---
title: DomainRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: DomainRequired 元素指示域是否需要身份验证。
ms.openlocfilehash: f314b9d27d1b4ee472d249ec49af1a785ff9ac25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753972"
---
# <a name="domainrequired-pox"></a>DomainRequired (POX)

**DomainRequired**元素指示域是否需要身份验证。 
  
- [自动发现 (POX)](autodiscover-pox.md)  
- [响应 (POX)](response-pox.md) 
- [帐户 (POX)](account-pox.md)  
- [协议 (POX)](protocol-pox.md)  
- [DomainRequired (POX)](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
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
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。  <br/> |
   
## <a name="text-value"></a>文本值

文本值指示是否需要身份验证的域。 可能的值为**在**打开和**关闭**。 如果值为**上**，后续请求必须包含用户的帐户的域。
  
## <a name="remarks"></a>备注

如果在[使用 LoginName (POX)](loginname-pox.md)元素中，不指定域或未指定**LoginName**元素，用户必须输入的域之前身份验证将失败。 
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

