---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: IsWritable 元素指定是否可以向写入基础联系人或 Active Directory 收件人。
ms.openlocfilehash: 03f258d01ecfc12dfa4e09ac88f4a75340d2acf3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826158"
---
# <a name="iswritable"></a>IsWritable

**IsWritable**元素指定是否可以向写入基础联系人或 Active Directory 收件人。 
  
```XML
<IsWritable> true | false </IsWritable>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[归属 (PersonaAttributionType)](attribution-personaattributiontype.md)
  
## <a name="text-value"></a>文本值

文本值为**true**的**IsWritable**元素指示的联系人或 Active Directory 对象是可供写访问权限。 如果值为**false**指示的联系人或 Active Directory 对象不可用的写访问权限。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  

