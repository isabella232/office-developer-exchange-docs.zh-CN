---
title: DirectoryPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: ab436b54-ceba-4cd9-aeb4-134f9b93986d
description: DirectoryPort 元素指定使用 Name Service Provider Interface (NSPI) 连接到目录的端口。
ms.openlocfilehash: 223e82840628e19896bde196d7467622a2ad5002
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543329"
---
# <a name="directoryport-pox"></a>DirectoryPort (POX)

**DirectoryPort** 元素指定使用 Name Service Provider Interface (NSPI) 连接到目录的端口。 
  
- [AutoDiscover (POX)](autodiscover-pox.md) 
- [Response (POX)](response-pox.md)  
- [Account (POX)](account-pox.md)  
- [Protocol (POX)](protocol-pox.md)  
- [DirectoryPort (POX)](directoryport-pox.md)
  
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
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到运行 2007 Microsoft Exchange Server安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示用于访问服务器Exchange端口。
  
## <a name="remarks"></a>注解

**DirectoryPort** 元素仅在 TYPE (POX) [EXCH](type-pox.md)或 EXPR 时使用。 
  
## <a name="see-also"></a>另请参阅

- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

