---
title: TimeZoneContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeZoneContext
api_type:
- schema
ms.assetid: 573c462b-aa1d-4ba0-8852-e3f48b26873b
description: TimeZoneContext 元素在 Simple Object Access Protocol (SOAP) 标头中用于指定时区定义，当为使用 Exchange Web 服务 (EWS) 创建、更新和检索的对象的 DateTime 属性分配时区时，该时区定义将用作默认值。
ms.openlocfilehash: a628d4a094e70f1190f2cc0eda8cc4416bc37860
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515171"
---
# <a name="timezonecontext"></a>TimeZoneContext

**TimeZoneContext** 元素在 Simple Object Access Protocol (SOAP) 标头中用于指定时区定义，当使用 Exchange Web 服务 (EWS) 创建、更新和检索的对象的 DateTime 属性分配时区时，该时区定义将用作默认值。 
  
```xml
<TimeZoneContext>
   <TimeZoneDefinition/>
</TimeZoneContext>
```

 **TimeZoneContextType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeZoneDefinition](timezonedefinition.md) <br/> |指定用于定义时区的时间段和转换。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

