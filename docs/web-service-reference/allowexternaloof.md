---
title: AllowExternalOof
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AllowExternalOof
api_type:
- schema
ms.assetid: e5387172-5b92-4bb1-8394-180e9c7ff771
description: AllowExternalOof 元素包含一个值，该值标识 OOF 邮件Office (外部) 发送到谁。
ms.openlocfilehash: 7d2e34797af8a9e9d11570a5ea2e618db7630f0c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523222"
---
# <a name="allowexternaloof"></a>AllowExternalOof

**AllowExternalOof** 元素包含一个值，该值标识 OOF 邮件Office (外部) 发送到谁。 
  
- [GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
- [AllowExternalOof](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 **ExternalAudience**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |包含用户的响应结果和 OOF 设置。  <br/> |
   
## <a name="text-value"></a>文本值

此元素需要文本值。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|**无** <br/> |向用户发送邮件的邮箱用户组织外部的电子邮件发件人不会收到外部 OOF 邮件响应。  <br/> |
|**已知** <br/> |邮箱用户组织外部向用户发送邮件的电子邮件发件人将仅收到外部 OOF 邮件响应（如果发件人位于用户的应用商店Exchange列表中）。  <br/> |
|**全部** <br/> |向用户发送邮件的邮箱用户组织外部的电子邮件发件人将收到外部 OOF 邮件响应。  <br/> |
   
## <a name="remarks"></a>注解

此元素与 [ExternalAudience 元素共享同一](externalaudience.md) 类型。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserOofSettings 操作](getuseroofsettings-operation.md) 
- [SetUserOofSettings 操作](setuseroofsettings-operation.md)

