---
title: SearchMailboxes 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a67c1d8-d021-4e68-aa62-35f7d9c2edc7
description: 查找信息 SearchMailboxes EWS 操作。
ms.openlocfilehash: 141ea466a24f3cb400a8e0b63e2162c1eae5d7f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827296"
---
# <a name="searchmailboxes-operation"></a>SearchMailboxes 操作

查找有关**SearchMailboxes** EWS 操作的信息。 
  
**SearchMailboxes**操作搜索词的项的邮箱中的邮箱项目。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-searchmailboxes-operation"></a>使用 SearchMailboxes 操作

**SearchMailboxes**操作可以使用多个同时搜索查询执行发现搜索在多个邮箱。 结果可以是任一统计信息的次数发生搜索词，也包含搜索词的项的预览。 
  
### <a name="searchmailboxes-operation-soap-headers"></a>SearchMailboxes 操作 SOAP 标头

**SearchMailboxes**操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |标识服务器角色所需顺序呼叫者发出请求。 适用于请求此标头。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 适用于请求此标头。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应该请求的服务器的版本。 适用于响应此标头。  <br/> |
   
## <a name="searchmailboxes-operation-request-example-search-mailboxes-for-number-of-search-term-hits"></a>SearchMailboxes 操作请求示例： 搜索邮箱搜索术语命中数

**SearchMailboxes**操作请求的下面的示例演示如何使用两个不同的查询搜索术语显示每个邮箱中有关多少次的统计信息的三个不同的邮箱。 
  
> [!NOTE]
> 本示例中，[查询](query.md)元素是 intentionaly 留空。 此时将显示如何成功的请求可包含错误条件，在每个邮箱搜索基础。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SearchMailboxes>
         <m:SearchQueries>
            <t:MailboxQuery>
               <t:Query>Test Item</t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=12311a742f0e47e392c8201a60d13ecf-Steve</t:Mailbox>
                     <t:SearchScope>All</t:SearchScope>
                  </t:MailboxSearchScope>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=f00c9f70539844beb52341d8f40c572e-Antho</t:Mailbox>
                     <t:SearchScope>PrimaryOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
            <t:MailboxQuery>
               <t:Query></t:Query>
               <t:MailboxSearchScopes>
                  <t:MailboxSearchScope>
                     <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=accba4fd5ddf12214a0e82ce1645f4e-Danie</t:Mailbox>
                     <t:SearchScope>ArchiveOnly</t:SearchScope>
                  </t:MailboxSearchScope>
               </t:MailboxSearchScopes>
            </t:MailboxQuery>
         </m:SearchQueries>
         <m:ResultType>StatisticsOnly</m:ResultType>
      </m:SearchMailboxes>
   </soap:Body>
</soap:Envelope>

