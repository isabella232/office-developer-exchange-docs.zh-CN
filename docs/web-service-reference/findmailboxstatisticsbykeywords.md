---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: FindMailboxStatisticsByKeywords 元素指定按关键字搜索邮箱统计信息的请求。
ms.openlocfilehash: 3f84b0c3bb2a4a0a2a164b9e9120c3505073417e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546502"
---
# <a name="findmailboxstatisticsbykeywords"></a>FindMailboxStatisticsByKeywords

**FindMailboxStatisticsByKeywords** 元素指定按关键字搜索邮箱统计信息的请求。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailboxes (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) <br/> |包含受保留影响的邮箱数组。  <br/> |
|[Keywords](keywords-ex15websvcsotherref.md) <br/> |指定搜索的关键字。  <br/> |
|[Language](language.md) <br/> |包含用于搜索查询的语言。  <br/> |
|[发件人](senders.md) <br/> |指定 SMTP 地址的数组。  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |指定邮件的收件人数组。  <br/> |
|[FromDate](fromdate.md) <br/> |指定邮件的发送日期。  <br/> |
|[ToDate](todate.md) <br/> |指定邮件的接收日期。  <br/> |
|[MessageTypes](messagetypes.md) <br/> |指定要搜索的邮件数组。  <br/> |
|[SearchDumpster](searchdumpster.md) <br/> |指定是否搜索已删除的项目。  <br/> |
|[IncludePersonalArchive](includepersonalarchive.md) <br/> |指定是否在搜索中包括个人存档。  <br/> |
|[IncludeUnsearchableItems](includeunsearchableitems.md) <br/> |指定是否包括无法搜索的项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

