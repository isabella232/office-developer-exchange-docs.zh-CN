---
title: DirectoryPort （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ab436b54-ceba-4cd9-aeb4-134f9b93986d
description: DirectoryPort 元素指定在使用名称服务提供程序接口（NSPI）协议时用于连接到目录的端口。
ms.openlocfilehash: 2ba0a15cea0b4eb9b6069fab384edb3d9747a360
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462085"
---
# <a name="directoryport-pox"></a>DirectoryPort （POX）

**DirectoryPort**元素指定在使用名称服务提供程序接口（NSPI）协议时用于连接到目录的端口。 
  
- [自动发现（POX）](autodiscover-pox.md) 
- [响应（POX）](response-pox.md)  
- [帐户（POX）](account-pox.md)  
- [协议（POX）](protocol-pox.md)  
- [DirectoryPort （POX）](directoryport-pox.md)
  
```xml
<DirectoryPort/>
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

该文本值表示用于访问 Exchange 服务器的端口。
  
## <a name="remarks"></a>备注

仅当[Type （POX）](type-pox.md)元素等于 EXCH 或 EXPR 时，才使用**DirectoryPort**元素。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

