---
title: ReplyBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ReplyBody
api_type:
- schema
ms.assetid: bb184144-3e4b-4419-a883-cc9fab1085e6
description: ReplyBody 元素包含 Out of Office (OOF) 消息和用于邮件的语言。
ms.openlocfilehash: 75af64277467246c7edcc2a48708bbf3f3c95c48
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517950"
---
# <a name="replybody"></a>ReplyBody

**ReplyBody** 元素包含 Out of Office (OOF) 消息和用于邮件的语言。 
  
```XML
<ReplyBody xml:lang="">
   <Message/>
</ReplyBody>
```

 **ReplyBody**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|xml：lang  <br/> |指定 **ReplyBody** 内容中使用的语言。 此特性是可选的。 此属性的可能值由 IETF RFC 3066 定义。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Message (Availability)](message-availability.md) <br/> |包含外出 OOF (响应) 。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[OutOfOffice](outofoffice.md) <br/> |定义 OOF 响应邮件和发送邮箱响应邮件的持续时间。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

此元素是必需的。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

