---
title: GetImItemList 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e31d14e1-0c1f-4b69-98b7-157d59c13698
description: 查找信息 GetImItemList EWS 操作。
ms.openlocfilehash: 3977b0ad31e819cd973ce261ba3152b3840003b3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754584"
---
# <a name="getimitemlist-operation"></a><span data-ttu-id="67b80-103">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="67b80-103">GetImItemList operation</span></span>

<span data-ttu-id="67b80-104">查找有关**GetImItemList** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="67b80-104">Find information about the **GetImItemList** EWS operation.</span></span> 
  
## <a name="using-the-getimitemlist-operation"></a><span data-ttu-id="67b80-105">使用 GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="67b80-105">Using the GetImItemList operation</span></span>

<span data-ttu-id="67b80-106">**GetImItemList**操作中检索的即时消息 (IM) 组的列表和 IM 联系人邮箱中的角色。</span><span class="sxs-lookup"><span data-stu-id="67b80-106">The **GetImItemList** operation retrieves the list of instant messaging (IM) groups and IM contact personas in a mailbox.</span></span> <span data-ttu-id="67b80-107">**GetImItemList**操作不采用任何参数。</span><span class="sxs-lookup"><span data-stu-id="67b80-107">The **GetImItemList** operation does not take any arguments.</span></span> 
  
<span data-ttu-id="67b80-108">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="67b80-108">This operation was introduced in Exchange Server 2013.</span></span>
  
### <a name="getimitemlist-operation-soap-headers"></a><span data-ttu-id="67b80-109">GetImItemList 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="67b80-109">GetImItemList operation SOAP headers</span></span>

<span data-ttu-id="67b80-110">**GetImItemList**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="67b80-110">The **GetImItemList** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="67b80-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="67b80-111">**Header name**</span></span>|<span data-ttu-id="67b80-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="67b80-112">**Element**</span></span>|<span data-ttu-id="67b80-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="67b80-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="67b80-114">**模拟**</span><span class="sxs-lookup"><span data-stu-id="67b80-114">**Impersonation**</span></span> <br/> |[<span data-ttu-id="67b80-115">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="67b80-115">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="67b80-116">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="67b80-116">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="67b80-117">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="67b80-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="67b80-118">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="67b80-118">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="67b80-119">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="67b80-119">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="67b80-120">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="67b80-120">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="67b80-121">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="67b80-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="67b80-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="67b80-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="67b80-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="67b80-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="67b80-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="67b80-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="67b80-125">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="67b80-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="67b80-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="67b80-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="67b80-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="67b80-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="67b80-128">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="67b80-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="67b80-129">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="67b80-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getimitemlist-operation-request-example-request-your-im-items-list"></a><span data-ttu-id="67b80-130">GetImItemList 操作请求示例： 请求您的 IM 项目列表</span><span class="sxs-lookup"><span data-stu-id="67b80-130">GetImItemList operation request example: Request your IM items list</span></span>

<span data-ttu-id="67b80-131">**GetImItemList**操作请求的下面的示例演示如何请求的 IM 组的列表和 IM 联系人邮箱中的角色。</span><span class="sxs-lookup"><span data-stu-id="67b80-131">The following example of a **GetImItemList** operation request shows how to request the list of IM groups and IM contact personas in a mailbox.</span></span> <span data-ttu-id="67b80-132">**GetImItemList**元素是 SOAP 正文中的唯一元素选项。</span><span class="sxs-lookup"><span data-stu-id="67b80-132">The **GetImItemList** element is the only element option in the SOAP body.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:GetImItemList/>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="67b80-133">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="67b80-133">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="67b80-134">GetImItemList</span><span class="sxs-lookup"><span data-stu-id="67b80-134">GetImItemList</span></span>](getimitemlist.md)
    
## <a name="successful-getimitemlist-operation-response"></a><span data-ttu-id="67b80-135">成功 GetImItemList 操作响应</span><span class="sxs-lookup"><span data-stu-id="67b80-135">Successful GetImItemList operation response</span></span>

