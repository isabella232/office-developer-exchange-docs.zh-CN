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
description: GetServerTimeZones 元素是从 Exchange 服务器中检索时区定义的请求中的根元素。
ms.openlocfilehash: 1ad503ff312497189f57bce9a3670571aedad5ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754688"
---
# <a name="getservertimezones"></a>GetServerTimeZones

**GetServerTimeZones**元素是从 Exchange 服务器中检索时区定义的请求中的根元素。 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |指定是否[GetServerTimeZones 操作](getservertimezones-operation.md)的完整定义或只返回名称和每个时区的标识符。 此属性是可选的。 默认值为 **true** 。  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a>ReturnFullTimeZoneData 属性

|**值**|**说明**|
|:-----|:-----|
|**true** <br/> |返回每个时区的完整定义。  <br/> |
|**false** <br/> |返回仅的名称和为每个时区的标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Id](ids.md) <br/> |包含指定的请求的所在的时区定义的时区定义标识符数组。 此元素是可选的。 如果此元素不包括[GetServerTimeZones 操作](getservertimezones-operation.md)请求中，可在服务器上的所有所在的时区定义的响应中都返回。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetServerTimeZones 操作](getservertimezones-operation.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

