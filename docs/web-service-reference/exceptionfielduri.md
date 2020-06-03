---
title: ExceptionFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: ExceptionFieldURI 元素标识请求中的特定错误。 此元素仅用作 MessageXml 节点中的错误响应的一部分。
ms.openlocfilehash: a47d44098f85d8bacb1e7a2c48a33e478e56c7ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454342"
---
# <a name="exceptionfielduri"></a>ExceptionFieldURI

**ExceptionFieldURI**元素标识请求中的特定错误。 此元素仅用作[MessageXml](messagexml.md)节点中的错误响应的一部分。 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 **ExceptionPropertyURIType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**FieldURI** <br/> |标识定期项目的事件的属性。 此特性是必需的。  <br/> |
   
#### <a name="fielduri-attribute"></a>FieldURI 属性

|**值**|**说明**|
|:-----|:-----|
|附件：名称  <br/> |将附件名称标识为包含错误。  <br/> |
|附件： ContentType  <br/> |将内容类型标识为包含一个错误。  <br/> |
|附件：内容  <br/> |将内容标识为包含错误。  <br/> |
|重复周期：月  <br/> |将 "月份" 字段标识为包含错误。  <br/> |
|重复周期： DayOfWeekIndex  <br/> |将星期索引的日期标识为包含错误。  <br/> |
|重复周期： DaysOfWeek  <br/> |将 DaysOfWeek 属性标识为包含一个错误。  <br/> |
|重复周期： DayOfMonth  <br/> |将 DayOfMonth 标识为包含错误。  <br/> |
|重复周期：间隔  <br/> |标识包含错误的间隔。  <br/> |
|重复周期： NumberOfOccurrences  <br/> |将发生次数标识为包含错误。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

