---
title: Count
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Count
api_type:
- schema
ms.assetid: 68314b4a-1e17-4e21-9c2e-224d70ef7a32
description: Count 元素包含 UpdateItem 操作响应中的冲突数。
ms.openlocfilehash: a43896a1b8b6a9d96ab02afe64f9e553639e478e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466757"
---
# <a name="count"></a>Count

[Count](count.md)元素包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突数。 
  
[UpdateItemResponse](updateitemresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[UpdateItemResponseMessage](updateitemresponsemessage.md)
  
[ConflictResults](conflictresults.md)
  
[Count](count.md)
  
```xml
<Count/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConflictResults](conflictresults.md) <br/> |包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突数。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值是一个整数，表示[UpdateItem 操作](updateitem-operation.md)响应中的冲突数。 
  
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateItem 操作](updateitem-operation.md)
  
 **ConflictResultsType**

