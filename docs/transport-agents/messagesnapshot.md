---
title: messageSnapshot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 4b814def8eef8fb452d2e754c5f6787d644055f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753082"
---
# <a name="messagesnapshot"></a>messageSnapshot

**适用于：** Exchange Server 2013
  
**MessageSnapshot**元素包含指定是否具有客户端访问或安装了邮箱服务器角色的 Exchange 服务器启用管道跟踪功能属性。 
  
- [configuration](configuration.md)  
- [mexRuntime](mexruntime.md) 
- [监控](monitoring.md) 
- [messageSnapshot](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

**messageSnapshotType （布尔值）**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**启用** <br/> |一个布尔值，该值指示是否为客户端访问或邮箱服务器启用管道跟踪功能。 如果启用管道跟踪，则值为**true**否则为值为**false**或不存在元素。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[监控](monitoring.md) <br/> |包含定义如何以及何时的传输服务将监视安装代理的配置信息。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |False。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

