---
title: FindMailboxStatisticsByKeywordsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d3835800-8887-43db-9a8a-fe3cfea7a863
description: FindMailboxStatisticsByKeywordsResponseMessage 元素指定 FindMailboxStatisticsByKeywords 请求的响应消息。
ms.openlocfilehash: 704eebbf82db2871ab36be8e5b30c88c6959baa5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44525974"
---
# <a name="findmailboxstatisticsbykeywordsresponsemessage"></a>FindMailboxStatisticsByKeywordsResponseMessage

**FindMailboxStatisticsByKeywordsResponseMessage**元素指定**FindMailboxStatisticsByKeywords**请求的响应消息。 
  
```XML
<FindMailboxStatisticsByKeywordsResponseMessage ResponseClass=" Success | Warning | Error ">
    <MailboxStatisticsSearchResult/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindMailboxStatisticsByKeywordsResponseMessage>
```

 **FindMailboxStatisticsByKeywordsResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|ResponseClass  <br/> |指定响应类。  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**值**|**说明**|
|:-----|:-----|
|成功  <br/> |指示成功。  <br/> |
|警告  <br/> |指示警告。  <br/> |
|错误  <br/> |指示错误。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md) <br/> |指定邮箱搜索的结果。  <br/> |
|[MessageText](messagetext.md) <br/> |提供响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供有关请求的状态信息。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，并已保留以供将来使用。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供其他错误响应信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |指定响应消息的数组。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |消息 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

