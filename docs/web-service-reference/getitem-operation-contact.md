---
title: GetItem 操作 （联系人）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 6b96dace-1260-4b83-869a-7c31c5583daa
description: GetItem operation，用于从 Exchange 存储中获取联系人项目。
ms.openlocfilehash: 8d7436421f0c54a49345e8ef6b37cb442bca4277
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754600"
---
# <a name="getitem-operation-contact"></a><span data-ttu-id="efef8-103">GetItem 操作 （联系人）</span><span class="sxs-lookup"><span data-stu-id="efef8-103">GetItem operation (contact)</span></span>

<span data-ttu-id="efef8-104">GetItem operation，用于从 Exchange 存储中获取联系人项目。</span><span class="sxs-lookup"><span data-stu-id="efef8-104">The GetItem operation is used to get contact items from the Exchange store.</span></span>
  
## <a name="getitem-contact-request-example"></a><span data-ttu-id="efef8-105">GetItem （联系人） 请求示例</span><span class="sxs-lookup"><span data-stu-id="efef8-105">GetItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="efef8-106">说明</span><span class="sxs-lookup"><span data-stu-id="efef8-106">Description</span></span>

<span data-ttu-id="efef8-107">下面的示例演示如何从 Exchange 存储中获取项。</span><span class="sxs-lookup"><span data-stu-id="efef8-107">The following example shows how to get an item from the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="efef8-108">代码</span><span class="sxs-lookup"><span data-stu-id="efef8-108">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='http://schemas.microsoft.com/exchange/services/2006/messages'>
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAtAE=" ChangeKey="EQAAABY" />
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="efef8-109">注释</span><span class="sxs-lookup"><span data-stu-id="efef8-109">Comments</span></span>

<span data-ttu-id="efef8-110">从 Exchange 存储中获取项的请求所需的所有项类型的同一窗体。</span><span class="sxs-lookup"><span data-stu-id="efef8-110">The request to get an item from the Exchange store takes the same form for all item types.</span></span> <span data-ttu-id="efef8-111">将不同的不同项目请求的响应，因为其他项返回基于响应形状上的其他信息。</span><span class="sxs-lookup"><span data-stu-id="efef8-111">The responses to requests for different items will be different because different items return different information based on the response shapes.</span></span>
  
> [!NOTE]
> <span data-ttu-id="efef8-112">已缩短的项标识符，若要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="efef8-112">The item identifier has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="efef8-113">请求元素</span><span class="sxs-lookup"><span data-stu-id="efef8-113">Request elements</span></span>

<span data-ttu-id="efef8-114">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="efef8-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="efef8-115">GetItem</span><span class="sxs-lookup"><span data-stu-id="efef8-115">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="efef8-116">ItemShape</span><span class="sxs-lookup"><span data-stu-id="efef8-116">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="efef8-117">BaseShape</span><span class="sxs-lookup"><span data-stu-id="efef8-117">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="efef8-118">ItemIds</span><span class="sxs-lookup"><span data-stu-id="efef8-118">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="efef8-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="efef8-119">ItemId</span></span>](itemid.md)
    
## <a name="successful-getitem-contact-response"></a><span data-ttu-id="efef8-120">成功 GetItem （联系人） 响应</span><span class="sxs-lookup"><span data-stu-id="efef8-120">Successful GetItem (Contact) Response</span></span>

### <a name="description"></a><span data-ttu-id="efef8-121">说明</span><span class="sxs-lookup"><span data-stu-id="efef8-121">Description</span></span>

<span data-ttu-id="efef8-122">下面的代码示例显示**AllProperties**[BaseShape](baseshape.md)成功的 GetItem 响应。</span><span class="sxs-lookup"><span data-stu-id="efef8-122">The following code example shows a successful GetItem response for the **AllProperties**[BaseShape](baseshape.md).</span></span>
  
