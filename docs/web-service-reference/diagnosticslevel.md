---
title: DiagnosticsLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DiagnosticsLevel
api_type:
- schema
ms.assetid: 66794226-f5e0-44f0-8a0e-1f194bb0ba0f
description: DiagnosticsLevel 元素表示将用于派生报告的计时和性能信息。
ms.openlocfilehash: c7e74f324385ca76a58872e2e735ea2c5d926a53
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519798"
---
# <a name="diagnosticslevel"></a>DiagnosticsLevel

**DiagnosticsLevel** 元素表示将用于派生报告的计时和性能信息。 
  
```XML
<DiagnosticsLevel/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |包含要查找的邮件的类型的条件。  <br/> |
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |包含 [GetMessageTrackingReport](getmessagetrackingreport-operation.md) 操作的请求，以检索指定 ID 的完整邮件跟踪报告。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则代表字符串的文本值是必需的。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