```

请求 SOAP 正文包含以下元素：
  
- [SearchMailboxes](searchmailboxes.md)
    
- [SearchQueries](searchqueries.md)
    
- [MailboxQuery](mailboxquery.md)
    
- [Query](query.md)
    
- [MailboxSearchScopes](mailboxsearchscopes.md)
    
- [MailboxSearchScope](mailboxsearchscope.md)
    
- [邮箱 (字符串)](mailbox-string.md)
    
- [SearchScope](searchscope.md)
    
- [ResultType](resulttype.md)
    
## <a name="successful-searchmailboxes-operation-response"></a>成功 SearchMailboxes 操作响应

下面的示例演示成功响应**SearchMailboxes**操作请求获取统计信息的目标邮箱中找到搜索词的次数。 上一次查询包含空的**Query**元素，其中显示失败的邮箱搜索。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:SearchMailboxesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=35181a94327e392c8201a60d13ecf-Steve</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                           <t:MailboxSearchScope>
                              <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=f00c9f789572-beb04001d8f40c572e-Antho</t:Mailbox>
                              <t:SearchScope>PrimaryOnly</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>2</t:ItemCount>
                  <t:Size>20206</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:KeywordStats>
                     <t:KeywordStat>
                        <t:Keyword>Test Item</t:Keyword>
                        <t:ItemHits>2</t:ItemHits>
                        <t:Size>20206</t:Size>
                     </t:KeywordStat>
                  </t:KeywordStats>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYPDLT)/cn=Recipients/cn=accba4as3df234234a0e82ce1645f4e-Danie</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>The search query can't be empty.</t:ErrorMessage>
                        <t:IsArchive>true</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

响应 SOAP 正文中包含以下元素：
  
- [SearchMailboxesResponse](searchmailboxesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SearchMailboxesResponseMessage](searchmailboxesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SearchMailboxesResult](searchmailboxesresult.md)
    
- [SearchQueries](searchqueries.md)
    
- [MailboxQuery](mailboxquery.md)
    
- [Query](query.md)
    
- [MailboxSearchScopes](mailboxsearchscopes.md)
    
- [MailboxSearchScope](mailboxsearchscope.md)
    
- [邮箱 (字符串)](mailbox-string.md)
    
- [SearchScope](searchscope.md)
    
- [ResultType](resulttype.md)
    
- [ItemCount](itemcount.md)
    
- [大小 (long)](size-long.md)
    
- [PageItemCount](pageitemcount.md)
    
- [KeywordStats](keywordstats.md)
    
- [KeywordStat](keywordstat.md)
    
- [关键字](keyword.md)
    
- [ItemHits](itemhits.md)
    
- [FailedMailboxes](failedmailboxes.md)
    
- [FailedMailbox](failedmailbox.md)
    
- [邮箱 (字符串)](mailbox-string.md)
    
- [错误代码 (int)](errorcode-int.md)
    
- [ErrorMessage](errormessage.md)
    
- [IsArchive](isarchive.md)
    
## <a name="searchmailboxes-operation-error-response"></a>SearchMailboxes 操作错误响应

下面的示例演示对**SearchMailboxes**操作请求错误响应。 这是对搜索邮箱的邮箱标识符时不正确的请求的响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:SearchMailboxesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:SearchMailboxesResponseMessage ResponseClass="Error">
               <m:MessageText>No mailbox is specified for search operation. If specified in the request, 
               then it could be due to permission issue.</m:MessageText>
               <m:ResponseCode>ErrorInvalidOperation</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
               <m:SearchMailboxesResult>
                  <t:SearchQueries>
                     <t:MailboxQuery>
                        <t:Query>subject:Test Item</t:Query>
                        <t:MailboxSearchScopes>
                           <t:MailboxSearchScope>
                              <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                              <t:SearchScope>All</t:SearchScope>
                           </t:MailboxSearchScope>
                        </t:MailboxSearchScopes>
                     </t:MailboxQuery>
                  </t:SearchQueries>
                  <t:ResultType>StatisticsOnly</t:ResultType>
                  <t:ItemCount>0</t:ItemCount>
                  <t:Size>0</t:Size>
                  <t:PageItemCount>0</t:PageItemCount>
                  <t:PageItemSize>0</t:PageItemSize>
                  <t:FailedMailboxes>
                     <t:FailedMailbox>
                        <t:Mailbox>sbrown@contoso.com</t:Mailbox>
                        <t:ErrorCode>0</t:ErrorCode>
                        <t:ErrorMessage>No mailbox is specified for search operation. If specified in the request, 
                        then it could be due to permission issue.</t:ErrorMessage>
                        <t:IsArchive>false</t:IsArchive>
                     </t:FailedMailbox>
                  </t:FailedMailboxes>
               </m:SearchMailboxesResult>
            </m:SearchMailboxesResponseMessage>
         </m:ResponseMessages>
      </m:SearchMailboxesResponse>
   </s:Body>
</s:Envelope>

```

错误响应 SOAP 正文包含以下元素：
  
- [SearchMailboxesResponse](searchmailboxesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SearchMailboxesResponseMessage](searchmailboxesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SearchMailboxesResult](searchmailboxesresult.md)
    
- [SearchQueries](searchqueries.md)
    
- [MailboxQuery](mailboxquery.md)
    
- [Query](query.md)
    
- [MailboxSearchScopes](mailboxsearchscopes.md)
    
- [MailboxSearchScope](mailboxsearchscope.md)
    
- [邮箱 (字符串)](mailbox-string.md)
    
- [SearchScope](searchscope.md)
    
- [ResultType](resulttype.md)
    
- [ItemCount](itemcount.md)
    
- [大小 (long)](size-long.md)
    
- [PageItemCount](pageitemcount.md)
    
- [PageItemSize](pageitemsize.md)
    
- [FailedMailboxes](failedmailboxes.md)
    
- [FailedMailbox](failedmailbox.md)
    
- [邮箱 (字符串)](mailbox-string.md)
    
- [错误代码 (int)](errorcode-int.md)
    
- [ErrorMessage](errormessage.md)
    
- [IsArchive](isarchive.md)
    
通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。
  
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS 操作](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes 操作](getsearchablemailboxes-operation.md)
    
- [SetHoldOnMailboxes 操作](setholdonmailboxes-operation.md)
    
- [GetHoldOnMailboxes 操作](getholdonmailboxes-operation.md)
    
- [GetDiscoverySearchConfiguration 操作](getdiscoverysearchconfiguration-operation.md)
    
- [GetNonIndexableItemDetails 操作](getnonindexableitemdetails-operation.md)
    
- [GetNonIndexableItemStatistics 操作](getnonindexableitemstatistics-operation.md)
    

