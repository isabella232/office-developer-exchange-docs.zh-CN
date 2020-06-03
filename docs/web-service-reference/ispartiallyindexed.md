---
title: IsPartiallyIndexed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 542e7b90-eafe-4711-a9d7-71bbc30d9646
description: IsPartiallyIndexed 元素指示是否对项目进行部分索引。
ms.openlocfilehash: 4bf0c3e5dd7b75a90ac087958fbceda334306af1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466484"
---
# <a name="ispartiallyindexed"></a>IsPartiallyIndexed

**IsPartiallyIndexed**元素指示是否对项目进行部分索引。 
  
```XML
<IsPartiallyIndexed>true | false</IsPartiallyIndexed>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[NonIndexableItemDetail](nonindexableitemdetail.md)
  
## <a name="text-value"></a>文本值

如果**IsPartiallyIndexed**元素的文本值为**true** ，则表示该邮箱项目已部分编制索引。 如果值为**false** ，则表示未对邮箱项目进行部分索引。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

