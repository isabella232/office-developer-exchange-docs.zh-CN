---
title: AlternateId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: AlternateId 元素描述在请求中转换的标识符，以及响应中转换后的标识符的结果。
ms.openlocfilehash: 6346a45b48eb811cac705d8da85dc77e6c18262c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520939"
---
# <a name="alternateid"></a>AlternateId

**AlternateId** 元素描述在请求中转换的标识符，以及响应中转换后的标识符的结果。 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |描述 [ConvertId](convertid-operation.md) 操作请求中的源标识符，并描述 [ConvertId](convertid-operation.md) 操作响应中的目标标识符。  <br/> |
|格式  <br/> |介绍 [ConvertId](convertid-operation.md) 操作请求中的源格式，并介绍 ConvertId 操作响应 [中的目标](convertid-operation.md) 格式。 目标格式由请求中 [ConvertId](convertid.md)元素的 **DestinationFormat** 属性描述。 此属性的类型为 **IdFormatType**。  <br/> |
|邮箱  <br/> |描述邮箱主简单邮件传输 (SMTP) 包含要转换的标识符的地址。  <br/> |
|IsArchive  <br/> |指示标识符是否表示已存档的项目或文件夹。 true **值表示** 标识符表示已存档的项目或文件夹。 此特性是可选的。  <br/> |
   
#### <a name="format-attribute-values"></a>设置属性值的格式

|**值**|**说明**|
|:-----|:-----|
|EwsLegacyId  <br/> |介绍由 Exchange 2007 初始发行版中的 Web 服务Exchange标识符。  <br/> |
|EwsId  <br/> |介绍从 2007 SP1 Exchange Web 服务Exchange生成的标识符。  <br/> |
|EntryId  <br/> |描述 MAPI 标识符，如 **PR_ENTRYID** 属性。  <br/> |
|HexEntryId  <br/> |描述 PR_ENTRYID 属性的十 **六进制编码** 表示形式。 这是可用性日历事件标识符的格式。  <br/> |
|StoreId  <br/> |介绍Exchange标识符。  <br/> |
|OwaId  <br/> |描述Outlook Web App标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |包含 ConvertId 操作请求 [的状态和](convertid-operation.md) 结果。  <br/> |
|[SourceIds](sourceids.md) <br/> |包含要转换的源标识符。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

**AlternateId** 元素描述两个标识符：一个是在 [ConvertId](convertid-operation.md)操作请求中转换的源标识符，另一个是在 [ConvertIdResponse](convertidresponse.md)元素中转换的标识符。 
  
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

