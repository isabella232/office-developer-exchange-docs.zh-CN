---
title: OofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: OofSettings 元素包含外出（OOF）设置。
ms.openlocfilehash: c1b214fd8bfab5b7a82d41a5187cf6e0fc4ba79c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467191"
---
# <a name="oofsettings"></a>OofSettings

**OofSettings**元素包含外出（OOF）设置。 
  
[GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
[OofSettings](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 **UserOofSettings**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |包含用户的 OOF 状态。  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |包含一个值，该值确定要向其发送外部 OOF 邮件的人员。  <br/> |
|[持续时间（UserOofSettings）](duration-useroofsettings.md) <br/> |包含在[OofState](oofstate.md)元素设置为 "已**计划**" 时启用了 OOF 状态的持续时间。 如果将[OofState](oofstate.md)元素设置为 "**启用**" 或 "**禁用**"，则忽略此元素的值。  <br/> |
|[InternalReply](internalreply.md) <br/> |包含发送给用户域或受信任域中的其他用户的 OOF 响应。  <br/> |
|[ExternalReply](externalreply.md) <br/> |包含发送给收件人域或受信任域外部的地址的 OOF 响应。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |包含用户的响应结果和 OOF 设置。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserOofSettings 操作](getuseroofsettings-operation.md)
  
[SetUserOofSettings 操作](setuseroofsettings-operation.md)

