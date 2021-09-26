---
title: RequestServerVersion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RequestServerVersion
api_type:
- schema
ms.assetid: af4032d5-42b3-463e-9d0a-8236d78e5b75
description: RequestServerVersion 元素包含版本控制信息，用于标识要针对请求的架构版本。
ms.openlocfilehash: 4f01d5fcc2a2e08d426efc8d1f0a193d6139a038
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541873"
---
# <a name="requestserverversion"></a>RequestServerVersion

**RequestServerVersion** 元素包含版本控制信息，用于标识要针对请求的架构版本。 
  
```XML
<RequestServerVersion Version=""/>
```

 **ExchangeVersionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|版本  <br/> |描述要针对请求的版本。 当目标服务器版本是自 2010 Exchange版本时，此属性Exchange Server必需。  <br/> |
   
#### <a name="version-attribute-values"></a>版本属性值

|**值**|**说明**|
|:-----|:-----|
|Exchange2007  <br/> |面向 2007 年 2 月Exchange版本的架构文件。  <br/> |
|Exchange2007_SP1  <br/> |针对 Exchange 2007 Service Pack 1 (SP1) 、Exchange 2007 Service Pack 2 (SP2) 和 Exchange 2007 Service Pack 3 (SP3) 的架构文件。  <br/> |
|Exchange2010  <br/> |面向 2010 Exchange文件。  <br/> |
|Exchange2010_SP1  <br/> |面向 Exchange 2010 Service Pack 1 sp1 (架构) 。  <br/> |
|Exchange2010_SP2  <br/> |面向 Exchange 2010 Service Pack 2 (SP2) 和 Exchange 2010 Service Pack 3 (SP3) 的架构文件。  <br/> |
|Exchange2013  <br/> |面向 2013 Exchange文件。  <br/> |
|Exchange2013_SP1  <br/> |面向 Exchange 2013 Service Pack 1 (SP1) 。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

**RequestServerVersion** 元素位于 SOAP 标头中。 
  
## <a name="remarks"></a>说明

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


[版本控制请求](https://msdn.microsoft.com/library/76877b0a-d2e5-4c74-9295-7b445a41d46a%28Office.15%29.aspx)

