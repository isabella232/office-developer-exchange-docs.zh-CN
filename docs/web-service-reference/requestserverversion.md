---
title: RequestServerVersion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: RequestServerVersion 元素包含标识目标的请求的架构版本的版本控制信息。
ms.openlocfilehash: 0092d90a5fc479363f6d774b793c7148ad29f21c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827143"
---
# <a name="requestserverversion"></a>RequestServerVersion

**RequestServerVersion**元素包含标识目标的请求的架构版本的版本控制信息。 
  
```XML
<RequestServerVersion Version=""/>
```

 **ExchangeVersionType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|版本  <br/> |描述到请求的目标的版本。 目标服务器版本的 Exchange Server 2010 开头的 Exchange 版本时，此属性是必需的。  <br/> |
   
#### <a name="version-attribute-values"></a>版本属性值

|**值**|**说明**|
|:-----|:-----|
|Exchange2007  <br/> |目标初始发行版 Exchange 2007 的架构文件。  <br/> |
|Exchange2007_SP1  <br/> |面向 Exchange 2007 Service Pack 1 (SP1)、 Exchange 2007 Service Pack 2 (SP2) 和 Exchange 2007 Service Pack 3 (SP3) 的架构文件。  <br/> |
|Exchange2010  <br/> |面向 Exchange 2010 的架构文件。  <br/> |
|Exchange2010_SP1  <br/> |面向 Exchange 2010 Service Pack 1 (SP1) 的架构文件。  <br/> |
|Exchange2010_SP2  <br/> |面向 Exchange 2010 Service Pack 2 (SP2) 和 Exchange 2010 Service Pack 3 (SP3) 的架构文件。  <br/> |
|Exchange2013  <br/> |面向 Exchange 2013 的架构文件。  <br/> |
|Exchange2013_SP1  <br/> |面向 Exchange 2013 Service Pack 1 (SP1) 的架构文件。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

**RequestServerVersion**元素位于的 SOAP 标头。 
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[版本控制请求](http://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

