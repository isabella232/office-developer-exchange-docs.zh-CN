---
title: AddressListId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: AddressListId 元素指定地址列表的标识符。
ms.openlocfilehash: 5348c6877e24fcc0c8873df1098f8a8e30fe4c1c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541558"
---
# <a name="addresslistid"></a>AddressListId

**AddressListId** 元素指定地址列表的标识符。 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 **AddressListIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |字符串地址列表标识符。 此特性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |指示针对使用文件夹的操作的文件夹。 在复制、删除、移动和设置目标文件夹中的对话项的读取状态时，此元素必须存在。  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |指定电子邮件项目复制到的文件夹的标识符。  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |指示复制和移动操作的目标文件夹。  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |指定电子邮件项目移动到的文件夹的标识符  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

