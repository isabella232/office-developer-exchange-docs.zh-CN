---
title: AddNewTelUriContactToGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9688ce8-2465-45bb-8bd2-94b32ed4885c
description: 查找有关如何使用 AddNewTelUriContactToGroup EWS 操作的信息。
ms.openlocfilehash: 91228ec627ad928d2f1837c135af24846f811b1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464943"
---
# <a name="addnewteluricontacttogroup-operation"></a><span data-ttu-id="7ca5b-103">AddNewTelUriContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="7ca5b-103">AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="7ca5b-104">查找有关如何使用**AddNewTelUriContactToGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-104">Find information about how to use the **AddNewTelUriContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="7ca5b-105">**AddNewTelUriContactToGroup**操作基于联系人的电话号码将新联系人添加到组中。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-105">The **AddNewTelUriContactToGroup** operation adds a new contact to a group based on a contact's phone number.</span></span> 
  
<span data-ttu-id="7ca5b-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewteluricontacttogroup-operation"></a><span data-ttu-id="7ca5b-107">使用 AddNewTelUriContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="7ca5b-107">Using the AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="7ca5b-108">**AddNewTelUriContactToGroup**操作请求提交联系人的电话 URI、SIP uri、电话号码和要向其添加联系人的组。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-108">An **AddNewTelUriContactToGroup** operation request submits a contact's TEL URI, SIP URI, phone number, and the group to add the contact to.</span></span> <span data-ttu-id="7ca5b-109">**AddNewTelUriContactToGroup**操作响应为新联系人创建角色。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-109">An **AddNewTelUriContactToGroup** operation response creates a persona for the new contact.</span></span> <span data-ttu-id="7ca5b-110">此操作允许客户端添加新联系人，即使该联系人没有名称也是如此。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-110">This operation allows clients to add a new contact even if the contact does not have a name.</span></span> 
  
### <a name="addnewteluricontacttogroup-operation-soap-headers"></a><span data-ttu-id="7ca5b-111">AddNewTelUriContactToGroup 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="7ca5b-111">AddNewTelUriContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="7ca5b-112">**AddNewTelUriContactToGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-112">The **AddNewTelUriContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="7ca5b-113">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="7ca5b-113">**Header name**</span></span>|<span data-ttu-id="7ca5b-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ca5b-114">**Element**</span></span>|<span data-ttu-id="7ca5b-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ca5b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ca5b-116">**模拟**</span><span class="sxs-lookup"><span data-stu-id="7ca5b-116">**Impersonation**</span></span> <br/> |[<span data-ttu-id="7ca5b-117">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="7ca5b-117">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="7ca5b-118">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-118">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="7ca5b-119">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="7ca5b-120">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="7ca5b-120">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="7ca5b-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="7ca5b-121">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="7ca5b-122">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-122">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="7ca5b-123">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-123">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="7ca5b-124">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="7ca5b-124">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="7ca5b-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="7ca5b-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="7ca5b-126">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-126">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="7ca5b-127">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="7ca5b-128">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="7ca5b-128">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="7ca5b-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7ca5b-129">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="7ca5b-130">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-130">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="7ca5b-131">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-131">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewteluricontacttogroup-operation-request-example-add-a-new-contact-to-a-group"></a><span data-ttu-id="7ca5b-132">AddNewTelUriContactToGroup 操作请求示例：向组添加新联系人</span><span class="sxs-lookup"><span data-stu-id="7ca5b-132">AddNewTelUriContactToGroup operation request example: Add a new contact to a group</span></span>

<span data-ttu-id="7ca5b-133">下面的**AddNewTelUriContactToGroup**操作请求示例演示如何创建新联系人，以及如何使用联系人的电话和 SIP uri 将新联系人添加到即时消息（IM）组。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-133">The following example of an **AddNewTelUriContactToGroup** operation request shows how to create a new contact and add the new contact to an instant messaging (IM) group by using the contact's TEL and SIP URIs.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7ca5b-134">本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:AddNewTelUriContactToGroup>
         <m:TelUriAddress>tel:5625550100</m:TelUriAddress>
         <m:ImContactSipUriAddress>sip:john@contoso.com</m:ImContactSipUriAddress>
         <m:ImTelephoneNumber>5625550100</m:ImTelephoneNumber>
         <m:GroupId Id="AAMkADEzOTm4QrAABY7+0GAAA="/>
      </m:AddNewTelUriContactToGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7ca5b-135">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="7ca5b-135">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="7ca5b-136">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="7ca5b-136">AddNewTelUriContactToGroup</span></span>](addnewteluricontacttogroup.md)
    
