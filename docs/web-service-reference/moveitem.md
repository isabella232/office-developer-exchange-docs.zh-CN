---
title: MoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: a4593377-22dd-415f-b01d-387389ef650f
description: MoveItem 元素定义了在 Exchange 存储中移动项目的请求。
ms.openlocfilehash: 61dbb91cc20a71f50999241b3daa21bf8ebfbcc8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530399"
---
# <a name="moveitem"></a>MoveItem

**MoveItem**元素定义了在 Exchange 存储中移动项目的请求。 
  
```XML
<MoveItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</MoveItem>
```

 **MoveItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ToFolderId](tofolderid.md) <br/> |表示所移动的项的目标文件夹。  <br/> |
|[ItemIds](itemids.md) <br/> |包含标识的项的数组，这些项将移至[ToFolderId](tofolderid.md)元素所表示的文件夹中。  <br/> |
|[ReturnNewItemIds](returnnewitemids.md) <br/> |指示响应中是否返回新项的项标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[MoveItem 操作](moveitem-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

