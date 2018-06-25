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
description: AllowExternalOof 元素包含一个值，该值标识向其发送外部外出 (OOF) 邮件。
ms.openlocfilehash: 1c87a51676bf6e44b2e650a4e973d0ab89a52e31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753142"
---
# <a name="allowexternaloof"></a>AllowExternalOof

**AllowExternalOof**元素包含一个值，该值标识向其发送外部外出 (OOF) 邮件。 
  
- [GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
- [AllowExternalOof](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 **ExternalAudience**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |包含响应结果和用户的 OOF 设置。  <br/> |
   
## <a name="text-value"></a>文本值

需要为此元素的文本值。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|**None** <br/> |邮箱用户的组织外部的电子邮件发件人将邮件发送到用户不会收到外部 OOF 消息响应。  <br/> |
|**已知** <br/> |邮箱用户的组织外部的电子邮件发件人发送给用户的消息将仅接收外部 OOF 消息响应如果发件人是用户的 Exchange 中存储的联系人列表。  <br/> |
|**All** <br/> |邮箱用户的组织外部的电子邮件发件人将邮件发送到用户将收到外部 OOF 消息响应。  <br/> |
   
## <a name="remarks"></a>注解

此元素共享[ExternalAudience](externalaudience.md)元素类型相同。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserOofSettings 操作](getuseroofsettings-operation.md) 
- [SetUserOofSettings 操作](setuseroofsettings-operation.md)

