---
title: base64FolderId （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: Base64FolderId 元素包含要指定为默认电子邮件文件夹的文件夹的标识符，统一消息在 SetTelephoneAccessFolderEmail 操作（UM web 服务）请求中通过电话读取邮件。
ms.openlocfilehash: ea31c7a0f93188e563bf95c4a3e6e91f0866746c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458045"
---
# <a name="base64folderid-um-web-service"></a>base64FolderId （UM web 服务）

**Base64FolderId**元素包含要指定为默认电子邮件文件夹的文件夹的标识符，统一消息在[SETTELEPHONEACCESSFOLDEREMAIL 操作（UM web 服务）](settelephoneaccessfolderemail-operation-um-web-service.md)请求中通过电话读取邮件。 
  
[SetTelephoneAccessFolderEmail （UM web 服务）](settelephoneaccessfolderemail-um-web-service.md)
  
[base64FolderId （UM web 服务）](base64folderid-um-web-service.md)
  
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
|[SetTelephoneAccessFolderEmail （UM web 服务）](settelephoneaccessfolderemail-um-web-service.md) <br/> |定义设置电话访问电子邮件文件夹的请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 该文本值表示文件夹的 MAPI ID。
  
## <a name="remarks"></a>备注

若要设置电话访问电子邮件文件夹，请使用[SetTelephoneAccessFolderEmail 操作（UM web 服务）](settelephoneaccessfolderemail-operation-um-web-service.md)。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SetTelephoneAccessFolderEmail （UM web 服务）](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmail 操作（UM web 服务）](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[FindFolder 操作](findfolder-operation.md)
  
[FindItem 操作](finditem-operation.md)

