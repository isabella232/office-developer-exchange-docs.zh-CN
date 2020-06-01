---
title: InPlaceHoldConfigurationOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 921ecc73-b7e2-40a7-8458-68f18dd5a13b
description: InPlaceHoldConfigurationOnly 元素指定是否包含就地保留配置。
ms.openlocfilehash: ca364ee7d8a9e2e4a608f8f6c4ca5851fa7d4b64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466099"
---
# <a name="inplaceholdconfigurationonly"></a>InPlaceHoldConfigurationOnly

**InPlaceHoldConfigurationOnly**元素指定是否包含就地保留配置。 
  
```XML
<InPlaceHoldConfigurationOnly>true | false</InPlaceHoldConfigurationOnly>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)
  
## <a name="text-value"></a>文本值

如果**InPlaceHoldConfigurationOnly**元素的文本值为**true** ，则表示包含就地保留配置。 **如果值为 false** ，则表示不包含就地保留配置。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

