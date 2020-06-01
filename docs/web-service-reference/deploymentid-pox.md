---
title: DeploymentId （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: DeploymentId 元素唯一标识 Microsoft Exchange Server 2007 林。
ms.openlocfilehash: 4986a3404763e88fb3e84d52a5d30d54c810f93a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467919"
---
# <a name="deploymentid-pox"></a>DeploymentId （POX）

**DeploymentId**元素唯一标识 Microsoft Exchange Server 2007 林。 
  
- [自动发现（POX）](autodiscover-pox.md)  
- [响应（POX）](response-pox.md) 
- [User （POX）](user-pox.md)  
- [DeploymentId （POX）](deploymentid-pox.md)
  
```xml
<DeploymentId/>
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
|[User （POX）](user-pox.md) <br/> |提供用户特定的信息。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值唯一标识采用 GUID 格式的 Exchange 2007 林。
  
## <a name="remarks"></a>备注

如果您卸载然后重新安装 Exchange 2007 并使用相同的服务器名称，则**DeploymentId**值将更改。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

