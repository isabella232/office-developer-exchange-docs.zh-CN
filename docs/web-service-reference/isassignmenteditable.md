---
title: IsAssignmentEditable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsAssignmentEditable
api_type:
- schema
ms.assetid: 0ddf9181-f65e-4ad6-ad69-7b074ea0f2e7
description: IsAssignmentEditable 元素表示任务类型。
ms.openlocfilehash: 10676cc8c6196a7294f3550856a47dce7d717e6a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544948"
---
# <a name="isassignmenteditable"></a>IsAssignmentEditable

**IsAssignmentEditable** 元素表示任务类型。 
  
```xml
<IsAssignmentEditable/>
```

 **integer**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="text-value"></a>文本值

此属性是只读的。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|0  <br/> |所有任务项的默认值。  <br/> |
|1  <br/> |任务请求。  <br/> |
|2  <br/> |任务请求的收件人接受的任务。  <br/> |
|3  <br/> |任务请求收件人的任务减减。  <br/> |
|4   <br/> |对上一个任务请求的更新。  <br/> |
|5  <br/> |未使用。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