<span data-ttu-id="67b80-136">下面的示例演示对**GetImItemList**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="67b80-136">The following example shows a successful response to a **GetImItemList** operation request.</span></span> <span data-ttu-id="67b80-137">则响应中包含四个 IM 组。</span><span class="sxs-lookup"><span data-stu-id="67b80-137">The response contains four IM groups.</span></span> <span data-ttu-id="67b80-138">IM 组中的三个 — 其他联系人、 标记，和收藏夹 — 是 Exchange 存储中的默认组。</span><span class="sxs-lookup"><span data-stu-id="67b80-138">Three of the IM groups — Other Contacts, Tagged, and Favorites — are default groups in the Exchange store.</span></span> <span data-ttu-id="67b80-139">MyCustomGroup2 组是用户创建自定义组。</span><span class="sxs-lookup"><span data-stu-id="67b80-139">The MyCustomGroup2 group is a custom user-created group.</span></span> <span data-ttu-id="67b80-140">其他联系人和标记组没有成员。</span><span class="sxs-lookup"><span data-stu-id="67b80-140">The Other Contacts and Tagged groups do not have members.</span></span> <span data-ttu-id="67b80-141">收藏夹组具有单个联系人的成员。</span><span class="sxs-lookup"><span data-stu-id="67b80-141">The Favorites group has a single contact member.</span></span> <span data-ttu-id="67b80-142">MyCustomGroup2 具有两个成员的联系人。</span><span class="sxs-lookup"><span data-stu-id="67b80-142">The MyCustomGroup2 has two member contacts.</span></span> <span data-ttu-id="67b80-143">提供了项标识符，以便可以执行后续**GetItem**请求以获取有关 IM 联系人详细信息。</span><span class="sxs-lookup"><span data-stu-id="67b80-143">The item identifiers are provided so that subsequent **GetItem** requests can be performed to get more information about the IM contacts.</span></span> 
  
