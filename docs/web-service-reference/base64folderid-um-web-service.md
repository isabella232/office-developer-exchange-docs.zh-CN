---
title: base64FolderId（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: base64FolderId 元素包含要指定为默认电子邮件文件夹的文件夹的标识符，统一消息通过该文件夹通过电话在 SetTelephoneAccessFolderEmail 操作 (UM Web 服务) 请求中读取邮件。
ms.openlocfilehash: 149ad55d0ab09f57b0dc3ace7eb0e17c96265e3f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518930"
---
# <a name="base64folderid-um-web-service"></a>base64FolderId（UM Web 服务）

**base64FolderId** 元素包含要指定为默认电子邮件文件夹的文件夹的标识符，统一消息通过 [SetTelephoneAccessFolderEmail](settelephoneaccessfolderemail-operation-um-web-service.md)操作 (UM Web 服务) 请求通过电话读取邮件。 
  
[SetTelephoneAccessFolderEmail（UM Web 服务）](settelephoneaccessfolderemail-um-web-service.md)
  
[base64FolderId（UM Web 服务）](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SetTelephoneAccessFolderEmail（UM Web 服务）](settelephoneaccessfolderemail-um-web-service.md) <br/> |定义设置电话访问电子邮件文件夹的请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值表示文件夹的 MAPI ID。
  
## <a name="remarks"></a>注解

若要设置电话访问电子邮件文件夹，请使用 [SetTelephoneAccessFolderEmail 操作 ](settelephoneaccessfolderemail-operation-um-web-service.md) (UM Web) 。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SetTelephoneAccessFolderEmail（UM Web 服务）](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmail 操作（UM Web 服务）](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[FindFolder 操作](findfolder-operation.md)
  
[FindItem 操作](finditem-operation.md)

