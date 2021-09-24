---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: PolicyTag 元素指定项目或文件夹的保留标识符。
ms.openlocfilehash: 16759748dded6978e68450a6b8d504dd378c04be
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519252"
---
# <a name="policytag"></a>PolicyTag

**PolicyTag** 元素指定项目或文件夹的保留标识符。 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|IsExplicit  <br/> |指示是否已对项目或文件夹显式设置策略标记。  <br/> **IsExplicit** 属性的文本值 **true** 指示策略标记在项目或文件夹上显式设置。 false **的文本值表示** 策略标记已基于父文件夹策略标记隐式设置在项目或文件夹上。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[SearchPreviewItem](searchpreviewitem.md)  | [Item](item.md)  | [联系人](contact.md)  | [邮件](message-ex15websvcsotherref.md)  | [DistributionList](distributionlist.md)  | [CalendarItem](calendaritem.md)  | [PostItem](postitem.md)  | [任务](task.md)
  
## <a name="text-value"></a>文本值

**PolicyTag** 元素的文本值是策略标记标识符。 策略标记标识符是一个 GUID。 
  
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
   