<span data-ttu-id="67b80-144">本示例返回两个角色。</span><span class="sxs-lookup"><span data-stu-id="67b80-144">This example returns two personas.</span></span> <span data-ttu-id="67b80-145">第一个角色表示两个联系人项目： 安 Smith 和 Tony Smith。</span><span class="sxs-lookup"><span data-stu-id="67b80-145">The first persona represents two contact items: Anthony Smith and Tony Smith.</span></span> <span data-ttu-id="67b80-146">**个人**对象中返回的组合的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="67b80-146">The combined contact information is returned in the **Persona** object.</span></span> <span data-ttu-id="67b80-147">第二个角色表示 Terence Adams 的显示名称与单个联系人。</span><span class="sxs-lookup"><span data-stu-id="67b80-147">The second persona represents a single contact with the display name of Terence Adams.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="67b80-148">Exchange 存储区标识符、 项标识符、 源标识符、 文件夹标识符和个人标识符已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="67b80-148">The Exchange store identifiers, item identifiers, source identifiers, folder identifiers, and persona identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetImItemListResponse ResponseClass="Success" 
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <ImGroup>
                  <DisplayName>Other Contacts</DisplayName>
                  <GroupType>IPM.DistList.MOC.OtherContacts</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLThQoTbWAAAAAAQUAAA=" 
                                   ChangeKey="EgAAAA==" />
               </ImGroup>
               <ImGroup>
                  <DisplayName>Tagged</DisplayName>
                  <GroupType>IPM.DistList.MOC.Tagged</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJAAQTAAA=" 
                                   ChangeKey="EgAAAA==" />
               </ImGroup>
               <ImGroup>
                  <DisplayName>Favorites</DisplayName>
                  <GroupType>IPM.DistList.MOC.Favorites</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJjMTAAAAAQSAAA=" 
                                   ChangeKey="EgAAAA==" />
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkAGQ1MjJtt/bhQoTbWAAAAAAvcAAA=" 
                             ChangeKey="EQAAAA==" />
                  </MemberCorrelationKey>
               </ImGroup>
               <ImGroup>
                  <DisplayName>MyCustomGroup2</DisplayName>
                  <GroupType>IPM.DistList.MOC.UserGroup</GroupType>
                  <ExchangeStoreId Id="AAMkAGQ1MjJjKAAA=" 
                                   ChangeKey="EgAAAA==" />
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkAGQ1Matt/bhQoTbWAAAAAAvcAAA=" 
                             ChangeKey="EQAAAA==" />
                     <ItemId Id="AAMkAGQ1MjJjMTBkTbWAAAAAAveAAA=" 
                             ChangeKey="EQAAAA==" />
                  </MemberCorrelationKey>
               </ImGroup>
            </Groups>
            <Personas xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <Persona>
                  <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4YkZmRkYQAQAFgxE1nBcqRGgYWWorM9/+s=" />
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-01-12T22:14:36Z</CreationTime>
                  <DisplayName>Anthony Smith</DisplayName>
                  <DisplayNameFirstLast>Anthony Smith</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Smith Anthony</DisplayNameLastFirst>
                  <FileAs>Smith, Anthony</FileAs>
                  <FileAsId>LastCommaFirst</FileAsId>
                  <GivenName>Anthony</GivenName>
                  <Surname>Smith</Surname>
                  <EmailAddress>
                     <Name>tsmith@contoso.com</Name>
                     <EmailAddress>tsmith@contoso.com</EmailAddress>
                     <RoutingType>SMTP</RoutingType>
                  </EmailAddress>
                  <EmailAddresses>
                     <EmailAddress>
                        <Name>tsmith@contoso.com</Name>
                        <EmailAddress>tsmith@contoso.com</EmailAddress>
                        <RoutingType>SMTP</RoutingType>
                     </EmailAddress>
                  </EmailAddresses>
                  <ImAddress>tsmith@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AQMkAGQ1MjIAYzEwZC03OGNlLTQ5Bq239uFChNtYAAAIvDAAAAA==" 
                                  ChangeKey="EQAAABYAAABtF8oI7iVOQatt/bhQoTbWAAAAADB3" />
                        <DisplayName>Outlook</DisplayName>
                        <IsWritable>true</IsWritable>
                        <IsQuickContact>false</IsQuickContact>
                        <IsHidden>false</IsHidden>
                        <FolderId Id="AQMkAGQ1MjIAYzEMikE3AQBtF8oI7iVOQatt/bhQoTbWAAADEAAAAA==" 
                                  ChangeKey="AQAAAA==" />
                     </Attribution>
                     <Attribution>
                        <Id>1</Id>
                        <SourceId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04/bhQoTbWAAAAAAveAAA=" 
                                  ChangeKey="EQAAABYAAABtF8oI7iVOQatt/bhQoTbWAAAAAAym" />
                        <DisplayName>Outlook</DisplayName>
                        <IsWritable>true</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                        <FolderId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Qatt/bhQoTbWAAAAAAvZAAA=" 
                                  ChangeKey="AQAAAA==" />
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Anthony Smith</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                     <StringAttributedValue>
                        <Value>Tony Smith</Value>
                        <Attributions>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </DisplayNames>
                  <FileAses>
                     <StringAttributedValue>
                        <Value>Smith, Anthony</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAses>
                  <FileAsIds>
                     <StringAttributedValue>
                        <Value>LastCommaFirst</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                     <StringAttributedValue>
                        <Value>None</Value>
                        <Attributions>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAsIds>
                  <GivenNames>
                     <StringAttributedValue>
                        <Value>Anthony</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </GivenNames>
                  <Surnames>
                     <StringAttributedValue>
                        <Value>Smith</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </Surnames>
                  <HomePhones>
                     <PhoneNumberAttributedValue>
                        <Value>
                           <Number>4255550110</Number>
                           <Type>Home</Type>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </PhoneNumberAttributedValue>
                  </HomePhones>
                  <MobilePhones>
                     <PhoneNumberAttributedValue>
                        <Value>
                           <Number>4255550120</Number>
                           <Type>Mobile</Type>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </PhoneNumberAttributedValue>
                  </MobilePhones>
                  <Emails1>
                     <EmailAddressAttributedValue>
                        <Value>
                           <Name>tsmith@contoso.com</Name>
                           <EmailAddress>tsmith@contoso.com</EmailAddress>
                           <RoutingType>SMTP</RoutingType>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </EmailAddressAttributedValue>
                  </Emails1>
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tsmith@contoso.com</Value>
                        <Attributions>
                           <Attribution>1</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
               </Persona>
               <Persona>
                  <PersonaId Id="AAQkAGQ1MjJjMTBkLkYQAQAJ3EkhEEXN5KufGbSYJanZk=" />
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-01-05T23:06:58Z</CreationTime>
                  <DisplayName>Terence Adams</DisplayName>
                  <DisplayNameFirstLast>Terence Adams</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Terence Adams</DisplayNameLastFirst>
                  <FileAsId>None</FileAsId>
                  <EmailAddress>
                     <Name>Terence Adams</Name>
                     <EmailAddress>tadams@contoso.com</EmailAddress>
                     <RoutingType>SMTP</RoutingType>
                  </EmailAddress>
                  <EmailAddresses>
                     <EmailAddress>
                        <Name>Terence Adams</Name>
                        <EmailAddress>tadams@contoso.com</EmailAddress>
                        <RoutingType>SMTP</RoutingType>
                     </EmailAddress>
                  </EmailAddresses>
                  <ImAddress>tadams@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AAMkAGQ1MjVOQatt/bhQoTbWAAAA7iVOQatt/bhQoTbWAAAAAAvcAAA=" 
                                  ChangeKey="EQAAABYAAABtF8oI7iVOQatt/bhQoTbWAAAAAAyg" />
                        <DisplayName>Outlook</DisplayName>
                        <IsWritable>true</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                        <FolderId Id="AAMkAGQ1MjJjMTBkLTc4Y2rBtF8oI7iVOQatt/bhQoTbWAAAAAAvZAAA=" 
                                  ChangeKey="AQAAAA==" />
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Terence Adams</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </DisplayNames>
                  <FileAsIds>
                     <StringAttributedValue>
                        <Value>None</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </FileAsIds>
                  <Emails1>
                     <EmailAddressAttributedValue>
                        <Value>
                           <Name>Terence Adams</Name>
                           <EmailAddress>tadams@contoso.com</EmailAddress>
                           <RoutingType>SMTP</RoutingType>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </EmailAddressAttributedValue>
                  </Emails1>
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tadams@contoso.com</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
               </Persona>
            </Personas>
         </ImItemList>
      </GetImItemListResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="67b80-149">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="67b80-149">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="67b80-150">GetImItemListResponse</span><span class="sxs-lookup"><span data-stu-id="67b80-150">GetImItemListResponse</span></span>](getimitemlistresponse.md)
    
