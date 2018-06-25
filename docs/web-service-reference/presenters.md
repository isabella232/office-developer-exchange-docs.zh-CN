---
title: 演示者
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: 演示者元素指定的联机会议的演示者。
ms.openlocfilehash: f62b458759e0d8199c98827602d6c3fe16aebeea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826875"
---
# <a name="presenters"></a>演示者

**演示者**元素指定的联机会议的演示者。 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 **PresentersType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>文本值

**演示者**元素的文本值的用户可以在联机会议的演示者的类型。 下表中介绍的**演示者**元素的文本值。 
  
**演示者元素的文本值**

|**值**|**说明**|
|:-----|:-----|
|已禁用  <br/> |演示者将被禁用。  <br/> |
|内部  <br/> |仅内部的参与者可以是演示者。  <br/> |
|所有人  <br/> |任何参与者都可以成为演示者。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

