---
title: ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: ConvertId 元素定义了在受支持的 Exchange 格式之间转换项目和文件夹标识符的请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: d421baf1f29fb59a8c6eb2b09e1fa0e8a38ffaa4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452536"
---
# <a name="convertid"></a>ConvertId

**ConvertId**元素定义了在受支持的 Exchange 格式之间转换项目和文件夹标识符的请求。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 **ConvertIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**DestinationFormat** <br/> |描述将为所有转换的标识符返回的标识符格式。 DestinationFormat 由 IdFormatType 描述。  <br/> |
   
#### <a name="destinationformat-attribute"></a>DestinationFormat 属性

|**值**|**说明**|
|:-----|:-----|
|**EwsLegacyId** <br/> |表示用于 exchange Web 服务标识符的标识符格式，这些标识符在 Exchange 2007 的初始发布版本中提供。  <br/> |
|**EwsId** <br/> |表示用于从 Exchange Server 2007 SP1 开始的 Exchange Web 服务标识符的标识符格式。  <br/> |
|**EntryId** <br/> |代表 MAPI 标识符，如 PR_ENTRYID 属性中所示。  <br/> |
|**HexEntryId** <br/> |表示可用性日历事件标识符。 这是 PR_ENTRYID 属性的十六进制编码表示形式。  <br/> |
|**StoreId** <br/> |表示 Exchange 存储区标识符。  <br/> |
|**OwaId** <br/> |表示 Outlook Web Access 标识符格式。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |包含要转换的源标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ConvertId 操作](convertid-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[转换标识符](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

