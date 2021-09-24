---
title: 演示者
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: Presenters 元素指定联机会议演示者。
ms.openlocfilehash: 1c9bf9093450e675245b647c98d7b1d00101ce9e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519140"
---
# <a name="presenters"></a>演示者

**Presenters** 元素指定联机会议演示者。 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 **PresentersType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>文本值

**Presenters 元素** 的文本值是可以是联机会议演示者的用户的类型。 下表介绍了 **Presenters** 元素的文本值。 
  
**Presenters 元素文本值**

|**值**|**说明**|
|:-----|:-----|
|已禁用  <br/> |演示者被禁用。  <br/> |
|内部  <br/> |只有内部参与者才能成为演示者。  <br/> |
|所有人  <br/> |任何参与者都可以是演示者。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

