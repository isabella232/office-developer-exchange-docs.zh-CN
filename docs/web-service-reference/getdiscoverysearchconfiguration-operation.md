---
title: GetDiscoverySearchConfiguration 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8a54a6dc-110c-4972-a8bc-5ddb43c4b857
description: 查找有关 GetDiscoverySearchConfiguration EWS 操作的信息。
ms.openlocfilehash: 62cadc818219e13199aa246e87066571d78c4e3d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525076"
---
# <a name="getdiscoverysearchconfiguration-operation"></a>GetDiscoverySearchConfiguration 操作

查找有关 **GetDiscoverySearchConfiguration** EWS 操作的信息。 
  
**GetDiscoverySearchConfiguration** 操作返回就地保留、保存的发现搜索以及启用发现搜索的邮箱的配置信息。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-getdiscoverysearchconfiguration-operation"></a>使用 GetDiscoverySearchConfiguration 操作

**GetDiscoverySearchConfiguration** 操作提供发现搜索的配置信息。 请求可以包含下列一个或多个参数： 
  
1. [SearchId](searchid.md) — 标识保存的发现搜索。 如果在请求中发送此参数，则忽略其他参数的值。 
    
2. [ExpandGroupMembership](expandgroupmembership.md) - 指示是否在响应中扩展组成员身份。 true **值表示** 展开组成员身份，以便所有可搜索的邮箱在响应中返回。 false **值表示** 响应中仅返回组。 
    
3. [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) - 指示除了就地保留配置之外，是否返回所有可搜索的邮箱。 true **值表示** 仅返回就地保留配置。 false **值表示** 除了就地保留标识符之外，还返回所有可搜索邮箱标识符。 如果此元素不存在，则默认行为与值 **false 等效**。 
    
### <a name="getdiscoverysearchconfiguration-operation-soap-headers"></a>GetDiscoverySearchConfiguration 操作 SOAP 标头

**GetDiscoverySearchConfiguration** 操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**ManagementRole** <br/> |[ManagementRole](managementrole.md) <br/> |标识调用方进行请求所需的服务器角色。 此标头适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。 此标头适用于响应。  <br/> |
   
## <a name="getdiscoverysearchconfiguration-operation-request-example-get-the-discovery-search-configuration-for-a-saved-search"></a>GetDiscoverySearchConfiguration 操作请求示例：获取已保存搜索的发现搜索配置

**GetDiscoverySearchConfiguration** 操作请求的以下示例显示如何请求配置名为"MyDiscSearchFor-sbrown"的已保存搜索。 [ExpandGroupMembership 和](expandgroupmembership.md) [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md)元素的参数将被忽略。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetDiscoverySearchConfiguration>
         <m:SearchId>MyDiscSearchFor-sbrown</m:SearchId>
         <m:ExpandGroupMembership>true</m:ExpandGroupMembership>
         <m:InPlaceHoldConfigurationOnly>false</m:InPlaceHoldConfigurationOnly>
      </m:GetDiscoverySearchConfiguration>
   </soap:Body>
</soap:Envelope>

```

请求 SOAP 正文包含以下元素：
  
- [GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)
    
- [SearchId](searchid.md)
    
- [ExpandGroupMembership](expandgroupmembership.md)
    
- [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-a-single-saved-search"></a>成功的 GetDiscoverySearchConfiguration 操作响应：请求单个保存的搜索

以下示例显示成功响应 **GetDiscoverySearchConfiguration** 操作请求，获取名为"MyDiscSearchFor-sbrown"的已保存搜索的配置。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetDiscoverySearchConfigurationResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <DiscoverySearchConfigurations>
        <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <SearchId>MyDiscSearchFor-sbrown</SearchId>
          <SearchQuery>test item</SearchQuery>
          <SearchableMailboxes>
            <SearchableMailbox>
              <Guid>3c620d04-8b22-432e-92be-5b9321599576</Guid>
              <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
              <IsExternalMailbox>false</IsExternalMailbox>
              <ExternalEmailAddress/>
              <DisplayName>Steven Brown</DisplayName>
              <IsMembershipGroup>false</IsMembershipGroup>
              <ReferenceId>/o=First/ou=Exchange(FYDILT)/cn=Recipients/cn=313ecf-Steve</ReferenceId>
            </SearchableMailbox>
          </SearchableMailboxes>
        </DiscoverySearchConfiguration>
      </DiscoverySearchConfigurations>
    </GetDiscoverySearchConfigurationResponse>
  </s:Body>
</s:Envelope>
```

响应 SOAP 正文包含以下元素：
  
