---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: IsWritable 元素指定基础联系人或 Active Directory 收件人是否可以写入。
ms.openlocfilehash: 96075adc1772027456f8829eee43bdc734644c09
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467569"
---
# <a name="iswritable"></a>IsWritable

**IsWritable**元素指定基础联系人或 Active Directory 收件人是否可以写入。 
  
```XML
<IsWritable> true | false </IsWritable>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[归属（PersonaAttributionType）](attribution-personaattributiontype.md)
  
## <a name="text-value"></a>文本值

如果**IsWritable**元素的文本值为**true** ，则表示联系人或 Active Directory 对象可用于写入访问。 如果值为**false** ，则表示联系人或 Active Directory 对象不可用于写访问。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  

