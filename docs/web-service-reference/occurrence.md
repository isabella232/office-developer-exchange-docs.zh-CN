---
title: Occurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Occurrence
api_type:
- schema
ms.assetid: d292b99c-b896-40b7-be5d-2cb314c9481f
description: Occurrence 元素表示定期日历项目的单个修改事件。
ms.openlocfilehash: 465c02263eadfc74629a8e21ebccf076206ec0d2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518090"
---
# <a name="occurrence"></a>Occurrence

**Occurrence** 元素表示定期日历项目的单个修改事件。 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

**OccurrenceInfoType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |包含定期日历项目的已修改事件的唯一标识符和更改键。  <br/> |
|[Start](start.md) <br/> |表示定期日历项目的已修改事件的开始时间。  <br/> |
|[End ](end-ex15websvcsotherref.md) <br/> |表示定期日历项目的修改事件的结束时间。  <br/> |
|[OriginalStart](originalstart.md) <br/> |表示定期日历项目的已修改事件的原始开始时间。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |包含已修改的定期日历项目事件的集合，以便它们不同于定期主项目。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

