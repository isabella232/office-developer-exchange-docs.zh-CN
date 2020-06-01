---
title: GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: GetServerTimeZones 元素是请求中的根元素，用于检索来自 Exchange 服务器的时区定义。
ms.openlocfilehash: 797e4543c94b0628242bcf544fe9a735ebaa5a63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460937"
---
# <a name="getservertimezones"></a>GetServerTimeZones

**GetServerTimeZones**元素是请求中的根元素，用于检索来自 Exchange 服务器的时区定义。 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |指定[GetServerTimeZones 操作](getservertimezones-operation.md)是返回完整定义还是仅返回每个时区的名称和标识符。 此特性是可选的。 默认值为 **true** 。  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a>ReturnFullTimeZoneData 属性

|**值**|**说明**|
|:-----|:-----|
|**true** <br/> |返回每个时区的完整定义。  <br/> |
|**该值** <br/> |仅返回每个时区的名称和标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[Id](ids.md) <br/> |包含时区定义标识符的数组，该数组指定请求的时区定义。 此元素为可选。 如果此元素未包含在[GetServerTimeZones 操作](getservertimezones-operation.md)请求中，则会在响应中返回服务器上可用的所有时区定义。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetServerTimeZones 操作](getservertimezones-operation.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

