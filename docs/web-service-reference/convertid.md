---
title: ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: ConvertId 元素定义一个请求，用于将项目标识符和文件夹标识符转换为受支持的Exchange格式。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: fe7d46697ba72ba6458136541488f5cd498169f4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545557"
---
# <a name="convertid"></a>ConvertId

**ConvertId** 元素定义一个请求，用于将项目标识符和文件夹标识符转换为受支持的Exchange格式。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。 
  
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
|**DestinationFormat** <br/> |描述将为所有转换后的标识符返回的标识符格式。 DestinationFormat 由 IdFormatType 描述。  <br/> |
   
#### <a name="destinationformat-attribute"></a>DestinationFormat 属性

|**值**|**说明**|
|:-----|:-----|
|**EwsLegacyId** <br/> |表示用于 2007 Exchange发布版本中提供的 Web 服务标识符的标识符Exchange格式。  <br/> |
|**EwsId** <br/> |表示从 2007 SP1 Exchange Web 服务标识符Exchange Server标识符格式。  <br/> |
|**EntryId** <br/> |表示 MAPI 标识符，如 PR_ENTRYID 属性。  <br/> |
|**HexEntryId** <br/> |表示可用性日历事件标识符。 这是一个十六进制编码的 PR_ENTRYID 表示形式。  <br/> |
|**StoreId** <br/> |表示Exchange标识符。  <br/> |
|**OwaId** <br/> |代表 Outlook Web Access 标识符格式。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |包含要转换的源标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

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

