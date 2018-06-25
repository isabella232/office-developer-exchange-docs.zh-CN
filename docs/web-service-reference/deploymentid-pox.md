---
title: DeploymentId (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: DeploymentId 元素唯一地标识 Microsoft Exchange Server 2007 林。
ms.openlocfilehash: 4f2548709753d8407d02218acecd9233f0ba764f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753837"
---
# <a name="deploymentid-pox"></a>DeploymentId (POX)

**DeploymentId**元素唯一地标识 Microsoft Exchange Server 2007 林。 
  
- [自动发现 (POX)](autodiscover-pox.md)  
- [响应 (POX)](response-pox.md) 
- [用户 (POX)](user-pox.md)  
- [DeploymentId (POX)](deploymentid-pox.md)
  
```xml
<DeploymentId/>
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
|[用户 (POX)](user-pox.md) <br/> |提供特定于用户的信息。  <br/> |
   
## <a name="text-value"></a>文本值

文本值唯一地标识 GUID 格式中的为 Exchange 2007 林。
  
## <a name="remarks"></a>注解

如果您卸载并重新安装 Exchange 2007，并使用相同的服务器名称， **DeploymentId**值发生更改。 
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

