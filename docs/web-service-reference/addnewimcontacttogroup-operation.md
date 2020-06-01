---
title: AddNewImContactToGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cb5525f-faa3-48f1-9551-df55ffc26f46
description: 查找有关 AddNewImContactToGroup EWS 操作的信息。
ms.openlocfilehash: e91cc067b4161b366e6713a9adc16873e63b1562
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465027"
---
# <a name="addnewimcontacttogroup-operation"></a><span data-ttu-id="16763-103">AddNewImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="16763-103">AddNewImContactToGroup operation</span></span>

<span data-ttu-id="16763-104">查找有关**AddNewImContactToGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="16763-104">Find information about the **AddNewImContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="16763-105">**AddNewImContactToGroup**操作将新联系人添加到即时消息（IM）组。</span><span class="sxs-lookup"><span data-stu-id="16763-105">The **AddNewImContactToGroup** operation adds a new contact to an instant messaging (IM) group.</span></span> 
  
<span data-ttu-id="16763-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="16763-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewimcontacttogroup-operation"></a><span data-ttu-id="16763-107">使用 AddNewImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="16763-107">Using the AddNewImContactToGroup operation</span></span>

<span data-ttu-id="16763-108">**AddNewImContactToGroup**操作使用以下三个参数将新联系人添加到 IM 组：</span><span class="sxs-lookup"><span data-stu-id="16763-108">The **AddNewImContactToGroup** operation takes the following three arguments to add a new contact to an IM group:</span></span> 
  
- <span data-ttu-id="16763-109">**ImAddress**属性-标识联系人的 IM 地址。</span><span class="sxs-lookup"><span data-stu-id="16763-109">**ImAddress** property - Identifies the contact's IM address.</span></span> <span data-ttu-id="16763-110">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="16763-110">This property is required.</span></span> 
    
- <span data-ttu-id="16763-111">**DisplayName**属性-标识联系人的显示名称。</span><span class="sxs-lookup"><span data-stu-id="16763-111">**DisplayName** property - Identifies the contact's display name.</span></span> 
    
- <span data-ttu-id="16763-112">**GroupId**属性-标识将联系人添加到的组。</span><span class="sxs-lookup"><span data-stu-id="16763-112">**GroupId** property - Identifies the group that the contact is added to.</span></span> 
    
<span data-ttu-id="16763-113">此操作将返回已添加到组中的联系人的角色。</span><span class="sxs-lookup"><span data-stu-id="16763-113">This operation returns the persona of the contact that was added to the group.</span></span>
  
### <a name="addnewimcontacttogroup-operation-soap-headers"></a><span data-ttu-id="16763-114">AddNewImContactToGroup 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="16763-114">AddNewImContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="16763-115">**AddNewImContactToGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="16763-115">The **AddNewImContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="16763-116">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="16763-116">**Header name**</span></span>|<span data-ttu-id="16763-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="16763-117">**Element**</span></span>|<span data-ttu-id="16763-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="16763-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16763-119">**模拟**</span><span class="sxs-lookup"><span data-stu-id="16763-119">**Impersonation**</span></span> <br/> |[<span data-ttu-id="16763-120">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="16763-120">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="16763-121">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="16763-121">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="16763-122">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="16763-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="16763-123">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="16763-123">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="16763-124">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="16763-124">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="16763-125">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="16763-125">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="16763-126">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="16763-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="16763-127">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="16763-127">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="16763-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="16763-128">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="16763-129">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="16763-129">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="16763-130">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="16763-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="16763-131">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="16763-131">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="16763-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="16763-132">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="16763-133">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="16763-133">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="16763-134">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="16763-134">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewimcontacttogroup-operation-request-example-add-a-new-im-contact-to-a-group"></a><span data-ttu-id="16763-135">AddNewImContactToGroup 操作请求示例：向组添加新的 IM 联系人</span><span class="sxs-lookup"><span data-stu-id="16763-135">AddNewImContactToGroup operation request example: Add a new IM contact to a group</span></span>

