---
title: FilterHtmlContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FilterHtmlContent
api_type:
- schema
ms.assetid: 2f9358a0-de1d-4544-9aa0-d9f6519f3b5f
description: FilterHtmlContent 元素指定是否从项目或附件筛选可能不安全的 HTML 内容。
ms.openlocfilehash: 9400c86465db994251a00164517590268e7e4ad1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510083"
---
# <a name="filterhtmlcontent"></a>FilterHtmlContent

**FilterHtmlContent** 元素指定是否从项目或附件筛选可能不安全的 HTML 内容。 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
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
|[AttachmentShape](attachmentshape.md) <br/> | 标识响应 [GetAttachment](getattachment.md) 请求时要返回的其他属性。  <br/><br/>  下面是此元素的 XPath 表达式：  <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[ItemShape](itemshape.md) <br/> | 标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。  <br/> <br/> 下面是此元素的 XPath 表达式： <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>文本值

此元素可以是 **true** 或 **false**。 默认值为 **false**。 这是一个布尔数据类型。
  
## <a name="remarks"></a>说明

此元素为可选。
  
描述此元素的架构位于在安装了客户端访问服务器角色Exchange Server运行的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

