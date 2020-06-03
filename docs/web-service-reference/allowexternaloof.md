---
title: AllowExternalOof
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowExternalOof
api_type:
- schema
ms.assetid: e5387172-5b92-4bb1-8394-180e9c7ff771
description: AllowExternalOof 元素包含一个值，该值标识向其发送外部外出（OOF）邮件的人员。
ms.openlocfilehash: e4934bc4bc86e1f9f764279a13ecaeca073d9e5d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464810"
---
# <a name="allowexternaloof"></a>AllowExternalOof

**AllowExternalOof**元素包含一个值，该值标识向其发送外部外出（OOF）邮件的人员。 
  
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

|**元素**|**描述**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |包含用户的响应结果和 OOF 设置。  <br/> |
   
## <a name="text-value"></a>文本值

此元素需要一个文本值。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|**无** <br/> |向用户发送邮件的邮箱用户组织外部的电子邮件发件人将不会收到外部 OOF 邮件响应。  <br/> |
|**叫做** <br/> |如果邮箱用户的组织外部的电子邮件发件人向用户发送邮件，则仅会收到外部 OOF 邮件响应（如果发件人位于用户的 Exchange 存储联系人列表中）。  <br/> |
|**All** <br/> |将邮件发送给用户的邮箱用户的组织外部的电子邮件发件人将收到外部 OOF 邮件响应。  <br/> |
   
## <a name="remarks"></a>备注

此元素与[ExternalAudience](externalaudience.md)元素共享相同的类型。 
  
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

