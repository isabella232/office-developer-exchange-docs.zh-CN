---
title: FindPeople 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 446106b7-ff2d-4107-90c1-29f4d38ba128
description: 查找有关 FindPeople EWS 操作的信息。
ms.openlocfilehash: ab5edc3f140e34123ce1f009c401ddd61a0e2598
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462906"
---
# <a name="findpeople-operation"></a><span data-ttu-id="505e3-103">FindPeople 操作</span><span class="sxs-lookup"><span data-stu-id="505e3-103">FindPeople operation</span></span>

<span data-ttu-id="505e3-104">查找有关**FindPeople** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="505e3-104">Find information about the **FindPeople** EWS operation.</span></span> 
  
<span data-ttu-id="505e3-105">**FindPeople**操作返回指定的 "联系人" 文件夹中的所有 persona 对象，或检索与指定的查询字符串匹配的联系人。</span><span class="sxs-lookup"><span data-stu-id="505e3-105">The **FindPeople** operation returns all persona objects from a specified Contacts folder or retrieves contacts that match a specified query string.</span></span> 
  
<span data-ttu-id="505e3-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="505e3-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-findpeople-operation"></a><span data-ttu-id="505e3-107">使用 FindPeople 操作</span><span class="sxs-lookup"><span data-stu-id="505e3-107">Using the FindPeople operation</span></span>

<span data-ttu-id="505e3-108">**FindPeople**操作返回聚合的联系人信息。</span><span class="sxs-lookup"><span data-stu-id="505e3-108">The **FindPeople** operation returns aggregated contact information.</span></span> 
  
<span data-ttu-id="505e3-109">**FindPeople**操作通过添加聚合限制和返回其他属性的功能，建立基于[限制](restriction.md)和[BaseShape](baseshape.md)复杂类型的现有功能。</span><span class="sxs-lookup"><span data-stu-id="505e3-109">The **FindPeople** operation builds on the existing functionality of the [Restriction](restriction.md) and [BaseShape](baseshape.md) complex types by adding an aggregation restriction and the ability to return additional properties.</span></span> <span data-ttu-id="505e3-110">通过使用限制，客户端可以指定筛选器，例如 "仅返回具有 IM 地址的结果"。</span><span class="sxs-lookup"><span data-stu-id="505e3-110">By using a restriction, a client can specify filters such as "only return results that have an IM address".</span></span> <span data-ttu-id="505e3-111">默认搜索行为针对指定用户的个人邮箱和全局地址列表（GAL）。</span><span class="sxs-lookup"><span data-stu-id="505e3-111">The default search behavior targets both the specified user's personal mailbox and the global address list (GAL).</span></span> <span data-ttu-id="505e3-112">在将 GAL 作为主搜索文件夹进行搜索时，必须指定查询字符串而不是限制，因为此操作不允许浏览 GAL。</span><span class="sxs-lookup"><span data-stu-id="505e3-112">When searching the GAL as the primary search folder, you must specify a query string instead of a restriction, because this operation does not allow for browsing of the GAL.</span></span> 
  
### <a name="findpeople-operation-soap-headers"></a><span data-ttu-id="505e3-113">FindPeople 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="505e3-113">FindPeople operation SOAP headers</span></span>

<span data-ttu-id="505e3-114">**FindPeople**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="505e3-114">The **FindPeople** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="505e3-115">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="505e3-115">**Header name**</span></span>|<span data-ttu-id="505e3-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="505e3-116">**Element**</span></span>|<span data-ttu-id="505e3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="505e3-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="505e3-118">**模拟**</span><span class="sxs-lookup"><span data-stu-id="505e3-118">**Impersonation**</span></span> <br/> |[<span data-ttu-id="505e3-119">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="505e3-119">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="505e3-120">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="505e3-120">Identifies the user whom the client application is impersonating.</span></span> <span data-ttu-id="505e3-121">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="505e3-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="505e3-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="505e3-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="505e3-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="505e3-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="505e3-124">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="505e3-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="505e3-125">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="505e3-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="505e3-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="505e3-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="505e3-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="505e3-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="505e3-128">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="505e3-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="505e3-129">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="505e3-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="findpeople-operation-request-example"></a><span data-ttu-id="505e3-130">FindPeople 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="505e3-130">FindPeople operation request example</span></span>

