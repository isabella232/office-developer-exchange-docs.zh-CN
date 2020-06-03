---
title: TelephoneAccessFolderEmail （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- TelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 5d32ae22-bb9f-4352-a251-d516b66ff35b
description: TelephoneAccessFolderEmail 元素包含一个值，该值指定了统一消息将通过电话读取邮件的电子邮件文件夹的标识符，该文件夹包含在对 GetUMProperties 操作（UM web 服务）请求的响应中。
ms.openlocfilehash: 8da4065921b736313d4bbf5bb96edb51761a4bdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468626"
---
# <a name="telephoneaccessfolderemail-um-web-service"></a>TelephoneAccessFolderEmail （UM web 服务）

**TelephoneAccessFolderEmail**元素包含一个值，该值指定了统一消息将通过电话读取邮件的电子邮件文件夹的标识符，该文件夹包含在对[GETUMPROPERTIES 操作（UM web 服务）](getumproperties-operation-um-web-service.md)请求的响应中。 
  
[GetUMPropertiesResponse （UM web 服务）](getumpropertiesresponse-um-web-service.md)
  
[TelephoneAccessFolderEmail （UM web 服务）](telephoneaccessfolderemail-um-web-service.md)
  
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
|[GetUMPropertiesResponse （UM web 服务）](getumpropertiesresponse-um-web-service.md) <br/> |定义对[GetUMProperties 操作（UM web 服务）](getumproperties-operation-um-web-service.md)请求的响应。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUMProperties 操作（UM web 服务）](getumproperties-operation-um-web-service.md)
  
[SetTelephoneAccessFolderEmail 操作（UM web 服务）](settelephoneaccessfolderemail-operation-um-web-service.md)

