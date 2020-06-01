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
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: a810bb229015054e0f244773760235114655a982
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455679"
---
# <a name="agent"></a>代理
  
**适用于：** Exchange Server 2013
  
**Agent**元素包含有关已安装的代理的配置信息。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**name** <br/> |安装代理时指定的名称。 此属性需要一个非空字符串值，最多包含64个字符。  <br/> |
|**#c1** <br/> |代理派生的类的完整名称（包括命名空间）。 此属性需要一个不包含至少一个字符的非空字符串值。  <br/> |
|**classFactory** <br/> |实现代理工厂创建代理实例的类的完整名称（包括命名空间）。 此属性必须包含实现代理工厂创建代理实例的类的完全限定名称。 此类必须派生自[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)或[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)类。  <br/> |
|**assemblyPath** <br/> |包含代理代码的程序集的完全限定路径（包括文件名）。 此属性需要一个不包含至少一个字符的非空字符串值。  <br/> |
|**enabled** <br/> |一个布尔值，该值指示是否已启用代理。 如果启用了代理，则此值为**true** ; 否则为 false。否则，该值为**false**。 此特性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[agentList](agentlist.md) <br/> |包含每个已安装代理的**代理**元素。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |不正确。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

