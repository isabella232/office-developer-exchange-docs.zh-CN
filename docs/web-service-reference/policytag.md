---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: PolicyTag 元素指定项目或文件夹的保留标识符。
ms.openlocfilehash: d6cd5aab1145f6006912541c8f8c1d0a91d1e17e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826835"
---
# <a name="policytag"></a>PolicyTag

**PolicyTag**元素指定项目或文件夹的保留标识符。 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|IsExplicit  <br/> |指示是否策略标记显式设置项目或文件夹。  <br/> 文本值为**true**的**IsExplicit**属性指示上的项目或文件夹的显式设置策略标记。 文本值为**false**指示的隐式的项目或基于父文件夹策略标记文件夹上设置了策略标记。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[SearchPreviewItem](searchpreviewitem.md) | [项](item.md) | [联系人](contact.md) | [消息](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [日历项目](calendaritem.md) | [PostItem](postitem.md) | [任务](task.md)
  
## <a name="text-value"></a>文本值

**PolicyTag**元素的文本值是策略标记标识符。 策略标记标识符是一个 GUID。 
  
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
   

