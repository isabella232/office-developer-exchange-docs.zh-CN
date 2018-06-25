---
title: GetPersona 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e2146df0-53d0-4caf-9758-b600bbc14b6a
description: 查找信息 GetPersona EWS 操作。
ms.openlocfilehash: c6ac357eaa34e9bae2fe0a79a4a2d02449100e78
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754654"
---
# <a name="getpersona-operation"></a><span data-ttu-id="73cfc-103">GetPersona 操作</span><span class="sxs-lookup"><span data-stu-id="73cfc-103">GetPersona operation</span></span>

<span data-ttu-id="73cfc-104">查找有关**GetPersona** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="73cfc-104">Find information about the **GetPersona** EWS operation.</span></span> 
  
<span data-ttu-id="73cfc-105">**GetPersona**操作返回一组与角色相关联的属性。</span><span class="sxs-lookup"><span data-stu-id="73cfc-105">The **GetPersona** operation returns a set of properties that are associated with a persona.</span></span> 
  
<span data-ttu-id="73cfc-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="73cfc-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getpersona-operation"></a><span data-ttu-id="73cfc-107">使用 GetPersona 操作</span><span class="sxs-lookup"><span data-stu-id="73cfc-107">Using the GetPersona operation</span></span>

<span data-ttu-id="73cfc-108">**GetPersona**操作提供了对个人的窗体中的聚合联系信息的访问。</span><span class="sxs-lookup"><span data-stu-id="73cfc-108">The **GetPersona** operation provides access to aggregated contact information in the form of a persona.</span></span> <span data-ttu-id="73cfc-109">请求中的[PersonaId](personaid.md)元素标识角色在响应中返回。</span><span class="sxs-lookup"><span data-stu-id="73cfc-109">The [PersonaId](personaid.md) element in the request identifies the persona to return in the response.</span></span> <span data-ttu-id="73cfc-110">响应可以包含一组默认的个人属性或自定义属性集。</span><span class="sxs-lookup"><span data-stu-id="73cfc-110">The response can contain a default set of persona properties or a custom property set.</span></span> <span data-ttu-id="73cfc-111">我们建议您指定的设置，使未使用的属性不处理并从服务器发送到客户端的自定义属性。</span><span class="sxs-lookup"><span data-stu-id="73cfc-111">We recommend that you specify a custom property set so that unused properties are not processed and sent from the server to the client.</span></span> 
  
### <a name="getpersona-operation-soap-headers"></a><span data-ttu-id="73cfc-112">GetPersona 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="73cfc-112">GetPersona operation SOAP headers</span></span>

<span data-ttu-id="73cfc-113">**GetPersona**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="73cfc-113">The **GetPersona** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="73cfc-114">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="73cfc-114">**Header name**</span></span>|<span data-ttu-id="73cfc-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="73cfc-115">**Element**</span></span>|<span data-ttu-id="73cfc-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="73cfc-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="73cfc-117">**模拟**</span><span class="sxs-lookup"><span data-stu-id="73cfc-117">**Impersonation**</span></span> <br/> |[<span data-ttu-id="73cfc-118">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="73cfc-118">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="73cfc-119">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="73cfc-119">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="73cfc-120">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="73cfc-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="73cfc-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="73cfc-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="73cfc-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="73cfc-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="73cfc-123">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="73cfc-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="73cfc-124">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="73cfc-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="73cfc-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="73cfc-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="73cfc-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="73cfc-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="73cfc-127">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="73cfc-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="73cfc-128">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="73cfc-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getpersona-operation-request-example-return-a-default-set-of-properties-for-a-persona"></a><span data-ttu-id="73cfc-129">GetPersona 操作请求示例： 返回一组默认的个人属性</span><span class="sxs-lookup"><span data-stu-id="73cfc-129">GetPersona operation request example: Return a default set of properties for a persona</span></span>

<span data-ttu-id="73cfc-130">**GetPersona**操作请求的下面的示例演示如何返回一组默认的与角色相关联的属性。</span><span class="sxs-lookup"><span data-stu-id="73cfc-130">The following example of a **GetPersona** operation request shows how to return a default set of properties that are associated with a persona.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetPersona>
         <PersonaId Id="AAQkADEzAQAKtOtR/l4MlLqHWORfhSYKU="/>
      </GetPersona>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="73cfc-131">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="73cfc-131">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="73cfc-132">GetPersona</span><span class="sxs-lookup"><span data-stu-id="73cfc-132">GetPersona</span></span>](getpersona.md)
    
