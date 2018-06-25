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
ms.openlocfilehash: 34450171776b4215d9c0a39700a309e2e2d755dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753120"
---
# <a name="addnewteluricontacttogroup-operation"></a><span data-ttu-id="79391-103">AddNewTelUriContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="79391-103">AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="79391-104">查找有关如何使用**AddNewTelUriContactToGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="79391-104">Find information about how to use the **AddNewTelUriContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="79391-105">**AddNewTelUriContactToGroup**操作将新的联系人添加到联系人的电话号码所基于的组。</span><span class="sxs-lookup"><span data-stu-id="79391-105">The **AddNewTelUriContactToGroup** operation adds a new contact to a group based on a contact's phone number.</span></span> 
  
<span data-ttu-id="79391-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="79391-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewteluricontacttogroup-operation"></a><span data-ttu-id="79391-107">使用 AddNewTelUriContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="79391-107">Using the AddNewTelUriContactToGroup operation</span></span>

<span data-ttu-id="79391-108">**AddNewTelUriContactToGroup**操作请求提交联系人的 TEL URI、 SIP URI、 电话号码和组添加到联系人。</span><span class="sxs-lookup"><span data-stu-id="79391-108">An **AddNewTelUriContactToGroup** operation request submits a contact's TEL URI, SIP URI, phone number, and the group to add the contact to.</span></span> <span data-ttu-id="79391-109">**AddNewTelUriContactToGroup**操作响应创建新的联系人的角色。</span><span class="sxs-lookup"><span data-stu-id="79391-109">An **AddNewTelUriContactToGroup** operation response creates a persona for the new contact.</span></span> <span data-ttu-id="79391-110">此操作将允许客户端添加新联系人，即使该联系人不具有一个名称。</span><span class="sxs-lookup"><span data-stu-id="79391-110">This operation allows clients to add a new contact even if the contact does not have a name.</span></span> 
  
### <a name="addnewteluricontacttogroup-operation-soap-headers"></a><span data-ttu-id="79391-111">AddNewTelUriContactToGroup 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="79391-111">AddNewTelUriContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="79391-112">**AddNewTelUriContactToGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="79391-112">The **AddNewTelUriContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="79391-113">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="79391-113">**Header name**</span></span>|<span data-ttu-id="79391-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="79391-114">**Element**</span></span>|<span data-ttu-id="79391-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="79391-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79391-116">**模拟**</span><span class="sxs-lookup"><span data-stu-id="79391-116">**Impersonation**</span></span> <br/> |[<span data-ttu-id="79391-117">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="79391-117">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="79391-118">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="79391-118">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="79391-119">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="79391-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="79391-120">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="79391-120">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="79391-121">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="79391-121">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="79391-122">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="79391-122">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="79391-123">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="79391-123">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="79391-124">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="79391-124">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="79391-125">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="79391-125">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="79391-126">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="79391-126">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="79391-127">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="79391-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="79391-128">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="79391-128">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="79391-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="79391-129">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="79391-130">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="79391-130">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="79391-131">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="79391-131">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewteluricontacttogroup-operation-request-example-add-a-new-contact-to-a-group"></a><span data-ttu-id="79391-132">AddNewTelUriContactToGroup 操作请求示例： 向组添加新联系人</span><span class="sxs-lookup"><span data-stu-id="79391-132">AddNewTelUriContactToGroup operation request example: Add a new contact to a group</span></span>

<span data-ttu-id="79391-133">**AddNewTelUriContactToGroup**操作请求的下面的示例演示如何创建新的联系人并将新联系人添加到的即时消息 (IM) 组中，使用该联系人的电话和 SIP Uri。</span><span class="sxs-lookup"><span data-stu-id="79391-133">The following example of an **AddNewTelUriContactToGroup** operation request shows how to create a new contact and add the new contact to an instant messaging (IM) group by using the contact's TEL and SIP URIs.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="79391-134">所有项目标识符，本文中的更改项具有已截短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="79391-134">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
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
      <m:AddNewTelUriContactToGroup>
         <m:TelUriAddress>tel:5625550100</m:TelUriAddress>
         <m:ImContactSipUriAddress>sip:john@contoso.com</m:ImContactSipUriAddress>
         <m:ImTelephoneNumber>5625550100</m:ImTelephoneNumber>
         <m:GroupId Id="AAMkADEzOTm4QrAABY7+0GAAA="/>
      </m:AddNewTelUriContactToGroup>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="79391-135">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="79391-135">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="79391-136">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="79391-136">AddNewTelUriContactToGroup</span></span>](addnewteluricontacttogroup.md)
    
- [<span data-ttu-id="79391-137">TelUriAddress</span><span class="sxs-lookup"><span data-stu-id="79391-137">TelUriAddress</span></span>](teluriaddress.md)
    
- [<span data-ttu-id="79391-138">ImContactSipUriAddress</span><span class="sxs-lookup"><span data-stu-id="79391-138">ImContactSipUriAddress</span></span>](imcontactsipuriaddress.md)
    
- [<span data-ttu-id="79391-139">ImTelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="79391-139">ImTelephoneNumber</span></span>](imtelephonenumber.md)
    
