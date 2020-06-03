---
title: GetPersona 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e2146df0-53d0-4caf-9758-b600bbc14b6a
description: 查找有关 GetPersona EWS 操作的信息。
ms.openlocfilehash: 2b335c694a85f87c96432ea6d7c1c674613d2f17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460944"
---
# <a name="getpersona-operation"></a><span data-ttu-id="ebeb1-103">GetPersona 操作</span><span class="sxs-lookup"><span data-stu-id="ebeb1-103">GetPersona operation</span></span>

<span data-ttu-id="ebeb1-104">查找有关**GetPersona** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-104">Find information about the **GetPersona** EWS operation.</span></span> 
  
<span data-ttu-id="ebeb1-105">**GetPersona**操作返回一组与角色相关联的属性。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-105">The **GetPersona** operation returns a set of properties that are associated with a persona.</span></span> 
  
<span data-ttu-id="ebeb1-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getpersona-operation"></a><span data-ttu-id="ebeb1-107">使用 GetPersona 操作</span><span class="sxs-lookup"><span data-stu-id="ebeb1-107">Using the GetPersona operation</span></span>

<span data-ttu-id="ebeb1-108">**GetPersona**操作提供对角色的形式的聚合联系人信息的访问。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-108">The **GetPersona** operation provides access to aggregated contact information in the form of a persona.</span></span> <span data-ttu-id="ebeb1-109">请求中的[PersonaId](personaid.md)元素标识要在响应中返回的角色。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-109">The [PersonaId](personaid.md) element in the request identifies the persona to return in the response.</span></span> <span data-ttu-id="ebeb1-110">响应可以包含一组默认的角色属性或自定义属性集。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-110">The response can contain a default set of persona properties or a custom property set.</span></span> <span data-ttu-id="ebeb1-111">我们建议您指定自定义属性集，以便不会处理未使用的属性，也不会将其从服务器发送到客户端。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-111">We recommend that you specify a custom property set so that unused properties are not processed and sent from the server to the client.</span></span> 
  
### <a name="getpersona-operation-soap-headers"></a><span data-ttu-id="ebeb1-112">GetPersona 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="ebeb1-112">GetPersona operation SOAP headers</span></span>

<span data-ttu-id="ebeb1-113">**GetPersona**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-113">The **GetPersona** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="ebeb1-114">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="ebeb1-114">**Header name**</span></span>|<span data-ttu-id="ebeb1-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="ebeb1-115">**Element**</span></span>|<span data-ttu-id="ebeb1-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="ebeb1-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebeb1-117">**模拟**</span><span class="sxs-lookup"><span data-stu-id="ebeb1-117">**Impersonation**</span></span> <br/> |[<span data-ttu-id="ebeb1-118">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="ebeb1-118">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="ebeb1-119">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-119">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="ebeb1-120">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ebeb1-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="ebeb1-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="ebeb1-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ebeb1-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ebeb1-123">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="ebeb1-124">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="ebeb1-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="ebeb1-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="ebeb1-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ebeb1-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ebeb1-127">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="ebeb1-128">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getpersona-operation-request-example-return-a-default-set-of-properties-for-a-persona"></a><span data-ttu-id="ebeb1-129">GetPersona 操作请求示例：返回角色的默认属性集</span><span class="sxs-lookup"><span data-stu-id="ebeb1-129">GetPersona operation request example: Return a default set of properties for a persona</span></span>

<span data-ttu-id="ebeb1-130">下面的**GetPersona**操作请求示例演示如何返回与角色关联的一组默认属性。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-130">The following example of a **GetPersona** operation request shows how to return a default set of properties that are associated with a persona.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GetPersona>
         <PersonaId Id="AAQkADEzAQAKtOtR/l4MlLqHWORfhSYKU="/>
      </GetPersona>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="ebeb1-131">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="ebeb1-131">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ebeb1-132">GetPersona</span><span class="sxs-lookup"><span data-stu-id="ebeb1-132">GetPersona</span></span>](getpersona.md)
    
