---
title: DeletedOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeletedOccurrence
api_type:
- schema
ms.assetid: ff24ea15-0cd7-407d-a378-73ec16451870
description: DeletedOccurrence 元素表示定期日历项目的已删除事件。
ms.openlocfilehash: 69e77f86097fe7037fc217806e4ef1b33b99c549
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542482"
---
# <a name="deletedoccurrence"></a>DeletedOccurrence

**DeletedOccurrence** 元素表示定期日历项目的已删除事件。 
  
```xml
<DeletedOccurrence>
   <Start/>
</DeletedOccurrence>
```

 **DeletedOccurrenceInfoType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Start](start.md) <br/> |表示定期日历项目的已删除事件的开始时间。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DeletedOccurrences](deletedoccurrences.md) <br/> |包含定期日历项目的已删除事件的数组。  <br/> |
   
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

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)  
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)