- [<span data-ttu-id="67b80-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="67b80-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="67b80-152">ImItemList</span><span class="sxs-lookup"><span data-stu-id="67b80-152">ImItemList</span></span>](imitemlist.md)
    
- [<span data-ttu-id="67b80-153">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="67b80-153">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="67b80-154">GroupType</span><span class="sxs-lookup"><span data-stu-id="67b80-154">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="67b80-155">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="67b80-155">ExchangeStoreId</span></span>](exchangestoreid.md)
    
- [<span data-ttu-id="67b80-156">MemberCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="67b80-156">MemberCorrelationKey</span></span>](membercorrelationkey.md)
    
- [<span data-ttu-id="67b80-157">ItemId</span><span class="sxs-lookup"><span data-stu-id="67b80-157">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="67b80-158">角色</span><span class="sxs-lookup"><span data-stu-id="67b80-158">Personas</span></span>](personas-ex15websvcsotherref.md)
    
- [<span data-ttu-id="67b80-159">PersonaId</span><span class="sxs-lookup"><span data-stu-id="67b80-159">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="67b80-160">PersonaType</span><span class="sxs-lookup"><span data-stu-id="67b80-160">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="67b80-161">CreationTime</span><span class="sxs-lookup"><span data-stu-id="67b80-161">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="67b80-162">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="67b80-162">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="67b80-163">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="67b80-163">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="67b80-164">FileAs</span><span class="sxs-lookup"><span data-stu-id="67b80-164">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="67b80-165">FileAsId</span><span class="sxs-lookup"><span data-stu-id="67b80-165">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="67b80-166">GivenName</span><span class="sxs-lookup"><span data-stu-id="67b80-166">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="67b80-167">姓</span><span class="sxs-lookup"><span data-stu-id="67b80-167">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="67b80-168">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="67b80-168">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="67b80-169">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="67b80-169">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="67b80-170">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="67b80-170">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="67b80-171">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="67b80-171">EmailAddresses (ArrayOfEmailAddressesType)</span></span>](emailaddresses-arrayofemailaddressestype.md)
    
