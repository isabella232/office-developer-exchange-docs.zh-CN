---
title: MessageTrackingReportId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageTrackingReportId
api_type:
- schema
ms.assetid: 9c604ca3-10fe-4760-b7fd-8b52f1a0c712
description: MessageTrackingReportId 元素按邮件 ID、找到邮件的组织、提交邮件的服务器以及唯一标识邮件的内部 ID 来表示邮件。
ms.openlocfilehash: 8ed8ddcfe20c9008a208035f2b101fb5241f432d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518258"
---
# <a name="messagetrackingreportid"></a>MessageTrackingReportId

**MessageTrackingReportId** 元素按邮件 ID、找到邮件的组织、提交邮件的服务器以及唯一标识邮件的内部 ID 来表示邮件。 
  
```XML
<MessageTrackingReportId/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |包含 [GetMessageTrackingReport](getmessagetrackingreport-operation.md) 操作的请求，以检索指定 ID 的完整邮件跟踪报告。  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |包含 [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) 元素的单个邮件结果。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则代表字符串的文本值是必需的。
  
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



[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

