---
title: GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: GetServerTimeZones 元素是请求从服务器检索时区定义的根Exchange元素。
ms.openlocfilehash: b710334e5778f8bc27ba7ac07c6bf9c2e2d3392e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533537"
---
# <a name="getservertimezones"></a>GetServerTimeZones

**GetServerTimeZones** 元素是请求从服务器检索时区定义的根Exchange元素。 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |指定 [GetServerTimeZones 操作](getservertimezones-operation.md) 是返回完整定义还是仅返回每个时区的名称和标识符。 此特性是可选的。 默认值为 **true** 。  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a>ReturnFullTimeZoneData 属性

|**值**|**说明**|
|:-----|:-----|
|**true** <br/> |返回每个时区的完整定义。  <br/> |
|**false** <br/> |仅返回每个时区的名称和标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Ids](ids.md) <br/> |包含指定请求的时区定义的时区定义标识符数组。 此元素为可选。 如果 [GetServerTimeZones](getservertimezones-operation.md) 操作请求中不包含此元素，响应中将返回服务器上可用的所有时区定义。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。
  
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

