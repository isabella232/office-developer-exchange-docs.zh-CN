---
title: ExceptionFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: ExceptionFieldURI 元素标识请求中的特定错误。 此元素仅用作 MessageXml 节点中的错误响应的一部分。
ms.openlocfilehash: 7368fd51e8eca2081b1fd50c86bce9ffa469c6b1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524327"
---
# <a name="exceptionfielduri"></a>ExceptionFieldURI

**ExceptionFieldURI** 元素标识请求中的特定错误。 此元素仅用作 MessageXml 节点中的错误响应 [的一](messagexml.md) 部分。 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 **ExceptionPropertyURIType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**FieldURI** <br/> |标识定期项目出现的属性。 此特性是必需的。  <br/> |
   
#### <a name="fielduri-attribute"></a>FieldURI 属性

|**值**|**说明**|
|:-----|:-----|
|attachment：Name  <br/> |将附件名称标识为包含错误。  <br/> |
|attachment：ContentType  <br/> |将内容类型标识为包含错误。  <br/> |
|attachment：Content  <br/> |将内容标识为包含错误。  <br/> |
|recurrence：Month  <br/> |将月字段标识为包含错误。  <br/> |
|recurrence：DayOfWeekIndex  <br/> |将星期中的索引日标识为包含错误。  <br/> |
|recurrence：DaysOfWeek  <br/> |将 DaysOfWeek 属性标识为包含错误。  <br/> |
|recurrence：DayOfMonth  <br/> |将 DayOfMonth 标识为包含错误。  <br/> |
|recurrence：Interval  <br/> |将间隔标识为包含错误。  <br/> |
|recurrence：NumberOfOccurrences  <br/> |标识包含错误的发生次数。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
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

