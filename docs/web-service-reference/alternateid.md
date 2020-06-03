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
description: AlternateId 元素描述要在请求中转换的标识符和响应中转换后的标识符的结果。
ms.openlocfilehash: 26df68bd814c2d323630c6bb40b4c31745017c71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527451"
---
# <a name="alternateid"></a>AlternateId

**AlternateId**元素描述要在请求中转换的标识符和响应中转换后的标识符的结果。 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |描述[ConvertId 操作](convertid-operation.md)请求中的源标识符，并描述[ConvertId 操作](convertid-operation.md)响应中的目标标识符。  <br/> |
|Format  <br/> |描述[ConvertId 操作](convertid-operation.md)请求中的源格式，并描述[ConvertId 操作](convertid-operation.md)响应中的目标格式。 目标格式由请求中的[ConvertId](convertid.md)元素的**DestinationFormat**属性描述。 此属性的类型为**IdFormatType**。  <br/> |
|邮箱  <br/> |描述邮箱主要简单邮件传输协议（SMTP）地址，该地址包含要翻译的标识符。  <br/> |
|IsArchive  <br/> |指示标识符是否表示存档的项或文件夹。 **如果值为 true** ，则表示标识符表示存档项或文件夹。 此特性是可选的。  <br/> |
   
#### <a name="format-attribute-values"></a>格式属性值

|**值**|**说明**|
|:-----|:-----|
|EwsLegacyId  <br/> |介绍 exchange 2007 的初始发布版本中的 Exchange Web 服务生成的标识符。  <br/> |
|EwsId  <br/> |介绍了 Exchange Web 服务从 Exchange 2007 SP1 开始生成的标识符。  <br/> |
|EntryId  <br/> |描述 MAPI 标识符，如**PR_ENTRYID**属性中所示。  <br/> |
|HexEntryId  <br/> |描述了**PR_ENTRYID**属性的十六进制编码表示形式。 这是可用性日历事件标识符的格式。  <br/> |
|StoreId  <br/> |描述 Exchange 存储标识符。  <br/> |
|OwaId  <br/> |介绍 Outlook Web App 标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |包含[ConvertId 操作](convertid-operation.md)请求的状态和结果。  <br/> |
|[SourceIds](sourceids.md) <br/> |包含要转换的源标识符。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

**AlternateId**元素描述两个标识符：要在[ConvertId 操作](convertid-operation.md)请求中转换的源标识符，以及[ConvertIdResponse](convertidresponse.md)元素中的已转换标识符。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

||||
|:-----|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |消息架构  <br/> |类型架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ConvertId 操作](convertid-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [转换标识符](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

