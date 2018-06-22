---
title: 代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 3895095ed4e469cdb9fec489ba6b6e228779a9c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753054"
---
# <a name="agent"></a>代理
  
**适用于：** Exchange Server 2013
  
**代理**元素包含安装代理的配置信息。 
  
- [configuration](configuration.md) 
- [mexRuntime](mexruntime.md)
- [agentList](agentlist.md)
- [代理](agent.md)
  
```XML
<agent
        name=""
        baseType=""
        classFactory=""
        assemblyPath=""
        enabled="" />
</agent>
```

**agentType （复杂类型）**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**name** <br/> |代理安装时指定的名称。 此属性需要包含超过 64 个字符的非空字符串值。  <br/> |
|**baseType** <br/> |完整名称，包括代理从中派生的类的命名空间。 此属性需要一个非空的 string 值，包含至少一个字符。  <br/> |
|**classFactory** <br/> |包括的命名空间的类的实现代理工厂创建代理的实例的完整名称。 此属性必须包含实现代理工厂创建代理的实例的类的完全限定的名称。 此类必须从[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)或[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)类。  <br/> |
|**assemblyPath** <br/> |包括的代理的包含代码的程序集的文件名的完全限定的路径。 此属性需要一个非空的 string 值，包含至少一个字符。  <br/> |
|**启用** <br/> |一个布尔值，该值指示是否启用代理。 如果启用代理，则值为**true**否则，值为**false**。 此属性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[agentList](agentlist.md) <br/> |包含的每个安装代理**代理**元素。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |False。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