- [<span data-ttu-id="ebeb1-133">PersonaId</span><span class="sxs-lookup"><span data-stu-id="ebeb1-133">PersonaId</span></span>](personaid.md)
    
## <a name="successful-getpersona-operation-response"></a><span data-ttu-id="ebeb1-134">成功的 GetPersona 操作响应</span><span class="sxs-lookup"><span data-stu-id="ebeb1-134">Successful GetPersona operation response</span></span>

<span data-ttu-id="ebeb1-135">下面的示例演示对**GetPersona**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-135">The following example shows a successful response to a **GetPersona** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ebeb1-136">本文中的所有项目标识符和更改密钥都已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="432" 
                           MinorBuildNumber="5" 
                           Version="Exchange2013"
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetPersonaResponseMessage ResponseClass="Success"
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <PersonaId Id="AAQkADEzAQAKtOtR="
              xmlns="https://schemas.microsoft.com/exchange/services/2006/types"/>
            <PersonaType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
            <CreationTime xmlns="https://schemas.microsoft.com/exchange/services/2006/types">2012-06-01T17:00:34Z</CreationTime>
            <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayName>
            <DisplayNameFirstLast xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayNameFirstLast>
            <DisplayNameLastFirst xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Johnson Brian</DisplayNameLastFirst>
            <FileAs xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Johnson, Brian</FileAs>
            <FileAsId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
            <GivenName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Brian</GivenName>
            <Surname xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Johnsoon</Surname>
            <CompanyName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">Contoso</CompanyName>
            <RelevanceScore xmlns="https://schemas.microsoft.com/exchange/services/2006/types">4255550110</RelevanceScore>
            <Attributions xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Attribution>
                  <Id>0</Id>
                  <SourceId Id="AAMkA =" ChangeKey="EQAAABY+"/>
                  <DisplayName>Outlook</DisplayName>
                  <IsWritable>true</IsWritable>
                  <IsQuickContact>false</IsQuickContact>
                  <IsHidden>false</IsHidden>
                  <FolderId Id="AAMkA=" ChangeKey="AQAAAA=="/>
               </Attribution>
            </Attributions>
            <DisplayNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </DisplayNames>
            <FileAses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson, Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAses>
            <FileAsIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>None</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAsIds>
            <GivenNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </GivenNames>
            <Surnames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </Surnames>
            <MobilePhones xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <PhoneNumberAttributedValue>
                  <Value>
                     <Number>(425)555-0110</Number>
                     <Type>Mobile</Type>
                  </Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </PhoneNumberAttributedValue>
            </MobilePhones>
            <CompanyNames xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Contoso</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </CompanyNames>
         </Persona>
      </GetPersonaResponseMessage>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="ebeb1-137">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="ebeb1-137">The response SOAP body contains the following elements:</span></span>
  
- <span data-ttu-id="ebeb1-138">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ebeb1-138">GetPersonaResponseMessage</span></span>
    
- [<span data-ttu-id="ebeb1-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ebeb1-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ebeb1-140">角色</span><span class="sxs-lookup"><span data-stu-id="ebeb1-140">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="ebeb1-141">PersonaId</span><span class="sxs-lookup"><span data-stu-id="ebeb1-141">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="ebeb1-142">PersonaType</span><span class="sxs-lookup"><span data-stu-id="ebeb1-142">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="ebeb1-143">CreationTime</span><span class="sxs-lookup"><span data-stu-id="ebeb1-143">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="ebeb1-144">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="ebeb1-144">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="ebeb1-145">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="ebeb1-145">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="ebeb1-146">FileAs</span><span class="sxs-lookup"><span data-stu-id="ebeb1-146">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="ebeb1-147">FileAsId</span><span class="sxs-lookup"><span data-stu-id="ebeb1-147">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="ebeb1-148">GivenName</span><span class="sxs-lookup"><span data-stu-id="ebeb1-148">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="ebeb1-149">姓氏</span><span class="sxs-lookup"><span data-stu-id="ebeb1-149">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="ebeb1-150">CompanyName</span><span class="sxs-lookup"><span data-stu-id="ebeb1-150">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="ebeb1-151">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="ebeb1-151">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="ebeb1-152">归属（ArrayOfValueAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="ebeb1-152">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="ebeb1-153">特性（string）</span><span class="sxs-lookup"><span data-stu-id="ebeb1-153">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="ebeb1-154">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="ebeb1-154">ID (String)</span></span>](id-string.md)
    
