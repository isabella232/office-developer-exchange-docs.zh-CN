---
title: TelephoneAccessFolderEmail（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- TelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 5d32ae22-bb9f-4352-a251-d516b66ff35b
description: TelephoneAccessFolderEmail 元素包含一个值，该值指定电子邮件文件夹的标识符，统一消息将通过电话读取邮件，如 GetUMProperties 操作 (UM Web 服务) 请求的响应中包含的内容。
ms.openlocfilehash: 2db1ca43168585d791d0d09a4042cf5af7a578e7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544505"
---
# <a name="telephoneaccessfolderemail-um-web-service"></a>TelephoneAccessFolderEmail（UM Web 服务）

**TelephoneAccessFolderEmail** 元素包含一个值，该值标识电子邮件文件夹的标识符，统一消息将通过电话读取邮件，如 [GetUMProperties](getumproperties-operation-um-web-service.md)操作 (UM Web 服务) 请求的响应中包含的内容。 
  
[GetUMPropertiesResponse（UM Web 服务）](getumpropertiesresponse-um-web-service.md)
  
[TelephoneAccessFolderEmail（UM Web 服务）](telephoneaccessfolderemail-um-web-service.md)
  
```xml
<TelephoneAccessFolderEmail/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUMPropertiesResponse（UM Web 服务）](getumpropertiesresponse-um-web-service.md) <br/> |定义对 UM Web 服务请求 ([GetUMProperties) ](getumproperties-operation-um-web-service.md) 的响应。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUMProperties 操作（UM Web 服务）](getumproperties-operation-um-web-service.md)
  
[SetTelephoneAccessFolderEmail 操作（UM Web 服务）](settelephoneaccessfolderemail-operation-um-web-service.md)

