---
title: ConnectionTimeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionTimeout
api_type:
- schema
ms.assetid: 14da68a0-bcca-4281-a774-47644baa4ee9
description: ConnectionTimeout 元素指定保持连接打开的分钟数。
ms.openlocfilehash: 671e3cf5466ee8b3543036811708bd7f54afdcce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463851"
---
# <a name="connectiontimeout"></a>ConnectionTimeout

**ConnectionTimeout**元素指定保持连接打开的分钟数。 
  
[GetStreamingEvents 操作](getstreamingevents-operation.md)
  
[ConnectionTimeout](connectiontimeout.md)
  
```xml
<ConnectionTimeout/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetStreamingEvents](getstreamingevents.md) <br/> |定义从流式连接获取事件通知的请求。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示一个整数，该整数描述将流式连接保持打开状态的最长时间（以分钟为单位）。 值必须介于1和30之间（含这两个值）。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetStreamingEvents 操作](getstreamingevents-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