<span data-ttu-id="505e3-131">以下示例的**FindPeople**操作请求显示如何从 "联系人" 文件夹中返回前100个联系人。</span><span class="sxs-lookup"><span data-stu-id="505e3-131">The following example of a **FindPeople** operation request shows how to return the first 100 contacts from the Contacts folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:FindPeople>
         <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
         <m:ParentFolderId>
            <t:DistinguishedFolderId Id="contacts"/>
         </m:ParentFolderId>
      </m:FindPeople>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="505e3-132">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="505e3-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="505e3-133">FindPeople</span><span class="sxs-lookup"><span data-stu-id="505e3-133">FindPeople</span></span>](findpeople.md)
    
- [<span data-ttu-id="505e3-134">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="505e3-134">IndexedPageItemView</span></span>](indexedpageitemview.md)
    
- [<span data-ttu-id="505e3-135">ParentFolderId （TargetFolderIdType）</span><span class="sxs-lookup"><span data-stu-id="505e3-135">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)
    
- [<span data-ttu-id="505e3-136">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="505e3-136">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
<span data-ttu-id="505e3-137">下面的**FindPeople**操作请求示例演示如何使用查询字符串从 GAL 中返回前100个联系人。</span><span class="sxs-lookup"><span data-stu-id="505e3-137">The following example of a **FindPeople** operation request shows how to return the first 100 contacts from the GAL by using a query string.</span></span> <span data-ttu-id="505e3-138">将**DistinguishedFolderId**设置为 "directory" 将在 GAL 中搜索 GAL 作为角色的主要来源。</span><span class="sxs-lookup"><span data-stu-id="505e3-138">Setting the **DistinguishedFolderId** to "directory" will search the GAL as the primary source of personas.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
    <m:FindPeople>
      <m:PersonaShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="persona:DisplayName"/>
          <t:FieldURI FieldURI="persona:Title"/>
        </t:AdditionalProperties>
      </m:PersonaShape>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="directory"/>
      </m:ParentFolderId>
      <m:QueryString>adams</m:QueryString>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-findpeople-operation-response"></a><span data-ttu-id="505e3-139">成功的 FindPeople 操作响应</span><span class="sxs-lookup"><span data-stu-id="505e3-139">Successful FindPeople operation response</span></span>

<span data-ttu-id="505e3-140">下面的示例演示对**FindPeople**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="505e3-140">The following example shows a successful response to a **FindPeople** operation request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope 
   xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
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
    <FindPeopleResponse ResponseClass="Success" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <People>
        <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <PersonaId Id="AAQkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MTYzNGNkZmRkYQAQAOjFqObcLmtOlzlRnHdXQjo=" />
          <CreationTime>2012-01-11T22:25:37Z</CreationTime>
          <DisplayName>Terry Adams</DisplayName>
          <DisplayNameFirstLast>Terry Adams</DisplayNameFirstLast>
          <DisplayNameLastFirst>Adams Terry</DisplayNameLastFirst>
          <FileAs>Adams, Terry</FileAs>
          <GivenName>Terry</GivenName>
          <Surname>Adams</Surname>
          <EmailAddress>
            <Name>terry@litwareinc.com</Name>
            <EmailAddress>terry@litwareinc.com</EmailAddress>
            <RoutingType>SMTP</RoutingType>
          </EmailAddress>
          <EmailAddresses>
            <EmailAddress>
              <Name>terry@litwareinc.com</Name>
              <EmailAddress>terry@litwareinc.com</EmailAddress>
              <RoutingType>SMTP</RoutingType>
            </EmailAddress>
            <EmailAddress>
              <Name>tadams@contoso.com</Name>
              <EmailAddress>tadams@contoso.com</EmailAddress>
              <RoutingType>SMTP</RoutingType>
            </EmailAddress>
          </EmailAddresses>
          <RelevanceScore>2147483647</RelevanceScore>
        </Persona>
      </People>
      <TotalNumberOfPeopleInView>1</TotalNumberOfPeopleInView>
    </FindPeopleResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="505e3-141">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="505e3-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="505e3-142">FindPeopleResponse</span><span class="sxs-lookup"><span data-stu-id="505e3-142">FindPeopleResponse</span></span>](findpeopleresponse.md)
    
- [<span data-ttu-id="505e3-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="505e3-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="505e3-144">人员</span><span class="sxs-lookup"><span data-stu-id="505e3-144">People</span></span>](people.md)
    
- [<span data-ttu-id="505e3-145">角色</span><span class="sxs-lookup"><span data-stu-id="505e3-145">Persona</span></span>](persona.md)
    
- [<span data-ttu-id="505e3-146">PersonaId</span><span class="sxs-lookup"><span data-stu-id="505e3-146">PersonaId</span></span>](personaid.md)
    
- [<span data-ttu-id="505e3-147">CreationTime</span><span class="sxs-lookup"><span data-stu-id="505e3-147">CreationTime</span></span>](creationtime.md)
    
- [<span data-ttu-id="505e3-148">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="505e3-148">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="505e3-149">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="505e3-149">DisplayNameFirstLast</span></span>](displaynamefirstlast.md)
    
- [<span data-ttu-id="505e3-150">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="505e3-150">DisplayNameLastFirst</span></span>](displaynamelastfirst.md)
    
- [<span data-ttu-id="505e3-151">FileAs</span><span class="sxs-lookup"><span data-stu-id="505e3-151">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="505e3-152">GivenName</span><span class="sxs-lookup"><span data-stu-id="505e3-152">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="505e3-153">姓氏</span><span class="sxs-lookup"><span data-stu-id="505e3-153">Surname</span></span>](surname.md)
    
- [<span data-ttu-id="505e3-154">EmailAddresses （ArrayOfEmailAddressesType）</span><span class="sxs-lookup"><span data-stu-id="505e3-154">EmailAddresses (ArrayOfEmailAddressesType)</span></span>](emailaddresses-arrayofemailaddressestype.md)
    
- [<span data-ttu-id="505e3-155">EmailAddress （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="505e3-155">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="505e3-156">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="505e3-156">Name (EmailAddressType)</span></span>](name-emailaddresstype.md)
    
- [<span data-ttu-id="505e3-157">EmailAddress （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="505e3-157">EmailAddress (EmailAddressType)</span></span>](emailaddress-emailaddresstype.md)
    
- [<span data-ttu-id="505e3-158">RoutingType （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="505e3-158">RoutingType (EmailAddressType)</span></span>](routingtype-emailaddresstype.md)
    
- [<span data-ttu-id="505e3-159">RelevanceScore</span><span class="sxs-lookup"><span data-stu-id="505e3-159">RelevanceScore</span></span>](relevancescore.md)
    
- [<span data-ttu-id="505e3-160">TotalNumberOfPeopleInView</span><span class="sxs-lookup"><span data-stu-id="505e3-160">TotalNumberOfPeopleInView</span></span>](totalnumberofpeopleinview.md)
    
## <a name="findpeople-operation-error-response"></a><span data-ttu-id="505e3-161">FindPeople 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="505e3-161">FindPeople operation error response</span></span>

<span data-ttu-id="505e3-162">有关对 EWS 通用的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="505e3-162">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="505e3-163">另请参阅</span><span class="sxs-lookup"><span data-stu-id="505e3-163">See also</span></span>

- [<span data-ttu-id="505e3-164">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="505e3-164">People and contacts in EWS in Exchange</span></span>](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [<span data-ttu-id="505e3-165">GetPersona 操作</span><span class="sxs-lookup"><span data-stu-id="505e3-165">GetPersona operation</span></span>](getpersona-operation.md)
    

