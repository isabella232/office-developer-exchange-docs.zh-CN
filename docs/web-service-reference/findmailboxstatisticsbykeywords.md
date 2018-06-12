---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: FindMailboxStatisticsByKeywords 元素指定按关键字搜索的邮箱统计信息的请求。
ms.openlocfilehash: e667f13b66e439dca88d73a5e05d74846183928c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754343"
---
# <a name="findmailboxstatisticsbykeywords"></a>FindMailboxStatisticsByKeywords

**FindMailboxStatisticsByKeywords**元素指定按关键字搜索的邮箱统计信息的请求。 
  
```XML
<FindMailboxStatisticsByKeywords>
    <Mailboxes/>
    <Keywords/>
    <Language/>
    <Senders/>
    <Recipients/>
    <FromDate/>
    <ToDate/>
    <MessageTypes/>
    <SearchDumpster/>
    <IncludePersonalArchive/>
    <IncludeUnsearchableItems/>
</FindMailboxStatisticsByKeywords>
```

 **FindMailboxStatisticsByKeywordsType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[邮箱 (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) <br/> |包含受保留的邮箱的数组。  <br/> |
|[Keywords](keywords-ex15websvcsotherref.md) <br/> |指定搜索的关键字。  <br/> |
|[Language](language.md) <br/> |包含用于搜索查询的语言。  <br/> |
|[发件人](senders.md) <br/> |指定 SMTP 地址的数组。  <br/> |
|[收件人 (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |指定的邮件收件人的数组。  <br/> |
|[FromDate](fromdate.md) <br/> |指定发送邮件的日期。  <br/> |
|[ToDate](todate.md) <br/> |指定收到邮件的日期。  <br/> |
|[MessageTypes](messagetypes.md) <br/> |指定要搜索消息的的数组。  <br/> |
|[SearchDumpster](searchdumpster.md) <br/> |指定是否在已删除项目中搜索。  <br/> |
|[IncludePersonalArchive](includepersonalarchive.md) <br/> |指定是否在搜索中包括个人存档。  <br/> |
|[IncludeUnsearchableItems](includeunsearchableitems.md) <br/> |指定是否包含无法搜索的项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