- <span data-ttu-id="ebeb1-155">[SourceId](sourceid.md)SourceId</span><span class="sxs-lookup"><span data-stu-id="ebeb1-155">[SourceId](sourceid.md) SourceId</span></span> 
    
- [<span data-ttu-id="ebeb1-156">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="ebeb1-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="ebeb1-157">IsWritable</span><span class="sxs-lookup"><span data-stu-id="ebeb1-157">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="ebeb1-158">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="ebeb1-158">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="ebeb1-159">IsHidden</span><span class="sxs-lookup"><span data-stu-id="ebeb1-159">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="ebeb1-160">FolderId</span><span class="sxs-lookup"><span data-stu-id="ebeb1-160">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="ebeb1-161">DisplayNames</span><span class="sxs-lookup"><span data-stu-id="ebeb1-161">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="ebeb1-162">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="ebeb1-162">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="ebeb1-163">Value （ArrayOfStringValueType）</span><span class="sxs-lookup"><span data-stu-id="ebeb1-163">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="ebeb1-164">归属（ArrayOfPersonaAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="ebeb1-164">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="ebeb1-165">归属（PersonaAttributionType）</span><span class="sxs-lookup"><span data-stu-id="ebeb1-165">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="ebeb1-166">FileAses</span><span class="sxs-lookup"><span data-stu-id="ebeb1-166">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="ebeb1-167">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="ebeb1-167">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="ebeb1-168">GivenNames</span><span class="sxs-lookup"><span data-stu-id="ebeb1-168">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="ebeb1-169">Surnames</span><span class="sxs-lookup"><span data-stu-id="ebeb1-169">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="ebeb1-170">MobilePhones</span><span class="sxs-lookup"><span data-stu-id="ebeb1-170">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="ebeb1-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="ebeb1-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="ebeb1-172">Value （PersonaPhoneNumberType）</span><span class="sxs-lookup"><span data-stu-id="ebeb1-172">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md)
    
- [<span data-ttu-id="ebeb1-173">Number</span><span class="sxs-lookup"><span data-stu-id="ebeb1-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="ebeb1-174">类型（字符串）</span><span class="sxs-lookup"><span data-stu-id="ebeb1-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="ebeb1-175">CompanyNames</span><span class="sxs-lookup"><span data-stu-id="ebeb1-175">CompanyNames</span></span>](companynames.md)
    
## <a name="getpersona-operation-error-response"></a><span data-ttu-id="ebeb1-176">GetPersona 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="ebeb1-176">GetPersona operation error response</span></span>

<span data-ttu-id="ebeb1-177">下面的示例演示对**GetPersona**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-177">The following example shows an error response to a **GetPersona** operation request.</span></span> <span data-ttu-id="ebeb1-178">这是对包含错误指定的角色标识符的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-178">This is a response to a request that contains an incorrectly specified persona identifier.</span></span> 
  
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
      <GetPersonaResponseMessage ResponseClass="Error" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Id is malformed.</MessageText>
         <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetPersonaResponseMessage>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="ebeb1-179">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="ebeb1-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="ebeb1-180">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ebeb1-180">GetPersonaResponseMessage</span></span>](getpersonaresponsemessage.md)
    
- [<span data-ttu-id="ebeb1-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="ebeb1-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="ebeb1-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ebeb1-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ebeb1-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ebeb1-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="ebeb1-184">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="ebeb1-184">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ebeb1-185">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ebeb1-185">See also</span></span>

- [<span data-ttu-id="ebeb1-186">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="ebeb1-186">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="ebeb1-187">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="ebeb1-187">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="ebeb1-188">FindPeople 操作</span><span class="sxs-lookup"><span data-stu-id="ebeb1-188">FindPeople operation</span></span>](findpeople-operation.md)
    

