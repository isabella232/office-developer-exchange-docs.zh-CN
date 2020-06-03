---
title: ContentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentId
api_type:
- schema
ms.assetid: bc59100d-6079-414b-a6e0-7c15feaa3184
description: ContentId 元素表示附件内容的标识符。 ContentId 可以设置为任何字符串值。 应用程序可以使用 ContentId 来实现自己的标识机制。
ms.openlocfilehash: ca89c8790e839326412003f26b738ad1ee956211
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529264"
---
# <a name="contentid"></a>ContentId

**ContentId**元素表示附件内容的标识符。 **ContentId**可以设置为任何字符串值。 应用程序可以使用**ContentId**来实现自己的标识机制。 
  
```xml
<ContentId/>
```

 **String**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |表示附加到另一个 Exchange 项目的 Exchange 项目。  <br/> |
|[FileAttachment](fileattachment.md) <br/> |代表附加到 Exchange 存储中的项目的文件。  <br/> |
   
## <a name="text-value"></a>文本值

字符串值表示附件内容的标识符。
  
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

