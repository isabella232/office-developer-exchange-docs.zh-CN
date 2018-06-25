---
title: UserConfigurationProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationProperties
api_type:
- schema
ms.assetid: c143a6ec-62ad-4d48-b844-b1ad88054bc1
description: UserConfigurationProperties 元素指定要获取 GetUserConfiguration 操作中的属性类型。
ms.openlocfilehash: 4f993765bb7c36f28a41a3f2fa7e28698a3f709e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838464"
---
# <a name="userconfigurationproperties"></a>UserConfigurationProperties

**UserConfigurationProperties**元素指定要获取 GetUserConfiguration 操作中的属性类型。 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 **UserConfigurationPropertyType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserConfiguration](getuserconfiguration.md) <br/> |指定要获取的用户配置对象的请求。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**UserConfigurationProperties**元素的可能值。 
  
|**值**|**说明**|
|:-----|:-----|
|Id  <br/> |指定的 identifier 属性。  <br/> |
|Dictionary  <br/> |指定词典属性类型。  <br/> |
|XmlData  <br/> |指定属性的 XML 数据的类型。  <br/> |
|BinaryData  <br/> |指定二进制数据属性类型。  <br/> |
|所有  <br/> |指定标识符、 字典、 XML 数据和二进制数据属性类型。  <br/> |
   
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