- [<span data-ttu-id="7ca5b-137">TelUriAddress</span><span class="sxs-lookup"><span data-stu-id="7ca5b-137">TelUriAddress</span></span>](teluriaddress.md)
    
- [<span data-ttu-id="7ca5b-138">ImContactSipUriAddress</span><span class="sxs-lookup"><span data-stu-id="7ca5b-138">ImContactSipUriAddress</span></span>](imcontactsipuriaddress.md)
    
- [<span data-ttu-id="7ca5b-139">ImTelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="7ca5b-139">ImTelephoneNumber</span></span>](imtelephonenumber.md)
    
- [<span data-ttu-id="7ca5b-140">GroupId</span><span class="sxs-lookup"><span data-stu-id="7ca5b-140">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewteluricontacttogroup-operation-response"></a><span data-ttu-id="7ca5b-141">成功的 AddNewTelUriContactToGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="7ca5b-141">Successful AddNewTelUriContactToGroup operation response</span></span>

<span data-ttu-id="7ca5b-142">以下示例显示了对创建联系人的**AddNewTelUriContactToGroup**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-142">The following example shows a successful response to an **AddNewTelUriContactToGroup** operation request to create a contact.</span></span> <span data-ttu-id="7ca5b-143">响应包含联系人的关联角色标识符、该角色的显示名称（在此示例中基于联系人的电话号码）和联系人的项目标识符（显示为源标识符归属的一部分）。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-143">The response contains the associated persona identifier for the contact, the display name of the persona, which in this case is based on the contact's phone number, and the contact's item identifier, which is displayed as part of the source identifier attribution.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"                           
            xmlns:xsd="http://www.w3.org/2001/XMLSchema"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body>
      <AddNewTelUriContactToGroupResponse ResponseClass="Success" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <t:PersonaId Id="AAQkADE686dX3s="/>
            <t:PersonaType>Person</t:PersonaType>
            <t:CreationTime>2012-10-29T23:10:13Z</t:CreationTime>
            <t:DisplayName/>
            <t:DisplayNameFirstLast>5625550100</t:DisplayNameFirstLast>
            <t:DisplayNameLastFirst>5625550100</t:DisplayNameLastFirst>
            <t:FileAs/>
            <t:FileAsId >None</t:FileAsId>
            <t:RelevanceScore >2147483647</t:RelevanceScore>
            <t:Attributions>
               <t:Attribution>
                  <t:Id>0</t:Id>
                  <t:SourceId Id="ABhHuhCAAA=" ChangeKey="EQAAABxFU"/>
                  <t:DisplayName>Lync Contacts</t:DisplayName>
                  <t:IsWritable>false</t:IsWritable>
                  <t:IsQuickContact>true</t:IsQuickContact>
                  <t:IsHidden>false</t:IsHidden>
               </t:Attribution>
            </t:Attributions>
            <t:FileAsIds>
               <t:StringAttributedValue>
                  <t:Value>None</t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:StringAttributedValue>
            </t:FileAsIds>
            <t:OtherTelephones>
               <t:PhoneNumberAttributedValue>
                  <t:Value>
                     <t:Number>5625550100</t:Number>
                     <t:Type>Other</t:Type>
                  </t:Value>
                  <t:Attributions>
                     <t:Attribution>0</t:Attribution>
                  </t:Attributions>
               </t:PhoneNumberAttributedValue>
            </t:OtherTelephones>
         </Persona>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="7ca5b-144">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="7ca5b-144">The response SOAP body contains following elements:</span></span>
  
- [<span data-ttu-id="7ca5b-145">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="7ca5b-145">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="7ca5b-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7ca5b-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7ca5b-147">角色</span><span class="sxs-lookup"><span data-stu-id="7ca5b-147">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="7ca5b-148">PersonaId</span><span class="sxs-lookup"><span data-stu-id="7ca5b-148">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="7ca5b-149">PersonaType</span><span class="sxs-lookup"><span data-stu-id="7ca5b-149">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="7ca5b-150">CreationTime</span><span class="sxs-lookup"><span data-stu-id="7ca5b-150">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="7ca5b-151">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="7ca5b-151">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="7ca5b-152">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="7ca5b-152">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="7ca5b-153">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="7ca5b-153">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="7ca5b-154">FileAs</span><span class="sxs-lookup"><span data-stu-id="7ca5b-154">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="7ca5b-155">FileAsId</span><span class="sxs-lookup"><span data-stu-id="7ca5b-155">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="7ca5b-156">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="7ca5b-156">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="7ca5b-157">归属（ArrayOfPersonaAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="7ca5b-157">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="7ca5b-158">归属（PersonaAttributionType）</span><span class="sxs-lookup"><span data-stu-id="7ca5b-158">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="7ca5b-159">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="7ca5b-159">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="7ca5b-160">SourceId</span><span class="sxs-lookup"><span data-stu-id="7ca5b-160">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="7ca5b-161">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="7ca5b-161">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="7ca5b-162">IsWritable</span><span class="sxs-lookup"><span data-stu-id="7ca5b-162">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="7ca5b-163">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="7ca5b-163">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="7ca5b-164">IsHidden</span><span class="sxs-lookup"><span data-stu-id="7ca5b-164">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="7ca5b-165">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="7ca5b-165">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="7ca5b-166">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="7ca5b-166">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="7ca5b-167">值</span><span class="sxs-lookup"><span data-stu-id="7ca5b-167">Value</span></span>](value.md)
    
- [<span data-ttu-id="7ca5b-168">归属（ArrayOfValueAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="7ca5b-168">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="7ca5b-169">特性（string）</span><span class="sxs-lookup"><span data-stu-id="7ca5b-169">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="7ca5b-170">OtherTelephones</span><span class="sxs-lookup"><span data-stu-id="7ca5b-170">OtherTelephones</span></span>](othertelephones.md)
    
- [<span data-ttu-id="7ca5b-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="7ca5b-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="7ca5b-172">值</span><span class="sxs-lookup"><span data-stu-id="7ca5b-172">Value</span></span>](value.md)
    
- [<span data-ttu-id="7ca5b-173">Number</span><span class="sxs-lookup"><span data-stu-id="7ca5b-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="7ca5b-174">类型（字符串）</span><span class="sxs-lookup"><span data-stu-id="7ca5b-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="7ca5b-175">归属（ArrayOfValueAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="7ca5b-175">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="7ca5b-176">特性（string）</span><span class="sxs-lookup"><span data-stu-id="7ca5b-176">Attribution (string)</span></span>](attribution-string.md)
    
## <a name="addnewteluricontacttogroup-operation-error-response-example"></a><span data-ttu-id="7ca5b-177">AddNewTelUriContactToGroup 操作错误响应示例</span><span class="sxs-lookup"><span data-stu-id="7ca5b-177">AddNewTelUriContactToGroup operation error response example</span></span>

<span data-ttu-id="7ca5b-178">下面的示例演示当组标识符包含一个格式良好的值，而该值不标识邮箱中的组时， **AddNewTelUriContactToGroup**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="7ca5b-178">The following example shows an error response to an **AddNewTelUriContactToGroup** operation request when the group identifier contains a well-formed value that does not identify a group in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewTelUriContactToGroupResponse ResponseClass="Error" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="7ca5b-179">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="7ca5b-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="7ca5b-180">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="7ca5b-180">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="7ca5b-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="7ca5b-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="7ca5b-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7ca5b-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7ca5b-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7ca5b-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="7ca5b-184">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ca5b-184">See also</span></span>

- [<span data-ttu-id="7ca5b-185">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="7ca5b-185">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="7ca5b-186">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="7ca5b-186">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

