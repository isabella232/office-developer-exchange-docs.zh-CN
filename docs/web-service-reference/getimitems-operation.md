---
title: GetImItems 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 51186691-46d2-4d5c-b8bc-4ee2bb20fbe7
description: 查找有关 GetImItems EWS 操作的信息。
ms.openlocfilehash: 960f4683dd478b0e5f8cf18fa8d1593b7433a249
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456043"
---
# <a name="getimitems-operation"></a><span data-ttu-id="c0359-103">GetImItems 操作</span><span class="sxs-lookup"><span data-stu-id="c0359-103">GetImItems operation</span></span>

<span data-ttu-id="c0359-104">查找有关**GetImItems** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="c0359-104">Find information about the **GetImItems** EWS operation.</span></span> 
  
<span data-ttu-id="c0359-105">**GetImItems**操作检索有关即时消息（IM）组和 IM 联系人角色的信息。</span><span class="sxs-lookup"><span data-stu-id="c0359-105">The **GetImItems** operation retrieves information about instant messaging (IM) groups and IM contact personas.</span></span> 
  
<span data-ttu-id="c0359-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="c0359-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getimitems-operation"></a><span data-ttu-id="c0359-107">使用 GetImItems 操作</span><span class="sxs-lookup"><span data-stu-id="c0359-107">Using the GetImItems operation</span></span>

<span data-ttu-id="c0359-108">**GetImItems**操作接受组和联系人项目标识符，并返回有关组和联系人的一组信息。</span><span class="sxs-lookup"><span data-stu-id="c0359-108">The **GetImItems** operation accepts group and contact item identifiers and returns a set of information about the groups and contacts.</span></span> <span data-ttu-id="c0359-109">在响应中返回的属性集由扩展属性、多个联系人标识符、组标识符和扩展属性定义标识为参数。</span><span class="sxs-lookup"><span data-stu-id="c0359-109">The property sets returned in the response are identified by extended properties, multiple contact identifiers, group identifiers, and extended property definitions as arguments.</span></span> 
  
### <a name="getimitems-operation-soap-headers"></a><span data-ttu-id="c0359-110">GetImItems 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="c0359-110">GetImItems operation SOAP headers</span></span>

