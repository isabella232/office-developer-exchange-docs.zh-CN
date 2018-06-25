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
description: OofSettings 元素包含的外出 (OOF) 设置。
ms.openlocfilehash: d71f068ff24af22da98b6b4de090ab26d3f74f26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826649"
---
# <a name="oofsettings"></a>OofSettings

**OofSettings**元素包含的外出 (OOF) 设置。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |包含用户的 OOF 状态。  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |包含一个值，确定外部 OOF 邮件发送到其。  <br/> |
|[持续时间 (UserOofSettings)](duration-useroofsettings.md) <br/> |包含如果[OofState](oofstate.md)元素设置为**计划**为其启用 OOF 状态的工期。 如果[OofState](oofstate.md)元素设置为**已启用**或**禁用**，则忽略此元素的值。  <br/> |
|[InternalReply](internalreply.md) <br/> |包含 OOF 响应发送给用户的域或受信任的域中其他用户。  <br/> |
|[ExternalReply](externalreply.md) <br/> |包含 OOF 响应发送给外部收件人的域或受信任的域的地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |包含响应结果和用户的 OOF 设置。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserOofSettings 操作](getuseroofsettings-operation.md)
  
[SetUserOofSettings 操作](setuseroofsettings-operation.md)

