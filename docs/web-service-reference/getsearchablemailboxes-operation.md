---
title: GetSearchableMailboxes 操作
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: 查找有关 GetSearchableMailboxes EWS 操作的信息。
ms.openlocfilehash: e893a66eb1b638479eeccc6bd7548cb020f37243
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530837"
---
# <a name="getsearchablemailboxes-operation"></a>GetSearchableMailboxes 操作

> [!IMPORTANT]
> 从2020年4月1日起，GetSearchableMailboxes 操作将不再在 Exchange Online 中可用。 此操作不会受到 Exchange Server 内部部署版本的影响。 有关详细信息，请参阅[在 Exchange Online 中停用旧版电子数据展示工具](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api)。

查找有关**GetSearchableMailboxes** EWS 操作的信息。 
  
**GetSearchableMailboxes**操作获取用于发现搜索的可搜索邮箱的范围集合。 响应中返回的可搜索邮箱的范围由搜索筛选器和是否扩展通讯组成员资格决定。 

> [!NOTE] 
> 此操作旨在用于搜索筛选器，并仅检索前几千位;它并不用于详尽的检索。
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-getsearchablemailboxes-operation"></a>使用 GetSearchableMailboxes 操作

**GetSearchableMailboxes**操作获取有关可搜索邮箱的信息。 可以在请求中传递以下参数： 
  
- [过滤](searchfilter.md)-接受一个电子邮件别名作为参数。 
    
- [ExpandGroupMembership](expandgroupmembership.md) -指示是否在响应中返回的结果中扩展通讯组成员资格。 
    
如果搜索筛选器中设置的电子邮件别名是通讯组，且通讯组成员身份未扩展，则响应将包含通讯组的邮箱信息。 如果搜索筛选器中设置的电子邮件别名是通讯组，并且展开了通讯组成员身份，则响应将包含作为通讯组成员的每个邮箱的邮箱信息。 如果搜索筛选器包含单个用户的别名，则响应将包含单个用户的邮箱信息。 如果[GetSearchableMailboxes](getsearchablemailboxes.md)元素为空，则响应将包含所有可搜索的邮箱。 这与将空的[过滤](searchfilter.md)元素和[ExpandGroupMembership](expandgroupmembership.md)元素设置为**false**相同。
  
### <a name="getsearchablemailboxes-operation-soap-headers"></a>GetSearchableMailboxes 操作 SOAP 标头

**GetSearchableMailboxes**操作可以使用下表中列出的 SOAP 标头。 
  
|头名称|元素|说明|
|:-----|:-----|:-----|
|**Get-managementrole** <br/> |[Get-managementrole](managementrole.md) <br/> |标识调用方发出请求所需的服务器角色。 此标头适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器版本。 此标头适用于响应。  <br/> |
   
## <a name="getsearchablemailboxes-operation-request-example-request-information-about-a-distribution-group"></a>GetSearchableMailboxes 操作请求示例：请求有关通讯组的信息

以下示例的**GetSearchableMailboxes**操作请求显示如何获取 lolgroup 通讯组的邮箱信息。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetSearchableMailboxes>
         <m:SearchFilter>lolgroup</m:SearchFilter>
         <m:ExpandGroupMembership>false</m:ExpandGroupMembership>
      </m:GetSearchableMailboxes>
   </soap:Body>
</soap:Envelope>

```

请求 SOAP 正文包含以下元素：
  
- [GetSearchableMailboxes](getsearchablemailboxes.md)   
- [过滤](searchfilter.md)    
- [ExpandGroupMembership](expandgroupmembership.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-a-distribution-group"></a>成功的 GetSearchableMailboxes 操作响应：获取有关通讯组的信息

下面的示例演示对**GetSearchableMailboxes**操作请求的成功响应，以获取 lolgroup 通讯组的发现信息。 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Guid>33a408fe-2574-4e3b-49f5-5e1e000a3035</Guid>
               <PrimarySmtpAddress>LOLgroup@contoso.com</PrimarySmtpAddress>
               <IsExternalMailbox>false</IsExternalMailbox>
               <ExternalEmailAddress/>
               <DisplayName>LOLgroup</DisplayName>
               <IsMembershipGroup>true</IsMembershipGroup>
               <ReferenceId>/o=First/ou=Exchange(FYLT)/cn=Recipients/cn=81213b958a0b5295b13b3f02b812bf1bc-LOLgroup</ReferenceId>
            </SearchableMailbox>
         </SearchableMailboxes>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

响应 SOAP 正文包含以下元素：
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)   
- [ResponseCode](responsecode.md)   
- [SearchableMailboxes](searchablemailboxes.md)    
- [SearchableMailbox](searchablemailbox.md)    
- [Guid](guid-ex15websvcsotherref.md)    
- [PrimarySmtpAddress](primarysmtpaddress.md)    
- [IsExternalMailbox](isexternalmailbox.md)   
- [ExternalEmailAddress](externalemailaddress.md)    
- [显示名称 (字符串)](displayname-string.md)    
- [IsMembershipGroup](ismembershipgroup.md)    
- [ReferenceId](referenceid.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-an-expanded-distribution-group"></a>成功的 GetSearchableMailboxes 操作响应：获取有关展开的通讯组的信息

下面的示例演示对**GetSearchableMailboxes**操作请求的成功响应，以获取有关已展开的 lolgroup 通讯组的成员的发现信息。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>3c620d04-8b33-435a-95be-5b939375576</Guid>
          <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Steven Brown</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=90312341a742f0e47e392c80a60d13ecf-Steve</ReferenceId>
        </SearchableMailbox>
      </SearchableMailboxes>
    </GetSearchableMailboxesResponse>
  </s:Body>
</s:Envelope>
```

响应 SOAP 正文包含以下元素：
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)    
- [ResponseCode](responsecode.md)   
- [SearchableMailboxes](searchablemailboxes.md)    
- [SearchableMailbox](searchablemailbox.md)    
- [Guid](guid-ex15websvcsotherref.md)    
- [PrimarySmtpAddress](primarysmtpaddress.md)    
- [IsExternalMailbox](isexternalmailbox.md)    
- [ExternalEmailAddress](externalemailaddress.md)    
- [显示名称 (字符串)](displayname-string.md)    
- [IsMembershipGroup](ismembershipgroup.md)    
- [ReferenceId](referenceid.md)
    
## <a name="getsearchablemailboxes-operation-error-response"></a>GetSearchableMailboxes 操作错误响应

下面的示例演示对**GetSearchableMailboxes**操作请求的错误响应。 这是对在**ExpandGroupMembership**参数设置为**true**时获取所有可搜索邮箱的请求的响应。 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

错误响应 SOAP 正文包含以下元素：
  
- [GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)  
- [MessageText](messagetext.md)   
- [ResponseCode](responsecode.md)   
- [DescriptiveLinkKey](descriptivelinkkey.md) 
- [SearchableMailboxes](searchablemailboxes.md)
    
有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。
  
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS 操作](ews-operations-in-exchange.md)   
- [SetHoldOnMailboxes 操作](setholdonmailboxes-operation.md)   
- [SearchMailboxes 操作](searchmailboxes-operation.md)   
- [GetHoldOnMailboxes 操作](getholdonmailboxes-operation.md)    
- [GetDiscoverySearchConfiguration 操作](getdiscoverysearchconfiguration-operation.md)   
- [GetNonIndexableItemDetails 操作](getnonindexableitemdetails-operation.md)   
- [GetNonIndexableItemStatistics 操作](getnonindexableitemstatistics-operation.md)
    

