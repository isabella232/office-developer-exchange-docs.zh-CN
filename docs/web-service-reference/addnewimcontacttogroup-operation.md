---
title: AddNewImContactToGroup 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cb5525f-faa3-48f1-9551-df55ffc26f46
description: 查找信息 AddNewImContactToGroup EWS 操作。
ms.openlocfilehash: f75b89dbb6e948431d56acb9baa93fe4d4a1d939
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753119"
---
# <a name="addnewimcontacttogroup-operation"></a><span data-ttu-id="2fa92-103">AddNewImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="2fa92-103">AddNewImContactToGroup operation</span></span>

<span data-ttu-id="2fa92-104">查找有关**AddNewImContactToGroup** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="2fa92-104">Find information about the **AddNewImContactToGroup** EWS operation.</span></span> 
  
<span data-ttu-id="2fa92-105">**AddNewImContactToGroup**操作将新的联系人添加到即时消息 (IM) 组。</span><span class="sxs-lookup"><span data-stu-id="2fa92-105">The **AddNewImContactToGroup** operation adds a new contact to an instant messaging (IM) group.</span></span> 
  
<span data-ttu-id="2fa92-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="2fa92-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-addnewimcontacttogroup-operation"></a><span data-ttu-id="2fa92-107">使用 AddNewImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="2fa92-107">Using the AddNewImContactToGroup operation</span></span>

<span data-ttu-id="2fa92-108">**AddNewImContactToGroup**操作所需的以下三个参数，将新的联系人添加到 IM 组：</span><span class="sxs-lookup"><span data-stu-id="2fa92-108">The **AddNewImContactToGroup** operation takes the following three arguments to add a new contact to an IM group:</span></span> 
  
- <span data-ttu-id="2fa92-109">**ImAddress**属性-标识联系人的 IM 地址。</span><span class="sxs-lookup"><span data-stu-id="2fa92-109">**ImAddress** property - Identifies the contact's IM address.</span></span> <span data-ttu-id="2fa92-110">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="2fa92-110">This property is required.</span></span> 
    
- <span data-ttu-id="2fa92-111">**DisplayName**属性-标识联系人的显示名称。</span><span class="sxs-lookup"><span data-stu-id="2fa92-111">**DisplayName** property - Identifies the contact's display name.</span></span> 
    
- <span data-ttu-id="2fa92-112">**GroupId**属性-标识该联系人添加到组。</span><span class="sxs-lookup"><span data-stu-id="2fa92-112">**GroupId** property - Identifies the group that the contact is added to.</span></span> 
    
<span data-ttu-id="2fa92-113">此操作返回的联系人已添加到组的角色。</span><span class="sxs-lookup"><span data-stu-id="2fa92-113">This operation returns the persona of the contact that was added to the group.</span></span>
  
### <a name="addnewimcontacttogroup-operation-soap-headers"></a><span data-ttu-id="2fa92-114">AddNewImContactToGroup 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="2fa92-114">AddNewImContactToGroup operation SOAP headers</span></span>

