---
title: OofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: OofSettings 元素包含 Out of Office (OOF) 设置。
ms.openlocfilehash: 0a612cacb69464dfda3c1f235c32f569d3e45775
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543168"
---
# <a name="oofsettings"></a>OofSettings

**OofSettings** 元素包含 Out of Office (OOF) 设置。 
  
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
|[ExternalAudience](externalaudience.md) <br/> |包含一个值，该值确定外部 OOF 邮件的发送对象。  <br/> |
|[Duration (UserOofSettings)](duration-useroofsettings.md) <br/> |包含当 [OofState](oofstate.md) 元素设置为 **Scheduled** 时启用 OOF 状态的持续时间。 如果 [OofState](oofstate.md) 元素设置为 **Enabled** 或 **Disabled，** 则忽略此元素的值。  <br/> |
|[InternalReply](internalreply.md) <br/> |包含发送给用户域或受信任域中其他用户的 OOF 响应。  <br/> |
|[ExternalReply](externalreply.md) <br/> |包含发送到收件人域或受信任域外部地址的 OOF 响应。  <br/> |
   
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