<span data-ttu-id="c0359-111">**GetImItems**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="c0359-111">The **GetImItems** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c0359-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="c0359-112">**Header name**</span></span>|<span data-ttu-id="c0359-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0359-113">**Element**</span></span>|<span data-ttu-id="c0359-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0359-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0359-115">**模拟**</span><span class="sxs-lookup"><span data-stu-id="c0359-115">**Impersonation**</span></span> <br/> |[<span data-ttu-id="c0359-116">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="c0359-116">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="c0359-117">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="c0359-117">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="c0359-118">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c0359-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c0359-119">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="c0359-119">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="c0359-120">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="c0359-120">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="c0359-121">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="c0359-121">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="c0359-122">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c0359-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c0359-123">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c0359-123">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c0359-124">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c0359-124">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c0359-125">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="c0359-125">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c0359-126">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="c0359-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c0359-127">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c0359-127">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c0359-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c0359-128">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c0359-129">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="c0359-129">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c0359-130">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="c0359-130">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getimitems-operation-request-example-get-detailed-information-about-im-contacts-and-groups"></a><span data-ttu-id="c0359-131">GetImItems 操作请求示例：获取有关 IM 联系人和组的详细信息</span><span class="sxs-lookup"><span data-stu-id="c0359-131">GetImItems operation request example: Get detailed information about IM contacts and groups</span></span>

<span data-ttu-id="c0359-132">以下示例的**GetImItems**操作请求显示如何请求有关 IM 联系人和组的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c0359-132">The following example of a **GetImItems** operation request shows how to request detailed information about IM contacts and groups.</span></span> <span data-ttu-id="c0359-133">**GetImItems**操作可以请求一个或多个联系人或组的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c0359-133">A **GetImItems** operation can request one or more contact or group details.</span></span> <span data-ttu-id="c0359-134">您还可以使用扩展属性获取组和联系人的自定义属性。</span><span class="sxs-lookup"><span data-stu-id="c0359-134">You can also use extended properties to get custom properties on groups and contacts.</span></span> <span data-ttu-id="c0359-135">如果某一项上不存在请求的扩展属性，则响应将忽略所请求的属性，并返回默认属性集的响应。</span><span class="sxs-lookup"><span data-stu-id="c0359-135">If a requested extended property does not exist on an item, the response will ignore the requested property and return the response for the default property set.</span></span> <span data-ttu-id="c0359-136">本示例演示如何使用扩展属性获取显示名称。</span><span class="sxs-lookup"><span data-stu-id="c0359-136">This example shows you how to get the display name by using extended properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c0359-137">本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="c0359-137">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> <span data-ttu-id="c0359-138">请注意，服务将忽略此操作的更改键。</span><span class="sxs-lookup"><span data-stu-id="c0359-138">Note that change keys are ignored by the service for this operation.</span></span> 
  
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
      <m:GetImItems>
         <m:ContactIds>
            <t:ItemId Id="AAMkADEzOTExYACABmEhpSAAA=" ChangeKey="EQAAABBmNDjF"/>
         </m:ContactIds>
         <m:GroupIds>
            <t:ItemId Id="AAMkADEzOTExYjJkBY7+0EAAA=" ChangeKey="EgAAAA=="/>
         </m:GroupIds>         
         <m:ExtendedProperties>
            <t:ExtendedProperty PropertyTag="0x3001" PropertyType="String"/>
         </m:ExtendedProperties>
      </m:GetImItems>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c0359-139">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c0359-139">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c0359-140">GetImItems</span><span class="sxs-lookup"><span data-stu-id="c0359-140">GetImItems</span></span>](getimitems.md)
    
- [<span data-ttu-id="c0359-141">ContactIds</span><span class="sxs-lookup"><span data-stu-id="c0359-141">ContactIds</span></span>](contactids.md)
    
- [<span data-ttu-id="c0359-142">ItemId</span><span class="sxs-lookup"><span data-stu-id="c0359-142">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="c0359-143">Groupid</span><span class="sxs-lookup"><span data-stu-id="c0359-143">GroupIds</span></span>](groupids.md)
    
- [<span data-ttu-id="c0359-144">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span><span class="sxs-lookup"><span data-stu-id="c0359-144">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span></span>](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [<span data-ttu-id="c0359-145">ExtendedProperty （PathToExtendedFieldType）</span><span class="sxs-lookup"><span data-stu-id="c0359-145">ExtendedProperty (PathToExtendedFieldType)</span></span>](extendedproperty-pathtoextendedfieldtype.md)
    
## <a name="successful-getimitems-operation-response"></a><span data-ttu-id="c0359-146">成功的 GetImItems 操作响应</span><span class="sxs-lookup"><span data-stu-id="c0359-146">Successful GetImItems operation response</span></span>

<span data-ttu-id="c0359-147">以下示例显示了对获取 IM 联系人和组的**GetImItems**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="c0359-147">The following example shows a successful response to a **GetImItems** request to get an IM contact and group.</span></span> <span data-ttu-id="c0359-148">在扩展属性中请求显示名称。</span><span class="sxs-lookup"><span data-stu-id="c0359-148">The display name is requested in an extended property.</span></span> <span data-ttu-id="c0359-149">IM 联系人以角色的形式返回。</span><span class="sxs-lookup"><span data-stu-id="c0359-149">IM contacts are returned in the form of a persona.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetImItemsResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImItemList>
            <Groups xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <ImGroup>
                  <DisplayName>Exchange SDK Team</DisplayName>
                  <GroupType>IPM.DistList.MOC.UserGroup</GroupType>
                  <ExchangeStoreId Id="AAMkADEzQrAABY7+0EAAA=" ChangeKey="EgAAAA=="/>
                  <MemberCorrelationKey>
                     <ItemId Id="AAMkADEzOTExYjeGgGqm4QrAABmEhpSAAA=" ChangeKey="EQAAAA=="/>
                  </MemberCorrelationKey>
                  <ExtendedProperties>
                     <ExtendedProperty>
                        <ExtendedFieldURI PropertyTag="0x3001" PropertyType="String"/>
                        <Value>Exchange SDK Team</Value>
                     </ExtendedProperty>
                  </ExtendedProperties>
               </ImGroup>
            </Groups>
            <Personas xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Persona>
                  <PersonaId Id="AAQkADEzOTBZImBzN5J/uHXc="/>
                  <PersonaType>Person</PersonaType>
                  <CreationTime>2012-11-07T00:10:35Z</CreationTime>
                  <DisplayName>Tony Smith</DisplayName>
                  <DisplayNameFirstLast>Tony Smith</DisplayNameFirstLast>
                  <DisplayNameLastFirst>Tony Smith</DisplayNameLastFirst>
                  <FileAs/>
                  <FileAsId>None</FileAsId>
                  <ImAddress>tsmith@contoso.com</ImAddress>
                  <RelevanceScore>2147483647</RelevanceScore>
                  <Attributions>
                     <Attribution>
                        <Id>0</Id>
                        <SourceId Id="AAMkADEzhQaoeGgGqm4QrAABmEhpSAAA=" ChangeKey="EQArAABmNDjF"/>
                        <DisplayName>Lync Contacts</DisplayName>
                        <IsWritable>false</IsWritable>
                        <IsQuickContact>true</IsQuickContact>
                        <IsHidden>false</IsHidden>
                     </Attribution>
                  </Attributions>
                  <DisplayNames>
                     <StringAttributedValue>
                        <Value>Tony Smith</Value>
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
                  <ImAddresses>
                     <StringAttributedValue>
                        <Value>tsmith@contoso.com</Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </StringAttributedValue>
                  </ImAddresses>
                  <ExtendedProperties>
                     <ExtendedPropertyAttributedValue>
                        <Value>
                           <ExtendedFieldURI PropertyTag="0x3001" PropertyType="String"/>
                           <Value>Tony Smith</Value>
                        </Value>
                        <Attributions>
                           <Attribution>0</Attribution>
                        </Attributions>
                     </ExtendedPropertyAttributedValue>
                  </ExtendedProperties>
               </Persona>
            </Personas>
         </ImItemList>
      </GetImItemsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="c0359-150">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c0359-150">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c0359-151">GetImItemsResponse</span><span class="sxs-lookup"><span data-stu-id="c0359-151">GetImItemsResponse</span></span>](getimitemsresponse.md)
    
- [<span data-ttu-id="c0359-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c0359-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c0359-153">ImItemList</span><span class="sxs-lookup"><span data-stu-id="c0359-153">ImItemList</span></span>](imitemlist.md)
    
- [<span data-ttu-id="c0359-154">组（ArrayOfImGroupType）</span><span class="sxs-lookup"><span data-stu-id="c0359-154">Groups (ArrayOfImGroupType)</span></span>](groups-arrayofimgrouptype.md)
    
- [<span data-ttu-id="c0359-155">ImGroup</span><span class="sxs-lookup"><span data-stu-id="c0359-155">ImGroup</span></span>](imgroup.md)
    
- [<span data-ttu-id="c0359-156">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="c0359-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="c0359-157">GroupType</span><span class="sxs-lookup"><span data-stu-id="c0359-157">GroupType</span></span>](grouptype.md)
    
- [<span data-ttu-id="c0359-158">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="c0359-158">ExchangeStoreId</span></span>](exchangestoreid.md)
    
- [<span data-ttu-id="c0359-159">MemberCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="c0359-159">MemberCorrelationKey</span></span>](membercorrelationkey.md)
    
- [<span data-ttu-id="c0359-160">ItemId</span><span class="sxs-lookup"><span data-stu-id="c0359-160">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="c0359-161">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span><span class="sxs-lookup"><span data-stu-id="c0359-161">ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)</span></span>](extendedproperties-nonemptyarrayofextendedfielduris.md)
    
- [<span data-ttu-id="c0359-162">ExtendedProperty （PathToExtendedFieldType）</span><span class="sxs-lookup"><span data-stu-id="c0359-162">ExtendedProperty (PathToExtendedFieldType)</span></span>](extendedproperty-pathtoextendedfieldtype.md)
    
- [<span data-ttu-id="c0359-163">人数</span><span class="sxs-lookup"><span data-stu-id="c0359-163">Personas</span></span>](personas-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c0359-164">PersonaId</span><span class="sxs-lookup"><span data-stu-id="c0359-164">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="c0359-165">PersonaType</span><span class="sxs-lookup"><span data-stu-id="c0359-165">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="c0359-166">CreationTime</span><span class="sxs-lookup"><span data-stu-id="c0359-166">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="c0359-167">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="c0359-167">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="c0359-168">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="c0359-168">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="c0359-169">FileAs</span><span class="sxs-lookup"><span data-stu-id="c0359-169">FileAs</span></span>](fileas.md)
    
- <span data-ttu-id="c0359-170">[FileAsId](fileasid.md)FileAsId</span><span class="sxs-lookup"><span data-stu-id="c0359-170">[FileAsId](fileasid.md) FileAsId</span></span> 
    
- [<span data-ttu-id="c0359-171">ImAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="c0359-171">ImAddress (String)</span></span>](imaddress-string.md)
    
- [<span data-ttu-id="c0359-172">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="c0359-172">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="c0359-173">归属（ArrayOfPersonaAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="c0359-173">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="c0359-174">归属（PersonaAttributionType）</span><span class="sxs-lookup"><span data-stu-id="c0359-174">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="c0359-175">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="c0359-175">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="c0359-176">SourceId</span><span class="sxs-lookup"><span data-stu-id="c0359-176">SourceId</span></span>](sourceid.md)
    
- [<span data-ttu-id="c0359-177">IsWritable</span><span class="sxs-lookup"><span data-stu-id="c0359-177">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="c0359-178">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="c0359-178">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="c0359-179">IsHidden</span><span class="sxs-lookup"><span data-stu-id="c0359-179">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="c0359-180">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="c0359-180">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="c0359-181">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="c0359-181">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="c0359-182">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="c0359-182">ImAddresses</span></span>](imaddresses.md)
    
- [<span data-ttu-id="c0359-183">Value （ExtendedPropertyType）</span><span class="sxs-lookup"><span data-stu-id="c0359-183">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md)
    
## <a name="getimitems-operation-error-response"></a><span data-ttu-id="c0359-184">GetImItems 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="c0359-184">GetImItems operation error response</span></span>

<span data-ttu-id="c0359-185">如果向服务提供了无效的联系人或组标识符，则**GetImItems**操作不会验证标识符，也不会返回预期的**ErrorInvalidImContactId**或**ErrorInvalidImGroupId**错误响应。</span><span class="sxs-lookup"><span data-stu-id="c0359-185">The **GetImItems** operation does not validate identifiers and will not return the expected **ErrorInvalidImContactId** or **ErrorInvalidImGroupId** error response if an invalid contact or group identifier is provided to the service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0359-186">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0359-186">See also</span></span>

- [<span data-ttu-id="c0359-187">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="c0359-187">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="c0359-188">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="c0359-188">GetImItemList operation</span></span>](getimitemlist-operation.md)
    