- [<span data-ttu-id="73cfc-133">PersonaId</span><span class="sxs-lookup"><span data-stu-id="73cfc-133">PersonaId</span></span>](personaid.md)
    
## <a name="successful-getpersona-operation-response"></a><span data-ttu-id="73cfc-134">成功 GetPersona 操作响应</span><span class="sxs-lookup"><span data-stu-id="73cfc-134">Successful GetPersona operation response</span></span>

<span data-ttu-id="73cfc-135">下面的示例演示对**GetPersona**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="73cfc-135">The following example shows a successful response to a **GetPersona** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="73cfc-136">所有项目标识符，本文中的更改项具有已截短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="73cfc-136">All item identifiers and change keys in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="432" 
                           MinorBuildNumber="5" 
                           Version="Exchange2013"
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetPersonaResponseMessage ResponseClass="Success"
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <Persona>
            <PersonaId Id="AAQkADEzAQAKtOtR="
              xmlns="http://schemas.microsoft.com/exchange/services/2006/types"/>
            <PersonaType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Person</PersonaType>
            <CreationTime xmlns="http://schemas.microsoft.com/exchange/services/2006/types">2012-06-01T17:00:34Z</CreationTime>
            <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayName>
            <DisplayNameFirstLast xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Brian Johnson</DisplayNameFirstLast>
            <DisplayNameLastFirst xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Johnson Brian</DisplayNameLastFirst>
            <FileAs xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Johnson, Brian</FileAs>
            <FileAsId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">None</FileAsId>
            <GivenName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Brian</GivenName>
            <Surname xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Johnsoon</Surname>
            <CompanyName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">Contoso</CompanyName>
            <RelevanceScore xmlns="http://schemas.microsoft.com/exchange/services/2006/types">4255550110</RelevanceScore>
            <Attributions xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <DisplayNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </DisplayNames>
            <FileAses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson, Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAses>
            <FileAsIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>None</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </FileAsIds>
            <GivenNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Brian</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </GivenNames>
            <Surnames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <StringAttributedValue>
                  <Value>Johnson</Value>
                  <Attributions>
                     <Attribution>0</Attribution>
                  </Attributions>
               </StringAttributedValue>
            </Surnames>
            <MobilePhones xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
            <CompanyNames xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="73cfc-137">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="73cfc-137">The response SOAP body contains the following elements:</span></span>
  
- <span data-ttu-id="73cfc-138">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="73cfc-138">GetPersonaResponseMessage</span></span>
    
- [<span data-ttu-id="73cfc-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="73cfc-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="73cfc-140">角色</span><span class="sxs-lookup"><span data-stu-id="73cfc-140">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="73cfc-141">PersonaId</span><span class="sxs-lookup"><span data-stu-id="73cfc-141">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="73cfc-142">PersonaType</span><span class="sxs-lookup"><span data-stu-id="73cfc-142">PersonaType</span></span>](personatype.md)
    
- [<span data-ttu-id="73cfc-143">CreationTime</span><span class="sxs-lookup"><span data-stu-id="73cfc-143">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="73cfc-144">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="73cfc-144">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="73cfc-145">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="73cfc-145">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="73cfc-146">FileAs</span><span class="sxs-lookup"><span data-stu-id="73cfc-146">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="73cfc-147">FileAsId</span><span class="sxs-lookup"><span data-stu-id="73cfc-147">FileAsId</span></span>](fileasid.md)
    