### <a name="code"></a><span data-ttu-id="efef8-123">代码</span><span class="sxs-lookup"><span data-stu-id="efef8-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAtAEA=" ChangeKey="EQAAABYq" />
              <t:ParentFolderId Id="AQAtAEFk==" ChangeKey="AQAAAA==" />
              <t:ItemClass>IPM.Contact</t:ItemClass>
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="Text" />
              <t:DateTimeReceived>2006-08-18T17:31:18Z</t:DateTimeReceived>
              <t:Size>382</t:Size>
              <t:Importance>Normal</t:Importance>
              <t:IsSubmitted>false</t:IsSubmitted>
              <t:IsDraft>true</t:IsDraft>
              <t:IsFromMe>false</t:IsFromMe>
              <t:IsResend>false</t:IsResend>
              <t:IsUnmodified>false</t:IsUnmodified>
              <t:DateTimeSent>2006-08-18T17:31:18Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-08-18T17:31:18Z</t:DateTimeCreated>
              <t:HasAttachments>false</t:HasAttachments>
              <t:Culture>en</t:Culture>
              <t:FileAs>SampleContact</t:FileAs>
              <t:FileAsMapping>None</t:FileAsMapping>
              <t:DisplayName>Tanja Plate</t:DisplayName>
              <t:GivenName>Tanja</t:GivenName>
              <t:Initials>T.P.</t:Initials>
              <t:CompleteName>
                <t:FirstName>Tanja</t:FirstName>
                <t:LastName>Plate</t:LastName>
                <t:Initials>T.P.</t:Initials>
                <t:FullName>Tanja Plate</t:FullName>
              </t:CompleteName>
              <t:CompanyName>Northwind Traders</t:CompanyName>
              <t:EmailAddresses>
                <t:Entry Key="EmailAddress1">tplate@example.com</t:Entry>
                <t:Entry Key="EmailAddress2">tplate@example.com</t:Entry>
              </t:EmailAddresses>
              <t:PhysicalAddresses>
                <t:Entry Key="Business">
                  <t:Street>12345 67th Ave</t:Street>
                  <t:City>Whittier</t:City>
                  <t:State>CA</t:State>
                  <t:Country>USA</t:Country>
                </t:Entry>
              </t:PhysicalAddresses>
              <t:PhoneNumbers>
                <t:Entry Key="BusinessPhone">5625550199</t:Entry>
              </t:PhoneNumbers>
              <t:JobTitle>Project Manager</t:JobTitle>
              <t:Surname>Plate</t:Surname>
            </t:Contact>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="efef8-124">注释</span><span class="sxs-lookup"><span data-stu-id="efef8-124">Comments</span></span>

<span data-ttu-id="efef8-125">已缩短的项标识符，若要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="efef8-125">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="efef8-126">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="efef8-126">Successful response elements</span></span>

<span data-ttu-id="efef8-127">下列元素用于在响应中与联系人项目的**AllProperties**响应形状 GetItem 请求。</span><span class="sxs-lookup"><span data-stu-id="efef8-127">The following elements are used in the response for a GetItem request with a response shape of **AllProperties** for a contact item.</span></span> 
  
