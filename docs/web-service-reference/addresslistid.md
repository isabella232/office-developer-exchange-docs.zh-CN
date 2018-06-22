---
title: AddressListId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: AddressListId 元素指定的地址列表的标识符。
ms.openlocfilehash: d8a513559b7d127559537b43d7c6c0a4db121702
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753127"
---
# <a name="addresslistid"></a>AddressListId

**AddressListId**元素指定的地址列表的标识符。 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 **AddressListIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|
  **Id** <br/> |一个 string 地址列表标识符。 此属性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |指示使用文件夹的操作的目标文件夹。 此元素必须存在时复制、 删除、 移动和目标文件夹中的对话项目上设置只读的状态。  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |指定电子邮件项目复制到其中的文件夹的标识符。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示副本的目标文件夹，并移动操作。  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |指定电子邮件项目移至其中的文件夹的标识符  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