- [<span data-ttu-id="73cfc-148">GivenName</span><span class="sxs-lookup"><span data-stu-id="73cfc-148">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="73cfc-149">姓</span><span class="sxs-lookup"><span data-stu-id="73cfc-149">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="73cfc-150">公司名称</span><span class="sxs-lookup"><span data-stu-id="73cfc-150">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="73cfc-151">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="73cfc-151">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="73cfc-152">归属 (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="73cfc-152">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md)
    
- [<span data-ttu-id="73cfc-153">归属 （字符串）</span><span class="sxs-lookup"><span data-stu-id="73cfc-153">Attribution (string)</span></span>](attribution-string.md)
    
- [<span data-ttu-id="73cfc-154">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="73cfc-154">ID (String)</span></span>](id-string.md)
    
- <span data-ttu-id="73cfc-155">[SourceId](sourceid.md)SourceId</span><span class="sxs-lookup"><span data-stu-id="73cfc-155">[SourceId](sourceid.md) SourceId</span></span> 
    
- [<span data-ttu-id="73cfc-156">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="73cfc-156">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="73cfc-157">IsWritable</span><span class="sxs-lookup"><span data-stu-id="73cfc-157">IsWritable</span></span>](iswritable.md)
    
- [<span data-ttu-id="73cfc-158">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="73cfc-158">IsQuickContact</span></span>](isquickcontact.md)
    
- [<span data-ttu-id="73cfc-159">IsHidden</span><span class="sxs-lookup"><span data-stu-id="73cfc-159">IsHidden</span></span>](ishidden.md)
    
- [<span data-ttu-id="73cfc-160">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="73cfc-160">FolderId</span></span>](folderid.md)
    
- [<span data-ttu-id="73cfc-161">DisplayNames</span><span class="sxs-lookup"><span data-stu-id="73cfc-161">DisplayNames</span></span>](displaynames.md)
    
- [<span data-ttu-id="73cfc-162">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="73cfc-162">StringAttributedValue</span></span>](stringattributedvalue.md)
    
- [<span data-ttu-id="73cfc-163">值 (ArrayOfStringValueType)</span><span class="sxs-lookup"><span data-stu-id="73cfc-163">Value (ArrayOfStringValueType)</span></span>](value-arrayofstringvaluetype.md)
    
- [<span data-ttu-id="73cfc-164">归属 (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="73cfc-164">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md)
    
- [<span data-ttu-id="73cfc-165">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="73cfc-165">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
    
- [<span data-ttu-id="73cfc-166">FileAses</span><span class="sxs-lookup"><span data-stu-id="73cfc-166">FileAses</span></span>](fileases.md)
    
- [<span data-ttu-id="73cfc-167">FileAsIds</span><span class="sxs-lookup"><span data-stu-id="73cfc-167">FileAsIds</span></span>](fileasids.md)
    
- [<span data-ttu-id="73cfc-168">GivenNames</span><span class="sxs-lookup"><span data-stu-id="73cfc-168">GivenNames</span></span>](givennames.md)
    
- [<span data-ttu-id="73cfc-169">姓</span><span class="sxs-lookup"><span data-stu-id="73cfc-169">Surnames</span></span>](surnames.md)
    
- [<span data-ttu-id="73cfc-170">MobilePhones</span><span class="sxs-lookup"><span data-stu-id="73cfc-170">MobilePhones</span></span>](mobilephones.md)
    
- [<span data-ttu-id="73cfc-171">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="73cfc-171">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md)
    
- [<span data-ttu-id="73cfc-172">值 (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="73cfc-172">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md)
    
- [<span data-ttu-id="73cfc-173">编号</span><span class="sxs-lookup"><span data-stu-id="73cfc-173">Number</span></span>](number.md)
    
- [<span data-ttu-id="73cfc-174">类型 （字符串）</span><span class="sxs-lookup"><span data-stu-id="73cfc-174">Type (string)</span></span>](type-string.md)
    
- [<span data-ttu-id="73cfc-175">CompanyNames</span><span class="sxs-lookup"><span data-stu-id="73cfc-175">CompanyNames</span></span>](companynames.md)
    
## <a name="getpersona-operation-error-response"></a><span data-ttu-id="73cfc-176">GetPersona 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="73cfc-176">GetPersona operation error response</span></span>

<span data-ttu-id="73cfc-177">下面的示例演示对**GetPersona**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="73cfc-177">The following example shows an error response to a **GetPersona** operation request.</span></span> <span data-ttu-id="73cfc-178">这是包含正确指定的个人标识符请求的响应。</span><span class="sxs-lookup"><span data-stu-id="73cfc-178">This is a response to a request that contains an incorrectly specified persona identifier.</span></span> 
  
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
      <GetPersonaResponseMessage ResponseClass="Error" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Id is malformed.</MessageText>
         <ResponseCode>ErrorInvalidIdMalformed</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetPersonaResponseMessage>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="73cfc-179">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="73cfc-179">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="73cfc-180">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="73cfc-180">GetPersonaResponseMessage</span></span>](getpersonaresponsemessage.md)
    
- [<span data-ttu-id="73cfc-181">MessageText</span><span class="sxs-lookup"><span data-stu-id="73cfc-181">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="73cfc-182">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="73cfc-182">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="73cfc-183">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="73cfc-183">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="73cfc-184">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="73cfc-184">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="73cfc-185">另请参阅</span><span class="sxs-lookup"><span data-stu-id="73cfc-185">See also</span></span>

- [<span data-ttu-id="73cfc-186">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="73cfc-186">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="73cfc-187">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="73cfc-187">People and contacts in EWS in Exchange</span></span>](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="73cfc-188">FindPeople 操作</span><span class="sxs-lookup"><span data-stu-id="73cfc-188">FindPeople operation</span></span>](findpeople-operation.md)
    

