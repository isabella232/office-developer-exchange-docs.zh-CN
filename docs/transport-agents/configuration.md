---
title: 设置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- configuration
api_type:
- schema
ms.assetid: 6fc04e4d-657a-4999-9431-186ccb7832b5
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: b886851b9a0c17d58428f49281d664930d0e4070
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461560"
---
# <a name="configuration"></a>设置
  
**适用于：** Exchange Server 2013
  
**Configuration**元素是代理配置文件的根元素。 
  
- [configuration](configuration.md) 
- [mexRuntime](mexruntime.md)
  
```XML
<configuration>
      <mexRuntime/>
</configuration>
```

**configurationType （复杂类型）**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |包含用于定义代理监视的配置信息和安装的 SMTP 和路由代理的配置信息的元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |此文件不定义命名空间。  <br/> |
|架构名称  <br/> |不可用。  <br/> |
|验证文件  <br/> |不可用。  <br/> |
|可以为空  <br/> |不正确。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的代理配置文件元素](agents-configuration-file-elements-for-exchange-2013.md)

