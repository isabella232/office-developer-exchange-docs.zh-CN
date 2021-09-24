---
title: messageSnapshot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: 上次修改时间：2015 年 9 月 17 日
ms.openlocfilehash: 2ac38dd3f50b5d9d070262f3daffb72b02df5d82
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525454"
---
# <a name="messagesnapshot"></a>messageSnapshot

**适用于：Exchange Server** 2013
  
**messageSnapshot** 元素包含一个属性，该属性指定是否对安装了客户端访问或邮箱服务器角色的 Exchange 服务器启用管道跟踪功能。 
  
- [configuration](configuration.md)  
- [mexRuntime](mexruntime.md) 
- [监视](monitoring.md) 
- [messageSnapshot](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

**messageSnapshotType (布尔)**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**enabled** <br/> |一个布尔值，指示是否对客户端访问或邮箱服务器启用管道跟踪功能。 如果启用管道跟踪，则值为 **true;** 否则，值为 **false** 或元素不存在。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[监视](monitoring.md) <br/> |包含配置信息，用于定义传输服务监视所安装代理的监视方式和时间。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |不正确。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