- [<span data-ttu-id="efef8-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="efef8-128">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="efef8-129">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="efef8-129">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="efef8-130">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="efef8-130">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="efef8-131">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="efef8-131">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="efef8-132">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="efef8-132">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="efef8-133">Items</span><span class="sxs-lookup"><span data-stu-id="efef8-133">Items</span></span>](items.md)
    
- [<span data-ttu-id="efef8-134">Contact</span><span class="sxs-lookup"><span data-stu-id="efef8-134">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="efef8-135">ItemId</span><span class="sxs-lookup"><span data-stu-id="efef8-135">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="efef8-136">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="efef8-136">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="efef8-137">ItemClass</span><span class="sxs-lookup"><span data-stu-id="efef8-137">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="efef8-138">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="efef8-138">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="efef8-139">Body</span><span class="sxs-lookup"><span data-stu-id="efef8-139">Body</span></span>](body.md)
    
- [<span data-ttu-id="efef8-140">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="efef8-140">DateTimeReceived</span></span>](datetimereceived.md)
    
- [<span data-ttu-id="efef8-141">Size</span><span class="sxs-lookup"><span data-stu-id="efef8-141">Size</span></span>](size.md)
    
- [<span data-ttu-id="efef8-142">Importance</span><span class="sxs-lookup"><span data-stu-id="efef8-142">Importance</span></span>](importance.md)
    
- [<span data-ttu-id="efef8-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="efef8-143">IsSubmitted</span></span>](issubmitted.md)
    
- [<span data-ttu-id="efef8-144">IsDraft</span><span class="sxs-lookup"><span data-stu-id="efef8-144">IsDraft</span></span>](isdraft.md)
    
- [<span data-ttu-id="efef8-145">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="efef8-145">IsFromMe</span></span>](isfromme.md)
    
- [<span data-ttu-id="efef8-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="efef8-146">IsResend</span></span>](isresend.md)
    
- [<span data-ttu-id="efef8-147">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="efef8-147">IsUnmodified</span></span>](isunmodified.md)
    
- [<span data-ttu-id="efef8-148">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="efef8-148">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="efef8-149">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="efef8-149">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="efef8-150">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="efef8-150">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="efef8-151">区域性</span><span class="sxs-lookup"><span data-stu-id="efef8-151">Culture</span></span>](culture.md)
    
- [<span data-ttu-id="efef8-152">FileAs</span><span class="sxs-lookup"><span data-stu-id="efef8-152">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="efef8-153">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="efef8-153">FileAsMapping</span></span>](fileasmapping.md)
    
- [<span data-ttu-id="efef8-154">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="efef8-154">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="efef8-155">GivenName</span><span class="sxs-lookup"><span data-stu-id="efef8-155">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="efef8-156">首字母缩写</span><span class="sxs-lookup"><span data-stu-id="efef8-156">Initials</span></span>](initials.md)
    
- [<span data-ttu-id="efef8-157">CompleteName</span><span class="sxs-lookup"><span data-stu-id="efef8-157">CompleteName</span></span>](completename.md)
    
- [<span data-ttu-id="efef8-158">FirstName</span><span class="sxs-lookup"><span data-stu-id="efef8-158">FirstName</span></span>](firstname.md)
    
- [<span data-ttu-id="efef8-159">姓氏</span><span class="sxs-lookup"><span data-stu-id="efef8-159">LastName</span></span>](lastname.md)
    
- [<span data-ttu-id="efef8-160">FullName</span><span class="sxs-lookup"><span data-stu-id="efef8-160">FullName</span></span>](fullname.md)
    
- [<span data-ttu-id="efef8-161">公司名称</span><span class="sxs-lookup"><span data-stu-id="efef8-161">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="efef8-162">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="efef8-162">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="efef8-163">条目 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="efef8-163">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="efef8-164">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="efef8-164">PhysicalAddresses</span></span>](physicaladdresses.md)
    
- [<span data-ttu-id="efef8-165">条目 (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="efef8-165">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md)
    
- [<span data-ttu-id="efef8-166">街道</span><span class="sxs-lookup"><span data-stu-id="efef8-166">Street</span></span>](street.md)
    
- [<span data-ttu-id="efef8-167">市/县</span><span class="sxs-lookup"><span data-stu-id="efef8-167">City</span></span>](city.md)
    
- [<span data-ttu-id="efef8-168">State</span><span class="sxs-lookup"><span data-stu-id="efef8-168">State</span></span>](state-ex15websvcsotherref.md)
    
- [<span data-ttu-id="efef8-169">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="efef8-169">CountryOrRegion</span></span>](countryorregion.md)
    
- [<span data-ttu-id="efef8-170">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="efef8-170">PhoneNumbers</span></span>](phonenumbers.md)
    
- [<span data-ttu-id="efef8-171">条目 (PhoneNumber)</span><span class="sxs-lookup"><span data-stu-id="efef8-171">Entry (PhoneNumber)</span></span>](entry-phonenumber.md)
    
- [<span data-ttu-id="efef8-172">JobTitle</span><span class="sxs-lookup"><span data-stu-id="efef8-172">JobTitle</span></span>](jobtitle.md)
    
- [<span data-ttu-id="efef8-173">姓</span><span class="sxs-lookup"><span data-stu-id="efef8-173">Surname</span></span>](surname.md)
    
## <a name="invalid-getitem-contact-request-example"></a><span data-ttu-id="efef8-174">无效的 GetItem （联系人） 请求示例</span><span class="sxs-lookup"><span data-stu-id="efef8-174">Invalid GetItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="efef8-175">说明</span><span class="sxs-lookup"><span data-stu-id="efef8-175">Description</span></span>

<span data-ttu-id="efef8-176">下面的代码示例显示了无效的请求。</span><span class="sxs-lookup"><span data-stu-id="efef8-176">The following code example shows an invalid request.</span></span>
  
### <a name="code"></a><span data-ttu-id="efef8-177">代码</span><span class="sxs-lookup"><span data-stu-id="efef8-177">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='http://schemas.microsoft.com/exchange/services/2006/messages'>
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="EQAAABq" />
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="efef8-178">注释</span><span class="sxs-lookup"><span data-stu-id="efef8-178">Comments</span></span>

<span data-ttu-id="efef8-179">项标识符具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="efef8-179">Item identifiers have been shortened to preserve readability.</span></span>
  
## <a name="getitem-contact-error-response"></a><span data-ttu-id="efef8-180">GetItem （联系人） 错误响应</span><span class="sxs-lookup"><span data-stu-id="efef8-180">GetItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="efef8-181">说明</span><span class="sxs-lookup"><span data-stu-id="efef8-181">Description</span></span>

<span data-ttu-id="efef8-182">下面的代码示例显示错误响应 GetItem （联系人） 的请求。</span><span class="sxs-lookup"><span data-stu-id="efef8-182">The following code example shows an error response to a GetItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="efef8-183">代码</span><span class="sxs-lookup"><span data-stu-id="efef8-183">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Error">
          <m:MessageText>Mime conversion is not supported for this item type.</m:MessageText>
          <m:ResponseCode>ErrorUnsupportedMimeConversion</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="efef8-184">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="efef8-184">Error response elements</span></span>

<span data-ttu-id="efef8-185">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="efef8-185">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="efef8-186">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="efef8-186">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="efef8-187">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="efef8-187">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="efef8-188">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="efef8-188">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="efef8-189">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="efef8-189">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="efef8-190">MessageText</span><span class="sxs-lookup"><span data-stu-id="efef8-190">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="efef8-191">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="efef8-191">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="efef8-192">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="efef8-192">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="efef8-193">Items</span><span class="sxs-lookup"><span data-stu-id="efef8-193">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="efef8-194">另请参阅</span><span class="sxs-lookup"><span data-stu-id="efef8-194">See also</span></span>



[<span data-ttu-id="efef8-195">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="efef8-195">GetItem operation</span></span>](getitem-operation.md)


- [<span data-ttu-id="efef8-196">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="efef8-196">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

