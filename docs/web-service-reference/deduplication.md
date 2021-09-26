---
title: Deduplication
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: 重复数据删除元素指示搜索结果是否应该删除重复项。
ms.openlocfilehash: 6178502d102b8c24b39d7276352c31740c62352c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543406"
---
# <a name="deduplication"></a>Deduplication

**重复数据删除元素** 指示搜索结果是否应该删除重复项。 
  
```XML
<Deduplication> true | false </Deduplication>
```

**Boolean**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[SearchMailboxes](searchmailboxes.md)  | [SetHoldOnMailboxes](setholdonmailboxes.md)
  
## <a name="text-value"></a>文本值

重复数据删除元素的文本值 **true** 指示搜索结果可能不包含重复项。 false **值表示** 搜索结果可能包含重复项。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

