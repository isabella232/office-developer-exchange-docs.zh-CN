---
title: 监控
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
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 1b5484467def0bf3d22ba0707357977d5ed461ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753081"
---
# <a name="monitoring"></a>监控
  
**适用于：** Exchange Server 2013
  
**监控**元素包含定义如何以及何时的前端传输服务或的传输服务监视安装代理的配置信息。 
  
- [configuration](configuration.md)  
- [mexRuntime](mexruntime.md)  
- [监控](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

**monitoringType （复杂类型）**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[agentExecution](agentexecution.md) <br/> |定义时间，以毫秒为单位，等待代理以从事件之前它写入事件日志中返回的客户端访问或邮箱服务器。  <br/> |
|[messageSnapshot](messagesnapshot.md) <br/> |包含指定是否为客户端访问或邮箱服务器启用管道跟踪功能属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |包含定义监控代理的配置信息和 SMTP 和安装的路由代理的配置信息的元素。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |False。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

