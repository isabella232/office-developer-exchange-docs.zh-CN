---
title: 监视
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- monitoring
api_type:
- schema
ms.assetid: 350d7b46-9260-41a7-8613-3cb8cc1b29a5
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: 5614ac2c6428da9b6845769a9335486d3ded5754
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455826"
---
# <a name="monitoring"></a>监视
  
**适用于：** Exchange Server 2013
  
**Monitoring**元素包含配置信息，用于定义前端传输服务或传输服务如何以及何时监视安装的代理。 
  
- [configuration](configuration.md)  
- [mexRuntime](mexruntime.md)  
- [监视](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

**monitoringType （复杂类型）**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[agentExecution](agentexecution.md) <br/> |定义客户端访问或邮箱服务器等待代理在写入事件日志之前从事件返回的时间（以毫秒为单位）。  <br/> |
|[messageSnapshot](messagesnapshot.md) <br/> |包含一个属性，该属性指定是否为客户端访问或邮箱服务器启用管道跟踪功能。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |包含用于定义代理监视的配置信息和安装的 SMTP 和路由代理的配置信息的元素。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |不正确。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