- [GetDiscoverySearchConfigurationResponse](getdiscoverysearchconfigurationresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [DiscoverySearchConfigurations](discoverysearchconfigurations.md)
    
- [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
    
- [SearchId](searchid.md)
    
- [SearchQuery](searchquery.md)
    
- [SearchableMailboxes](searchablemailboxes.md)
    
- [SearchableMailbox](searchablemailbox.md)
    
- [Guid](guid-ex15websvcsotherref.md)
    
- [PrimarySmtpAddress (string)](primarysmtpaddress-string.md)
    
- [IsExternalMailbox](isexternalmailbox.md)
    
- [ExternalEmailAddress](externalemailaddress.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
- [IsMembershipGroup](ismembershipgroup.md)
    
- [ReferenceId](referenceid.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-in-place-holds"></a>成功的 GetDiscoverySearchConfiguration 操作响应：就地保留请求

以下示例显示了对仅获取就地保留的 **GetDiscoverySearchConfiguration** 操作请求的成功响应。 
  
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
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <InPlaceHoldIdentity>3f37d90f53144558a80814ef0272749a9</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <InPlaceHoldIdentity>6ea486f0f3f140efb044682a2e782abdf</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

响应 SOAP 正文包含以下元素：
  
- [GetDiscoverySearchConfigurationResponse](getdiscoverysearchconfigurationresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [DiscoverySearchConfigurations](discoverysearchconfigurations.md)
    
- [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
    
- [SearchId](searchid.md)
    
- [SearchQuery](searchquery.md)
    
- [InPlaceHoldIdentity](inplaceholdidentity.md)
    
- [ManagedByOrganization](managedbyorganization.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-all-saved-discovery-search-configurations"></a>成功的 GetDiscoverySearchConfiguration 操作响应：请求所有保存的发现搜索配置

以下示例显示成功响应 **GetDiscoverySearchConfiguration** 操作请求，以获取所有保存的发现搜索。 
  
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
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>3c620d04-8b33-435e-95be-5b9351599576</Guid>
                     <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Steven Brown</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=35381a742f0e47e395c8601a60d13ecz-Steve</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>e788c4b0-54a2-458c-83b2-22d5bb02b23f</Guid>
                     <PrimarySmtpAddress>Administrator@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Administrator</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=ebez7871332d4595abe1c62962911a58-Admin</ReferenceId>
                  </SearchableMailbox>
                  <SearchableMailbox>
                     <Guid>6f6cff39-8967-4a60-b43f-328413c25199</Guid>
                     <PrimarySmtpAddress>ADavis@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Anthony Davis</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=f10c9f70519844beb04101d8f40c572z-Antho</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>
```

响应 SOAP 正文包含以下元素：
  
- [GetDiscoverySearchConfigurationResponse](getdiscoverysearchconfigurationresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [DiscoverySearchConfigurations](discoverysearchconfigurations.md)
    
- [DiscoverySearchConfiguration](discoverysearchconfiguration.md)
    
- [SearchId](searchid.md)
    
- [SearchQuery](searchquery.md)
    
- [SearchableMailboxes](searchablemailboxes.md)
    
- [SearchableMailbox](searchablemailbox.md)
    
- [Guid](guid-ex15websvcsotherref.md)
    
- [PrimarySmtpAddress (string)](primarysmtpaddress-string.md)
    
- [IsExternalMailbox](isexternalmailbox.md)
    
- [ExternalEmailAddress](externalemailaddress.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
- [IsMembershipGroup](ismembershipgroup.md)
    
- [ReferenceId](referenceid.md)
    
## <a name="getdiscoverysearchconfiguration-operation-error-response"></a>GetDiscoverySearchConfiguration 操作错误响应

以下示例显示对 **GetDiscoverySearchConfiguration** 操作请求的错误响应。 这是对请求的响应，请求获取服务器上找不到的已保存搜索。 
  
```XML
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
      <GetDiscoverySearchConfigurationResponse ResponseClass="Error" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Search configuration corresponding to the search id was not found.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <DiscoverySearchConfigurations/>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

错误响应 SOAP 正文包含以下元素：
  
- [GetDiscoverySearchConfigurationResponse](getdiscoverysearchconfigurationresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [DiscoverySearchConfigurations](discoverysearchconfigurations.md)
    
有关 EWS 通用且特定于此操作的其他错误代码，请参阅 [ResponseCode](responsecode.md)。
  
## <a name="see-also"></a>另请参阅

- [EWS 操作在Exchange](ews-operations-in-exchange.md)
    
- [GetSearchableMailboxes](getsearchablemailboxes.md)
    
- [SearchMailboxes](searchmailboxes.md)
    
- [GetHoldOnMailboxes](getholdonmailboxes.md)
    
- [SetHoldOnMailboxes](setholdonmailboxes.md)
    
- [GetNonIndexableItemDetails](getnonindexableitemdetails.md)
    
- [GetNonIndexableItemStatistics](getnonindexableitemstatistics.md)
    

