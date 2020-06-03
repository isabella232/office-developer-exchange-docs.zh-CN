---
title: ReportTemplate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReportTemplate
api_type:
- schema
ms.assetid: f528eee6-d5af-4745-8b00-a9834bf34be6
description: ReportTemplate 元素表示要获取的报告类型。
ms.openlocfilehash: 22f14d326032a30e5cb4c2c9e1aff390d98e95e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528697"
---
# <a name="reporttemplate"></a>ReportTemplate

**ReportTemplate**元素表示要获取的报告类型。 
  
```xml
<ReportTemplate>Summary or RecipientPath</ReportTemplate>
```

 **MessageTrackingReportTemplateType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |包含[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)的请求，以检索指定 ID 的完整邮件跟踪报告。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**ReportTemplate**元素的可能值。 
  
**ReportTemplate 元素值**

|**值**|**说明**|
|:-----|:-----|
|总结  <br/> |指定报告将显示邮件的所有收件人以及邮件到每个收件人的传递状态。  <br/> |
|RecipientPath  <br/> |指定对于单个收件人，报告将显示所发生事件的完整历史记录。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

