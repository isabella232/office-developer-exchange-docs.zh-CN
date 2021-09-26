---
title: MessageTrackingSearchResults
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageTrackingSearchResults
api_type:
- schema
ms.assetid: 6bf36f37-c2b3-40c1-a4df-31573ed8642a
description: MessageTrackingSearchResults 元素包含与搜索条件匹配的记录列表。
ms.openlocfilehash: d478bec8a898e03a7f90c7aab4d89b13add14e0a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542062"
---
# <a name="messagetrackingsearchresults"></a>MessageTrackingSearchResults

**MessageTrackingSearchResults** 元素包含与搜索条件匹配的记录列表。 
  
```XML
<MessageTrackingSearchResults>
   <MessageTrackingSearchResult/>
</MessageTrackingSearchResults>
```

 **ArrayOfFindMessageTrackingSearchResultType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |包含 [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) 元素的单个邮件结果。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |包含单个 [FindMessageTrackingReport](findmessagetrackingreport-operation.md) 操作请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

