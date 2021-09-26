---
title: GetNonIndexableItemStatistics 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ed077877-9d98-4434-b8b6-a4a905e7f7a6
description: 查找有关 GetNonIndexableItemStatistics EWS 操作的信息。
ms.openlocfilehash: e95cd016f73c92a75d9f366527e58045497363d0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546236"
---
# <a name="getnonindexableitemstatistics-operation"></a>GetNonIndexableItemStatistics 操作

查找有关 **GetNonIndexableItemStatistics** EWS 操作的信息。 
  
**GetNonIndexableItemStatistics** 操作检索无法在邮箱中编制索引的项目数。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-getnonindexableitemstatistics-operation"></a>使用 GetNonIndexableItemStatistics 操作

**GetNonIndexableItemStatistics** 操作对无法编制索引的邮箱项目计数。 无法在发现搜索期间搜索无法编制索引的项目。 
  
### <a name="getnonindexableitemstatistics-operation-soap-headers"></a>GetNonIndexableItemStatistics 操作 SOAP 标头

**GetNonIndexableItemStatistics** 操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |标识调用方进行请求所需的服务器角色。 此标头适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。 此标头适用于响应。  <br/> |
   
## <a name="getnonindexableitemstatistics-operation-request-example-get-the-count-of-items-that-cannot-be-indexed-in-a-mailbox"></a>GetNonIndexableItemStatistics 操作请求示例：获取邮箱中无法编制索引的项目数

**GetNonIndexableItemStatistics** 操作请求的以下示例显示如何请求无法在邮箱中编制索引的项目数。 
  
> [!NOTE]
> 此示例中所有旧域名已缩短，以保持可读性。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemStatistics>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIDLT)/cn=Recipients/cn=3518cf-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemStatistics>
   </soap:Body>
</soap:Envelope>

```

请求 SOAP 正文包含以下元素：
  
- [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)
    
- [Mailboxes (NonEmptyArrayOfLegacyDNsType)](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [LegacyDN](legacydn.md)
    
- [SearchArchiveOnly](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemstatistics-operation-response"></a>成功的 GetNonIndexableItemStatistics 操作响应

以下示例显示成功响应 **GetNonIndexableItemStatistics** 操作请求，获取邮箱中无法编制索引的项目数。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0"
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemStatisticsResponse ResponseClass="Success" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemStatistics>
            <NonIndexableItemStatistic xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35181acf-Steve</Mailbox>
               <ItemCount>2</ItemCount>
            </NonIndexableItemStatistic>
         </NonIndexableItemStatistics>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

响应 SOAP 正文包含以下元素：
  
- [GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [NonIndexableItemStatistics](nonindexableitemstatistics.md)
    
- [NonIndexableItemStatistic](nonindexableitemstatistic.md)
    
- [邮箱 (字符串)](mailbox-string.md)
    
- [ItemCount](itemcount.md)
    
## <a name="getnonindexableitemstatistics-operation-error-response"></a>GetNonIndexableItemStatistics 操作错误响应

以下示例显示对 **GetNonIndexableItemStatistics** 操作请求的错误响应。 这是对请求的响应，请求获取无法从多个邮箱编制索引的项目数。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemStatisticsResponse ResponseClass="Error" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

错误响应 SOAP 正文包含以下元素：
  
- [GetNonIndexableItemStatisticsResponse](getnonindexableitemstatisticsresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
有关 EWS 通用且特定于此操作的其他错误代码，请参阅 [ResponseCode](responsecode.md)。
  
## <a name="see-also"></a>另请参阅

- [EWS 操作在Exchange](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes 操作](getsearchablemailboxes-operation.md)
    
- [SearchMailboxes 操作](searchmailboxes-operation.md)
    
- [GetHoldOnMailboxes 操作](getholdonmailboxes-operation.md)
    
- [SetHoldOnMailboxes 操作](setholdonmailboxes-operation.md)
    
- [GetDiscoverySearchConfiguration 操作](getdiscoverysearchconfiguration-operation.md)
    
- [GetNonIndexableItemDetails 操作](getnonindexableitemdetails-operation.md)
    

