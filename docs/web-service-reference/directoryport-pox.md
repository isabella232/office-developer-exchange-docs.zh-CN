---
title: DirectoryPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ab436b54-ceba-4cd9-aeb4-134f9b93986d
description: DirectoryPort 元素指定用于连接到目录时使用的名称服务提供程序界面 (NSPI) 协议的端口。
ms.openlocfilehash: 1b73b9cd1d21c73f4e897684371993312f741322
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753877"
---
# <a name="directoryport-pox"></a>DirectoryPort (POX)

**DirectoryPort**元素指定用于连接到目录时使用的名称服务提供程序界面 (NSPI) 协议的端口。 
  
- [自动发现 (POX)](autodiscover-pox.md) 
- [响应 (POX)](response-pox.md)  
- [帐户 (POX)](account-pox.md)  
- [协议 (POX)](protocol-pox.md)  
- [DirectoryPort (POX)](directoryport-pox.md)
  
```xml
<DirectoryPort/>
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

文本值表示用于访问 Exchange 服务器的端口。
  
## <a name="remarks"></a>注解

[类型 (POX)](type-pox.md)元素等于 EXCH 或 EXPR 时才使用**DirectoryPort**元素。 
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

