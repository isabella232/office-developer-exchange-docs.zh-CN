---
title: ItemChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemChanges
api_type:
- schema
ms.assetid: cd307892-2f69-4494-8325-219bdb5c3ad5
description: ItemChanges 元素包含 ItemChange 元素的数组，用于标识项目以及要应用于项目的更新。
ms.openlocfilehash: 69a90f7bce330910b9ff44c63656f38509438981
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516683"
---
# <a name="itemchanges"></a>ItemChanges

**ItemChanges** 元素包含 [ItemChange](itemchange.md)元素的数组，用于标识项目以及要应用于项目的更新。 
  
[UpdateItem](updateitem.md)
  
[ItemChanges](itemchanges.md)
  
```xml
<ItemChanges>
   <ItemChange/>
</ItemChanges>
```

 **NonEmptyArrayOfItemChangesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemChange](itemchange.md) <br/> |包含项目标识符和要应用于项目的更新。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UpdateItem](updateitem.md) <br/> |定义更新邮箱中的项目的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/UpdateItem` <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateItem 操作](updateitem-operation.md)