- [<span data-ttu-id="79391-140">GroupId</span><span class="sxs-lookup"><span data-stu-id="79391-140">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewteluricontacttogroup-operation-response"></a><span data-ttu-id="79391-141">成功 AddNewTelUriContactToGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="79391-141">Successful AddNewTelUriContactToGroup operation response</span></span>

<span data-ttu-id="79391-142">下面的示例演示对**AddNewTelUriContactToGroup**操作请求创建联系人成功响应。</span><span class="sxs-lookup"><span data-stu-id="79391-142">The following example shows a successful response to an **AddNewTelUriContactToGroup** operation request to create a contact.</span></span> <span data-ttu-id="79391-143">则响应中包含该联系人的相关联的角色标识符，该角色，在这种情况下根据联系人的电话号码，以及联系人的项标识符，显示为源标识符归属的一部分的显示名称。</span><span class="sxs-lookup"><span data-stu-id="79391-143">The response contains the associated persona identifier for the contact, the display name of the persona, which in this case is based on the contact's phone number, and the contact's item identifier, which is displayed as part of the source identifier attribution.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"                           
            xmlns:xsd="http://www.w3.org/2001/XMLSchema"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
   </s:Header>
   <s:Body>
      <AddNewTelUriContactToGroupResponse ResponseClass="Success" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="79391-144">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="79391-144">The response SOAP body contains following elements:</span></span>
  
- [<span data-ttu-id="79391-145">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="79391-145">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="79391-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="79391-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="79391-147">角色</span><span class="sxs-lookup"><span data-stu-id="79391-147">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="79391-148">PersonaId</span><span class="sxs-lookup"><span data-stu-id="79391-148">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="79391-149">PersonaType</span><span class="sxs-lookup"><span data-stu-id="79391-149">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="79391-150">CreationTime</span><span class="sxs-lookup"><span data-stu-id="79391-150">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="79391-151">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="79391-151">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="79391-152">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="79391-152">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="79391-153">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="79391-153">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="79391-154">FileAs</span><span class="sxs-lookup"><span data-stu-id="79391-154">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="79391-155">FileAsId</span><span class="sxs-lookup"><span data-stu-id="79391-155">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="79391-156">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="79391-156">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="79391-157">归属 (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="79391-157">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="79391-158">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="79391-158">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="79391-159">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="79391-159">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="79391-160">SourceId</span><span class="sxs-lookup"><span data-stu-id="79391-160">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="79391-161">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="79391-161">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="79391-162">IsWritable</span><span class="sxs-lookup"><span data-stu-id="79391-162">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="79391-163">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="79391-163">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="79391-164">IsHidden</span><span class="sxs-lookup"><span data-stu-id="79391-164">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="79391-165">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="79391-165">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="79391-166">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="79391-166">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="79391-167">值</span><span class="sxs-lookup"><span data-stu-id="79391-167">Value</span></span>](value.md)
    
- [<span data-ttu-id="79391-168">归属 (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="79391-168">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="79391-169">归属 （字符串）</span><span class="sxs-lookup"><span data-stu-id="79391-169">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="79391-170">OtherTelephones</span><span class="sxs-lookup"><span data-stu-id="79391-170">OtherTelephones</span></span>](othertelephones.md)
    
- [<span data-ttu-id="79391-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="79391-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="79391-172">值</span><span class="sxs-lookup"><span data-stu-id="79391-172">Value</span></span>](value.md)
    
- [<span data-ttu-id="79391-173">编号</span><span class="sxs-lookup"><span data-stu-id="79391-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="79391-174">类型 （字符串）</span><span class="sxs-lookup"><span data-stu-id="79391-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="79391-175">归属 (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="79391-175">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="79391-176">归属 （字符串）</span><span class="sxs-lookup"><span data-stu-id="79391-176">Attribution (string)</span></span>](attribution-string.md)
    
## <a name="addnewteluricontacttogroup-operation-error-response-example"></a><span data-ttu-id="79391-177">AddNewTelUriContactToGroup 操作错误响应示例</span><span class="sxs-lookup"><span data-stu-id="79391-177">AddNewTelUriContactToGroup operation error response example</span></span>

<span data-ttu-id="79391-178">下面的示例演示**AddNewTelUriContactToGroup**操作请求错误响应组标识符包含一个格式正确的值，它未识别的邮箱中的一组时。</span><span class="sxs-lookup"><span data-stu-id="79391-178">The following example shows an error response to an **AddNewTelUriContactToGroup** operation request when the group identifier contains a well-formed value that does not identify a group in the mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="545" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewTelUriContactToGroupResponse ResponseClass="Error" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddNewTelUriContactToGroupResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="79391-179">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="79391-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="79391-180">AddNewTelUriContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="79391-180">AddNewTelUriContactToGroupResponse</span></span>](addnewteluricontacttogroupresponse.md)
    
- [<span data-ttu-id="79391-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="79391-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="79391-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="79391-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="79391-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="79391-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="79391-184">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79391-184">See also</span></span>

- [<span data-ttu-id="79391-185">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="79391-185">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="79391-186">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="79391-186">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    

