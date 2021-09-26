---
title: 删除
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Delete
api_type:
- schema
ms.assetid: aa45f0c1-a80d-4b6c-8a85-375b6de515f4
description: Delete 元素指示客户端是否可以删除文件夹或项目。
ms.openlocfilehash: e1ecbfbcb11be04e39dc8353140653e6b5ca1c3b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542489"
---
# <a name="delete"></a>删除

**Delete** 元素指示客户端是否可以删除文件夹或项目。 
  
```XML
<Delete>true or false</Delete>
```

**boolean**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[EffectiveRights](effectiverights.md) <br/> |包含基于项目或文件夹的权限设置的客户端权限。  <br/> |
|[操作](actions.md) <br/> |表示可在满足条件时要采取对邮件的操作的集合。  <br/> |
   
## <a name="text-value"></a>文本值

如果文本值为 **true，** 则表明客户端可以删除项目或文件夹。 false **值表示** 客户端无法删除项目或文件夹。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [Setting Folder-Level Permissions](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