<span data-ttu-id="2fa92-115">**AddNewImContactToGroup**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="2fa92-115">The **AddNewImContactToGroup** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="2fa92-116">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="2fa92-116">**Header name**</span></span>|<span data-ttu-id="2fa92-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="2fa92-117">**Element**</span></span>|<span data-ttu-id="2fa92-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="2fa92-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2fa92-119">**模拟**</span><span class="sxs-lookup"><span data-stu-id="2fa92-119">**Impersonation**</span></span> <br/> |[<span data-ttu-id="2fa92-120">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="2fa92-120">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="2fa92-121">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="2fa92-121">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="2fa92-122">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="2fa92-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2fa92-123">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="2fa92-123">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="2fa92-124">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="2fa92-124">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="2fa92-125">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="2fa92-125">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="2fa92-126">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="2fa92-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2fa92-127">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="2fa92-127">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="2fa92-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2fa92-128">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2fa92-129">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="2fa92-129">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="2fa92-130">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="2fa92-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2fa92-131">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="2fa92-131">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="2fa92-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2fa92-132">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2fa92-133">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="2fa92-133">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="2fa92-134">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="2fa92-134">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="addnewimcontacttogroup-operation-request-example-add-a-new-im-contact-to-a-group"></a><span data-ttu-id="2fa92-135">AddNewImContactToGroup 操作请求示例： 向组添加新的 IM 联系人</span><span class="sxs-lookup"><span data-stu-id="2fa92-135">AddNewImContactToGroup operation request example: Add a new IM contact to a group</span></span>

<span data-ttu-id="2fa92-136">**AddNewImContactToGroup**操作请求的下面的示例演示如何向现有 IM 组中添加新联系人。</span><span class="sxs-lookup"><span data-stu-id="2fa92-136">The following example of an **AddNewImContactToGroup** operation request shows how to add a new contact to an existing IM group.</span></span> <span data-ttu-id="2fa92-137">本示例的**GroupId**属性值返回从[AddImGroup 操作](addimgroup-operation.md)的结果。</span><span class="sxs-lookup"><span data-stu-id="2fa92-137">The **GroupId** property value for this example was returned from results of the [AddImGroup operation](addimgroup-operation.md).</span></span> <span data-ttu-id="2fa92-138">**ExchangeStoreId**属性包含**GroupId**属性值。</span><span class="sxs-lookup"><span data-stu-id="2fa92-138">The **ExchangeStoreId** property contains the **GroupId** property value.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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
> <span data-ttu-id="2fa92-139">已缩短**GroupId**值，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="2fa92-139">The **GroupId** value has been shortened to preserve readability.</span></span> 
  
<span data-ttu-id="2fa92-140">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="2fa92-140">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2fa92-141">AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="2fa92-141">AddNewImContactToGroup</span></span>](addnewimcontacttogroup.md)
    
- [<span data-ttu-id="2fa92-142">ImAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="2fa92-142">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="2fa92-143">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="2fa92-143">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="2fa92-144">GroupId</span><span class="sxs-lookup"><span data-stu-id="2fa92-144">GroupId</span></span>](groupid.md)
    
## <a name="successful-addnewimcontacttogroup-operation-response"></a><span data-ttu-id="2fa92-145">成功 AddNewImContactToGroup 操作响应</span><span class="sxs-lookup"><span data-stu-id="2fa92-145">Successful AddNewImContactToGroup operation response</span></span>

<span data-ttu-id="2fa92-146">下面的示例演示对**AddNewImContactToGroup**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="2fa92-146">The following example shows a successful response to an **AddNewImContactToGroup** operation request.</span></span> <span data-ttu-id="2fa92-147">则响应中包含新创建的联系人的角色。</span><span class="sxs-lookup"><span data-stu-id="2fa92-147">The response contains the persona of the newly created contact.</span></span> <span data-ttu-id="2fa92-148">该联系人在 Exchange 添加到快速联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="2fa92-148">The contact is added to the Quick Contacts folder in Exchange.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2fa92-149">标识符具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="2fa92-149">Identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
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
    <AddNewImContactToGroupResponse ResponseClass="Success" 
                                    xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Persona>
        <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MTYzNGNkZmRkYQAQAJ3EkhEEXN5KufGbSYJanZk=" 
                   xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
        <PersonaType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
        <CreationTime xmlns="http://schemas.microsoft.com/exchange/services/2006/types">2012-01-05T23:06:58Z</CreationTime>
        <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayName>
        <DisplayNameFirstLast xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameFirstLast>
        <DisplayNameLastFirst xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Tony Smith</DisplayNameLastFirst>
        <FileAsId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
        <EmailAddress xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Tony Smith</Name>
          <Address>tsmith@contoso.com</Address>
          <RoutingType>SMTP</RoutingType>
        </EmailAddress>
        <EmailAddresses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <EmailAddress>
            <Name>Tony Smith</Name>
            <Address>tsmith@contoso.com</Address>
            <RoutingType>SMTP</RoutingType>
          </EmailAddress>
        </EmailAddresses>
        <ImAddress xmlns="http://schemas.microsoft.com/exchange/services/2006/types">tsmith@contoso.com</ImAddress>
        <RelevanceScore xmlns="http://schemas.microsoft.com/exchange/services/2006/types">2147483647</RelevanceScore>
        <Attributions xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
        <DisplayNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>Tony Smith</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </DisplayNames>
        <FileAsIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <StringAttributedValue>
            <Value>None</Value>
            <Attributions>
              <Attribution>0</Attribution>
            </Attributions>
          </StringAttributedValue>
        </FileAsIds>
        <Emails1 xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
        <ImAddresses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="2fa92-150">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="2fa92-150">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2fa92-151">AddNewImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="2fa92-151">AddNewImContactToGroupResponse</span></span>](addnewimcontacttogroupresponse.md)
    
- [<span data-ttu-id="2fa92-152">角色</span><span class="sxs-lookup"><span data-stu-id="2fa92-152">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="2fa92-153">PersonaId</span><span class="sxs-lookup"><span data-stu-id="2fa92-153">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="2fa92-154">PersonaType</span><span class="sxs-lookup"><span data-stu-id="2fa92-154">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="2fa92-155">CreationTime</span><span class="sxs-lookup"><span data-stu-id="2fa92-155">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="2fa92-156">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="2fa92-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="2fa92-157">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="2fa92-157">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="2fa92-158">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="2fa92-158">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="2fa92-159">FileAsId</span><span class="sxs-lookup"><span data-stu-id="2fa92-159">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="2fa92-160">EmailAddress (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="2fa92-160">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="2fa92-161">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="2fa92-161">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="2fa92-162">地址 （字符串）</span><span class="sxs-lookup"><span data-stu-id="2fa92-162">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="2fa92-163">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="2fa92-163">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="2fa92-164">ImAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="2fa92-164">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="2fa92-165">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="2fa92-165">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="2fa92-166">归属 (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="2fa92-166">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="2fa92-167">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="2fa92-167">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="2fa92-168">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="2fa92-168">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="2fa92-169">SourceId</span><span class="sxs-lookup"><span data-stu-id="2fa92-169">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="2fa92-170">IsWritable</span><span class="sxs-lookup"><span data-stu-id="2fa92-170">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="2fa92-171">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="2fa92-171">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="2fa92-172">IsHidden</span><span class="sxs-lookup"><span data-stu-id="2fa92-172">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="2fa92-173">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="2fa92-173">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="2fa92-174">DisplayNames</span><span class="sxs-lookup"><span data-stu-id="2fa92-174">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="2fa92-175">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2fa92-175">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="2fa92-176">值 (ArrayOfStringValueType)</span><span class="sxs-lookup"><span data-stu-id="2fa92-176">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="2fa92-177">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="2fa92-177">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="2fa92-178">Emails1</span><span class="sxs-lookup"><span data-stu-id="2fa92-178">Emails1</span></span>](emails1.md)
    
- [<span data-ttu-id="2fa92-179">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2fa92-179">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md)
    
- [<span data-ttu-id="2fa92-180">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="2fa92-180">ImAddresses</span></span>](imaddresses.md)
    
## <a name="addnewimcontacttogroup-operation-error-response"></a><span data-ttu-id="2fa92-181">AddNewImContactToGroup 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="2fa92-181">AddNewImContactToGroup operation error response</span></span>

<span data-ttu-id="2fa92-182">下面的示例演示对**AddNewImContactToGroup**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="2fa92-182">The following example shows an error response to a **AddNewImContactToGroup** operation request.</span></span> <span data-ttu-id="2fa92-183">这是对将联系人添加到请求者的邮箱中不是组的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="2fa92-183">This is a response to a request to add a contact to a group that is not in the requester's mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="578" 
                           MinorBuildNumber="11" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddNewImContactToGroupResponse ResponseClass="Error" 
                                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox with such guid.</MessageText>
         <ResponseCode>ErrorNonExistentMailbox</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <MessageXml>
            <t:Value Name="MailboxGuid" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">d5fasdadcw3d-23de-2341-8f59-b71523fsddda</t:Value>
         </MessageXml>
      </AddNewImContactToGroupResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="2fa92-184">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="2fa92-184">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2fa92-185">AddNewImContactToGroupResponse</span><span class="sxs-lookup"><span data-stu-id="2fa92-185">AddNewImContactToGroupResponse</span></span>](addnewimcontacttogroupresponse.md)
    
- [<span data-ttu-id="2fa92-186">MessageText</span><span class="sxs-lookup"><span data-stu-id="2fa92-186">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2fa92-187">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2fa92-187">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2fa92-188">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2fa92-188">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="2fa92-189">MessageXml</span><span class="sxs-lookup"><span data-stu-id="2fa92-189">MessageXml</span></span>](messagexml.md)
    
<span data-ttu-id="2fa92-190">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="2fa92-190">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2fa92-191">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2fa92-191">See also</span></span>



[<span data-ttu-id="2fa92-192">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="2fa92-192">AddImGroup operation</span></span>](addimgroup-operation.md)
  
[<span data-ttu-id="2fa92-193">AddImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="2fa92-193">AddImContactToGroup operation</span></span>](addimcontacttogroup-operation.md)
  
[<span data-ttu-id="2fa92-194">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="2fa92-194">AddImGroup operation</span></span>](addimgroup-operation.md)
  
[<span data-ttu-id="2fa92-195">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="2fa92-195">RemoveImGroup operation</span></span>](removeimgroup-operation.md)
  
[<span data-ttu-id="2fa92-196">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="2fa92-196">SetImGroup operation</span></span>](setimgroup-operation.md)


[<span data-ttu-id="2fa92-197">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="2fa92-197">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)

