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
description: ConvertId 元素定义转换支持 Exchange 格式之间的项目和文件夹标识符的请求。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 956f6464fd9013f9e72d2915f21c3b011d0add5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753593"
---
# <a name="convertid"></a>ConvertId

**ConvertId**元素定义转换支持 Exchange 格式之间的项目和文件夹标识符的请求。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 **ConvertIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**DestinationFormat** <br/> |描述将返回所有已转换的标识符的标识符格式。 DestinationFormat 由 IdFormatType 描述。  <br/> |
   
#### <a name="destinationformat-attribute"></a>DestinationFormat 属性

|**值**|**说明**|
|:-----|:-----|
|**EwsLegacyId** <br/> |表示用于初始发行版 Exchange 2007 中提供的 Exchange Web 服务标识符的标识符格式。  <br/> |
|**EwsId** <br/> |表示用于启动与 Exchange Server 2007 SP1 的 Exchange Web 服务标识符的标识符格式。  <br/> |
|**EntryId** <br/> |表示的 MAPI 标识符，如 PR_ENTRYID 属性中所示。  <br/> |
|**HexEntryId** <br/> |代表可用性日历事件标识符。 这是 PR_ENTRYID 属性的十六进制编码表示形式。  <br/> |
|**StoreId** <br/> |表示 Exchange 存储区标识符。  <br/> |
|**OwaId** <br/> |代表 Outlook Web Access 标识符格式。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |包含要转换的源标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ConvertId 操作](convertid-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[转换标识符](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