- [<span data-ttu-id="67b80-172">ImAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="67b80-172">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="67b80-173">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="67b80-173">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="67b80-174">归属 (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="67b80-174">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="67b80-175">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="67b80-175">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="67b80-176">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="67b80-176">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="67b80-177">SourceId</span><span class="sxs-lookup"><span data-stu-id="67b80-177">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="67b80-178">IsWritable</span><span class="sxs-lookup"><span data-stu-id="67b80-178">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="67b80-179">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="67b80-179">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="67b80-180">IsHidden</span><span class="sxs-lookup"><span data-stu-id="67b80-180">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="67b80-181">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="67b80-181">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="67b80-182">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="67b80-182">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="67b80-183">FileAses</span><span class="sxs-lookup"><span data-stu-id="67b80-183">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="67b80-184">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="67b80-184">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="67b80-185">GivenNames</span><span class="sxs-lookup"><span data-stu-id="67b80-185">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="67b80-186">姓</span><span class="sxs-lookup"><span data-stu-id="67b80-186">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="67b80-187">HomePhones</span><span class="sxs-lookup"><span data-stu-id="67b80-187">HomePhones</span></span>](homephones.md)
    
- [<span data-ttu-id="67b80-188">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="67b80-188">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="67b80-189">MobilePhones</span><span class="sxs-lookup"><span data-stu-id="67b80-189">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="67b80-190">Emails1</span><span class="sxs-lookup"><span data-stu-id="67b80-190">Emails1</span></span>](emails1.md)
    
- [<span data-ttu-id="67b80-191">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="67b80-191">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
    
- [<span data-ttu-id="67b80-192">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="67b80-192">ImAddresses</span></span>](imaddresses.md)
    
- [<span data-ttu-id="67b80-193">值 (ExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="67b80-193">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md)
    
## <a name="getimitemlist-operation-error-response"></a><span data-ttu-id="67b80-194">GetImItemList 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="67b80-194">GetImItemList operation error response</span></span>

<span data-ttu-id="67b80-195">下面的示例演示对**GetImItemList**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="67b80-195">The following example shows an error response to a **GetImItemList** operation request.</span></span> <span data-ttu-id="67b80-196">这是对包含将不正确请求的服务器版本中的 SOAP 标头的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="67b80-196">This is a response to a request that contains an incorrect requested server version in the SOAP header.</span></span> <span data-ttu-id="67b80-197">此错误响应 SOAP 故障，并不表示 EWS 架构中。</span><span class="sxs-lookup"><span data-stu-id="67b80-197">This error response is a SOAP fault and is not represented in the EWS schema.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="http://schemas.microsoft.com/exchange/services/2006/types">a:ErrorIncorrectSchemaVersion</faultcode>
         <faultstring xml:lang="en-US">The request is valid but does not specify the correct server version in the RequestServerVersion SOAP header.  Ensure that the RequestServerVersion SOAP header is set with the correct RequestServerVersionValue.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">ErrorIncorrectSchemaVersion</e:ResponseCode>
            <e:Message xmlns:e="http://schemas.microsoft.com/exchange/services/2006/errors">The request is valid but does not specify the correct server version in the RequestServerVersion SOAP header.  Ensure that the RequestServerVersion SOAP header is set with the correct RequestServerVersionValue.</e:Message>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="67b80-198">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67b80-198">See also</span></span>

- [<span data-ttu-id="67b80-199">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="67b80-199">AddImGroup operation</span></span>](addimgroup-operation.md)
    
- [<span data-ttu-id="67b80-200">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="67b80-200">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="67b80-201">GetImItems 操作</span><span class="sxs-lookup"><span data-stu-id="67b80-201">GetImItems operation</span></span>](getimitems-operation.md)
    

