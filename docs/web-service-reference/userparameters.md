---
title: UserParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bad7311f-7ecd-4f0c-b8e7-dd8f7d378f55
description: UserParameters 元素包含已启用和已禁用客户端扩展的列表。
ms.openlocfilehash: 1d93ec0f4e44b238fcb9aca23672c262795290a6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510727"
---
# <a name="userparameters"></a>UserParameters

**UserParameters** 元素包含已启用和已禁用客户端扩展的列表。 
  
```XML
<UserParameters UserId="" EnabledOnly="">
   <UserEnabledExtensions/>
   <UserDisabledExtensions/>
</UserParameters>
```

 **GetClientExtensionUserParametersType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|UserID  <br/> |**UserId** 属性的文本值是用户的标识符。  <br/> |
|EnabledOnly  <br/> |**EnabledOnly** 的文本值指示响应是否仅包含已启用的扩展。  <br/> |
   
### <a name="child-elements"></a>子元素

[UserEnabledExtensions](userenabledextensions.md)  | [UserDisabledExtensions](userdisabledextensions.md)
  
### <a name="parent-elements"></a>父元素

[GetClientExtension](getclientextension.md)
  
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
   

