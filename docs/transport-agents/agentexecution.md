---
title: agentExecution
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- agentExecution
api_type:
- schema
ms.assetid: 600c4690-941c-45af-a906-5528748d09cd
description: 上次修改时间：2015 年 9 月 17 日
ms.openlocfilehash: 04a53e2698c66326943bcd083c775b53f5c6d5d5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513057"
---
# <a name="agentexecution"></a>agentExecution
  
**适用于：Exchange Server** 2013 
  
**agentExecution** 元素定义客户端访问或邮箱服务器等待代理在写入事件日志之前从事件返回的时间（以毫秒为单位）。 
  
- [configuration](configuration.md)  
- [监视](monitoring.md)
- [agentExecution](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

**agentExecutionType (complexType)**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**timeLimitInMilliseconds** <br/> |一个正整数值，指定服务器等待代理在向事件日志写入警告之前从事件返回的时间（以毫秒为单位）。 如果此值太小，性能可能会降低。 此属性的建议值为 300，000，等于 5 分钟。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[监视](monitoring.md) <br/> |包含配置信息，用于定义前端传输服务或传输服务监视所安装的代理时和方式。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |不正确。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

