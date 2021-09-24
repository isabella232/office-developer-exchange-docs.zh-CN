---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: IsWritable 元素指定是否可以将基础联系人或 Active Directory 收件人写入其中。
ms.openlocfilehash: 2663e18f2589516f304930b86a717455b6ab77c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516711"
---
# <a name="iswritable"></a>IsWritable

**IsWritable** 元素指定是否可以将基础联系人或 Active Directory 收件人写入其中。 
  
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

[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md)
  
## <a name="text-value"></a>文本值

**IsWritable** 元素的文本值 **true** 指示联系人或 Active Directory 对象可用于写入访问。 false **值表示** 联系人或 Active Directory 对象不能进行写入访问。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  

