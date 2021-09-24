---
title: agent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: 上次修改时间：2015 年 9 月 17 日
ms.openlocfilehash: 8bcfdd9bffd4c7a15af40528fd431a99c7868637
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520965"
---
# <a name="agent"></a>agent
  
**适用于：Exchange Server** 2013
  
agent 元素包含有关已安装代理的配置信息。 
  
- [configuration](configuration.md) 
- [mexRuntime](mexruntime.md)
- [agentList](agentlist.md)
- [agent](agent.md)
  
```XML
<agent
        name=""
        baseType=""
        classFactory=""
        assemblyPath=""
        enabled="" />
</agent>
```

**agentType (complexType)**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**name** <br/> |安装代理时指定的名称。 此属性需要一个最多包含 64 个字符的无空字符串值。  <br/> |
|**baseType** <br/> |代理派生自的类的全名（包括命名空间）。 此属性需要至少包含一个字符的无空字符串值。  <br/> |
|**classFactory** <br/> |实现创建代理实例的代理工厂的类的完整名称（包括命名空间）。 此属性必须包含实现创建代理实例的代理工厂的类的完全限定名称。 此类必须派生自 [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) 或 [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) 类。  <br/> |
|**assemblyPath** <br/> |包含代理代码的程序集的完全限定路径（包括文件名）。 此属性需要至少包含一个字符的无空字符串值。  <br/> |
|**enabled** <br/> |一个布尔值，指示是否已启用代理。 如果已启用代理，则值为 **true;** 否则，值为 **false**。 此特性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[agentList](agentlist.md) <br/> |包含每个 **已安装** 代理的代理元素。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |不正确。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

