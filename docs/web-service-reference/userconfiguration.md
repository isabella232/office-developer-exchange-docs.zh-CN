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
description: UserConfiguration 元素定义的单个用户配置对象。
ms.openlocfilehash: ce3eaa470ef592c5a8e5a7ef24c377bb2feeca2e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838461"
---
# <a name="userconfiguration"></a>UserConfiguration

**UserConfiguration**元素定义的单个用户配置对象。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[UserConfigurationName](userconfigurationname.md) <br/> |代表用户配置对象的名称。 创建用户配置对象时，必须使用此元素。  <br/> |
|[ItemId](itemid.md) <br/> |定义的用户配置对象项标识符。  <br/> |
|"词典" <br/> |定义一组用户配置对象的词典属性条目。  <br/> |
|[XmlData](xmldata.md) <br/> |包含 XML 数据属性的用户配置对象的新内容。  <br/> |
|[BinaryData](binarydata.md) <br/> |包含二进制数据属性的用户配置对象的新内容。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateUserConfiguration](createuserconfiguration.md) <br/> |表示要创建用户配置对象的请求。  <br/> |
|[GetUserConfigurationResponseMessage](getuserconfigurationresponsemessage.md) <br/> |代表一个响应，其中返回的用户配置对象。  <br/> |
|[UpdateUserConfiguration](updateuserconfiguration.md) <br/> |表示要更新的用户配置对象的请求。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