<span data-ttu-id="16763-136">以下示例的**AddNewImContactToGroup**操作请求显示如何将新联系人添加到现有 IM 组。</span><span class="sxs-lookup"><span data-stu-id="16763-136">The following example of an **AddNewImContactToGroup** operation request shows how to add a new contact to an existing IM group.</span></span> <span data-ttu-id="16763-137">此示例的**GroupId**属性值是从[AddImGroup 操作](addimgroup-operation.md)的结果返回的。</span><span class="sxs-lookup"><span data-stu-id="16763-137">The **GroupId** property value for this example was returned from results of the [AddImGroup operation](addimgroup-operation.md).</span></span> <span data-ttu-id="16763-138">**ExchangeStoreId**属性包含**GroupId**属性值。</span><span class="sxs-lookup"><span data-stu-id="16763-138">The **ExchangeStoreId** property contains the **GroupId** property value.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:AddNewImContactToGroup>
         <m:ImAddress>tsmith@contoso.com</m:ImAddress>
         <m:DisplayName>Tony Smith</m:DisplayName>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:AddNewImContactToGroup>
   </soap:Body>
</soap:Envelope>
```

> [!NOTE]
> <span data-ttu-id="16763-139">为了保持可读性， **GroupId**值已缩短。</span><span class="sxs-lookup"><span data-stu-id="16763-139">The **GroupId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="16763-140">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="16763-140">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16763-141">AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="16763-141">AddNewImContactToGroup</span></span>](addnewimcontacttogroup.md)
    
- [<span data-ttu-id="16763-142">ImAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="16763-142">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="16763-143">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="16763-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="16763-144">GroupId</span><span class="sxs-lookup"><span data-stu-id="16763-144">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewimcontacttogroup-operation-response"></a><span data-ttu-id="16763-145">成功的 AddNewImContactToGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="16763-145">Successful AddNewImContactToGroup operation response</span></span>

<span data-ttu-id="16763-146">下面的示例演示对**AddNewImContactToGroup**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="16763-146">The following example shows a successful response to an **AddNewImContactToGroup** operation request.</span></span> <span data-ttu-id="16763-147">响应包含新创建的联系人的角色。</span><span class="sxs-lookup"><span data-stu-id="16763-147">The response contains the persona of the newly created contact.</span></span> <span data-ttu-id="16763-148">该联系人将添加到 Exchange 中的 "快速联系人" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="16763-148">The contact is added to the Quick Contacts folder in Exchange.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="16763-149">为了保持可读性，标识符已被缩短。</span><span class="sxs-lookup"><span data-stu-id="16763-149">Identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="349" 
                         MinorBuildNumber="0" 
                         Version="Exchange2013" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <AddNewImContactToGroupResponse ResponseClass="Success" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Persona>
        <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MTYzNGNkZmRkYQAQAJ3EkhEEXN5KufGbSYJanZk=" 
                   xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
        <PersonaType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
        <CreationTime xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2012-01-05T23:06:58Z</CreationTime>
        <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayName>
        <DisplayNameFirstLast xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameFirstLast>
        <DisplayNameLastFirst xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameLastFirst>
        <FileAsId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
        <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Tony Smith</Name>
          <Address>tsmith@contoso.com</Address>
          <RoutingType>SMTP</RoutingType>
        </EmailAddress>
        <EmailAddresses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EmailAddress>
            <Name>Tony Smith</Name>
            <Address>tsmith@contoso.com</Address>
            <RoutingType>SMTP</RoutingType>
          </EmailAddress>
        </EmailAddresses>
        <ImAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">tsmith@contoso.com</ImAddress>
        <RelevanceScore xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2147483647</RelevanceScore>
        <Attributions xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Attribution>
            <Id>0</Id>
            <SourceId Id="BtF8oI7iVOQatt/bhQoTbWAAAAAAvcAAA=" 
                      ChangeKey="EQAAABYAAABtF8oIQoTbWAAAAAAyg" />
            <DisplayName>Outlook</DisplayName>
            <IsWritable>true</IsWritable>
            <IsQuickContact>true</IsQuickContact>
            <IsHidden>false</IsHidden>
            <FolderId Id="AAMkAGQ1MjJjMTBkLTc4YhQoTbWAAAAAAvZAAA=" 
                      ChangeKey="AQAAAA==" />
          </Attribution>
        </Attributions>
        <DisplayNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>Tony Smith</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </DisplayNames>
        <FileAsIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>None</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </FileAsIds>
        <Emails1 xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EmailAddressAttributedValue>
            <Value>
              <Name>Tony Smith</Name>
              <Address>tsmith@contoso.com</Address>
              <RoutingType>SMTP</RoutingType>
            </Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </EmailAddressAttributedValue>
        </Emails1>
        <ImAddresses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>tsmith@contoso.com</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </ImAddresses>
      </Persona>
    </AddNewImContactToGroupResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="16763-150">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="16763-150">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16763-151">AddNewImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="16763-151">AddNewImContactToGroupResponse</span></span>](addnewimcontacttogroupresponse.md)
    
- [<span data-ttu-id="16763-152">角色</span><span class="sxs-lookup"><span data-stu-id="16763-152">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="16763-153">PersonaId</span><span class="sxs-lookup"><span data-stu-id="16763-153">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="16763-154">PersonaType</span><span class="sxs-lookup"><span data-stu-id="16763-154">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="16763-155">CreationTime</span><span class="sxs-lookup"><span data-stu-id="16763-155">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="16763-156">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="16763-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="16763-157">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="16763-157">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="16763-158">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="16763-158">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="16763-159">FileAsId</span><span class="sxs-lookup"><span data-stu-id="16763-159">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="16763-160">EmailAddress （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="16763-160">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="16763-161">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="16763-161">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="16763-162">Address （string）</span><span class="sxs-lookup"><span data-stu-id="16763-162">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="16763-163">RoutingType （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="16763-163">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="16763-164">ImAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="16763-164">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="16763-165">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="16763-165">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="16763-166">归属（ArrayOfPersonaAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="16763-166">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="16763-167">归属（PersonaAttributionType）</span><span class="sxs-lookup"><span data-stu-id="16763-167">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="16763-168">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="16763-168">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="16763-169">SourceId</span><span class="sxs-lookup"><span data-stu-id="16763-169">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="16763-170">IsWritable</span><span class="sxs-lookup"><span data-stu-id="16763-170">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="16763-171">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="16763-171">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="16763-172">IsHidden</span><span class="sxs-lookup"><span data-stu-id="16763-172">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="16763-173">FolderId</span><span class="sxs-lookup"><span data-stu-id="16763-173">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="16763-174">DisplayNames</span><span class="sxs-lookup"><span data-stu-id="16763-174">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="16763-175">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="16763-175">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="16763-176">Value （ArrayOfStringValueType）</span><span class="sxs-lookup"><span data-stu-id="16763-176">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="16763-177">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="16763-177">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="16763-178">Emails1</span><span class="sxs-lookup"><span data-stu-id="16763-178">Emails1</span></span>](emails1.md)
    
- [<span data-ttu-id="16763-179">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="16763-179">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
    
- [<span data-ttu-id="16763-180">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="16763-180">ImAddresses</span></span>](imaddresses.md)
    
## <a name="addnewimcontacttogroup-operation-error-response"></a><span data-ttu-id="16763-181">AddNewImContactToGroup 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="16763-181">AddNewImContactToGroup operation error response</span></span>

<span data-ttu-id="16763-182">下面的示例演示对**AddNewImContactToGroup**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="16763-182">The following example shows an error response to a **AddNewImContactToGroup** operation request.</span></span> <span data-ttu-id="16763-183">这是对向不在请求者邮箱中的组添加联系人的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="16763-183">This is a response to a request to add a contact to a group that is not in the requester's mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="578" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewImContactToGroupResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox with such guid.</MessageText>
         <ResponseCode>ErrorNonExistentMailbox</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <MessageXml>
            <t:Value Name="MailboxGuid" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">d5fasdadcw3d-23de-2341-8f59-b71523fsddda</t:Value>
         </MessageXml>
      </AddNewImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="16763-184">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="16763-184">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16763-185">AddNewImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="16763-185">AddNewImContactToGroupResponse</span></span>](addnewimcontacttogroupresponse.md)
    
- [<span data-ttu-id="16763-186">MessageText</span><span class="sxs-lookup"><span data-stu-id="16763-186">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="16763-187">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="16763-187">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="16763-188">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="16763-188">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="16763-189">MessageXml</span><span class="sxs-lookup"><span data-stu-id="16763-189">MessageXml</span></span>](messagexml.md)
    
<span data-ttu-id="16763-190">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="16763-190">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16763-191">另请参阅</span><span class="sxs-lookup"><span data-stu-id="16763-191">See also</span></span>



[<span data-ttu-id="16763-192">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="16763-192">AddImGroup operation</span></span>](addimgroup-operation.md)
  
[<span data-ttu-id="16763-193">AddImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="16763-193">AddImContactToGroup operation</span></span>](addimcontacttogroup-operation.md)
  
[<span data-ttu-id="16763-194">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="16763-194">AddImGroup operation</span></span>](addimgroup-operation.md)
  
[<span data-ttu-id="16763-195">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="16763-195">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
  
[<span data-ttu-id="16763-196">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="16763-196">SetImGroup operation</span></span>](setimgroup-operation.md)


[<span data-ttu-id="16763-197">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="16763-197">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)

