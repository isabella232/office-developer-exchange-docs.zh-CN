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
ms.openlocfilehash: 79909405179cec0d0b86ad12bf52031e1daeb790
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754176"
---
# <a name="exceptionfielduri"></a>ExceptionFieldURI

**ExceptionFieldURI**元素标识请求中的特定错误。 此元素仅用作[MessageXml](messagexml.md)节点中的错误响应的一部分。 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 **ExceptionPropertyURIType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**FieldURI** <br/> |标识定期项匹配项的属性。 此属性是必需的。  <br/> |
   
#### <a name="fielduri-attribute"></a>FieldURI 属性

|**值**|**说明**|
|:-----|:-----|
|附件： 名称  <br/> |标识为包含出错附件名称。  <br/> |
|附件： ContentType  <br/> |标识为包含错误的内容类型。  <br/> |
|附件： 内容  <br/> |标识为包含错误的内容。  <br/> |
|重复月：  <br/> |标识为包含错误 month 字段。  <br/> |
|定期： DayOfWeekIndex  <br/> |标识为包含错误的周索引的天。  <br/> |
|定期： DaysOfWeek  <br/> |标识为包含错误的 DaysOfWeek 属性。  <br/> |
|定期： DayOfMonth  <br/> |标识为包含错误 DayOfMonth。  <br/> |
|定期： 间隔  <br/> |标识为包含错误的时间间隔。  <br/> |
|定期： NumberOfOccurrences  <br/> |标识为包含错误的次数。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageXml](messagexml.md) <br/> |提供了其他错误响应信息。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

