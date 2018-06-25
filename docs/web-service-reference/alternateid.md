---
title: AlternateId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: AlternateId 元素描述要转换请求和响应中的转换标识符的结果中的标识符。
ms.openlocfilehash: e4d29087b63b52638dd93e4e3b643cdee39a5b97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753138"
---
# <a name="alternateid"></a>AlternateId

**AlternateId**元素描述要转换请求和响应中的转换标识符的结果中的标识符。 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |介绍[ConvertId 操作](convertid-operation.md)请求中的源标识符以及[ConvertId 操作](convertid-operation.md)响应中的目标标识符。  <br/> |
|格式  <br/> |介绍[ConvertId 操作](convertid-operation.md)请求中的源格式以及[ConvertId 操作](convertid-operation.md)响应中的目标格式。 请求中的[ConvertId](convertid.md)元素的**DestinationFormat**属性描述了目标格式。 此属性是类型**IdFormatType**。  <br/> |
|Mailbox  <br/> |介绍邮箱主要简单邮件传输协议 (SMTP) 地址包含翻译的标识符。  <br/> |
|IsArchive  <br/> |指示标识符是否表示存档的项目或文件夹。 值为**true**指示标识符表示存档的项目或文件夹。 此属性是可选的。  <br/> |
   
#### <a name="format-attribute-values"></a>Format 属性值

|**值**|**说明**|
|:-----|:-----|
|EwsLegacyId  <br/> |描述所产生的 Exchange Web 服务的初始发行版本的 Exchange 2007 中的标识符。  <br/> |
|EwsId  <br/> |描述所产生的开头 Exchange 2007 SP1 的 Exchange Web 服务的标识符。  <br/> |
|EntryId  <br/> |描述 MAPI 标识符，如**PR_ENTRYID**属性中所示。  <br/> |
|HexEntryId  <br/> |介绍**PR_ENTRYID**属性的十六进制编码表示形式。 这是可用性日历事件标识符的格式。  <br/> |
|StoreId  <br/> |描述 Exchange 存储区标识符。  <br/> |
|OwaId  <br/> |介绍 Outlook Web App 标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |包含状态和[ConvertId 操作](convertid-operation.md)请求的结果。  <br/> |
|[SourceIds](sourceids.md) <br/> |包含要转换的源标识符。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

**AlternateId**元素介绍两个标识符、 在[ConvertId 操作](convertid-operation.md)要求中，要转换的源标识符和[ConvertIdResponse](convertidresponse.md)元素中转换后的标识符。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

||||
|:-----|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |消息架构  <br/> |类型架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ConvertId 操作](convertid-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [转换标识符](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

