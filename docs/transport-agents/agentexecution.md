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
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: 457257e59fb37659daf2f91b0fa5dfced5c48c03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44446488"
---
# <a name="agentexecution"></a>agentExecution
  
**适用于：** Exchange Server 2013 
  
**AgentExecution**元素定义客户端访问或邮箱服务器等待代理在写入事件日志之前从事件返回的时间（以毫秒为单位）。 
  
- [configuration](configuration.md)  
- [监视](monitoring.md)
- [agentExecution](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

**agentExecutionType （复杂类型）**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**timeLimitInMilliseconds** <br/> |一个正整数值，指定服务器在将警告写入事件日志之前等待代理从事件返回的时间（以毫秒为单位）。 如果此值太小，则性能可能会降低。 此属性的建议值为300000，相当于5分钟。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[监视](monitoring.md) <br/> |包含定义前端传输服务或传输服务如何以及何时监视安装的代理的配置信息。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |不正确。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

