---
title: UserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfiguration
api_type:
- schema
ms.assetid: 1811df99-ca5b-48a3-b160-b3fd70320c34
description: UserConfiguration 元素定义单个用户配置对象。
ms.openlocfilehash: 1217f5d591570c2d8df49a116b6bf35c243d1e0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468906"
---
# <a name="userconfiguration"></a>UserConfiguration

**UserConfiguration**元素定义单个用户配置对象。 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 **UserConfigurationType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UserConfigurationName](userconfigurationname.md) <br/> |表示用户配置对象的名称。 创建用户配置对象时，必须使用此元素。  <br/> |
|[ItemId](itemid.md) <br/> |定义 "用户配置对象" 项标识符。  <br/> |
|"词典" <br/> |为用户配置对象定义一组字典属性项。  <br/> |
|[XmlData](xmldata.md) <br/> |包含用户配置对象的 XML 数据属性内容。  <br/> |
|[BinaryData](binarydata.md) <br/> |包含用户配置对象的二进制数据属性内容。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateUserConfiguration](createuserconfiguration.md) <br/> |表示创建用户配置对象的请求。  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |表示返回用户配置对象的响应。  <br/> |
|[UpdateUserConfiguration](updateuserconfiguration.md) <br/> |表示一个更新用户配置对象的请求。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

