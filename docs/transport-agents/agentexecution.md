---
title: agentExecution
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentExecution
api_type:
- schema
ms.assetid: 600c4690-941c-45af-a906-5528748d09cd
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 5848d52a68c8c3f747614015e49becb34bc4cfd8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753051"
---
# <a name="agentexecution"></a>agentExecution
  
**适用于：** Exchange Server 2013 
  
**AgentExecution**元素定义时间，以毫秒为单位，等待代理以从事件之前它写入事件日志中返回客户端访问或邮箱服务器。 
  
- [configuration](configuration.md)  
- [监控](monitoring.md)
- [agentExecution](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

**agentExecutionType （复杂类型）**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**timeLimitInMilliseconds** <br/> |正整数值，该值指定时间，以毫秒为单位，服务器等待代理以从之前的事件返回事件日志中写入一条警告。 如果此值太小，可能会降低性能。 此属性的建议的值为 300000，其等于 5 分钟。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[监控](monitoring.md) <br/> |包含定义如何以及何时前端传输服务或的传输服务监视安装代理的配置信息。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |False。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

