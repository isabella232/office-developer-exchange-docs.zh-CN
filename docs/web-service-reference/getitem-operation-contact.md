---
title: GetItem 操作（联系人）
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
description: GetItem 操作用于从 Exchange 存储中获取联系人项目。
ms.openlocfilehash: 93e8dbe28e130ab64d4b8d12d2befde1f77ae8fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460020"
---
# <a name="getitem-operation-contact"></a><span data-ttu-id="95c77-103">GetItem 操作（联系人）</span><span class="sxs-lookup"><span data-stu-id="95c77-103">GetItem operation (contact)</span></span>

<span data-ttu-id="95c77-104">GetItem 操作用于从 Exchange 存储中获取联系人项目。</span><span class="sxs-lookup"><span data-stu-id="95c77-104">The GetItem operation is used to get contact items from the Exchange store.</span></span>
  
## <a name="getitem-contact-request-example"></a><span data-ttu-id="95c77-105">GetItem （Contact）请求示例</span><span class="sxs-lookup"><span data-stu-id="95c77-105">GetItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="95c77-106">Description</span><span class="sxs-lookup"><span data-stu-id="95c77-106">Description</span></span>

<span data-ttu-id="95c77-107">下面的示例演示如何从 Exchange 存储中获取项目。</span><span class="sxs-lookup"><span data-stu-id="95c77-107">The following example shows how to get an item from the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="95c77-108">代码</span><span class="sxs-lookup"><span data-stu-id="95c77-108">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
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

### <a name="comments"></a><span data-ttu-id="95c77-109">备注</span><span class="sxs-lookup"><span data-stu-id="95c77-109">Comments</span></span>

<span data-ttu-id="95c77-110">从 Exchange 存储区获取项目的请求将为所有项目类型采用相同的表单。</span><span class="sxs-lookup"><span data-stu-id="95c77-110">The request to get an item from the Exchange store takes the same form for all item types.</span></span> <span data-ttu-id="95c77-111">对不同项目的请求的响应将有所不同，因为不同的项目会返回基于响应形状的不同信息。</span><span class="sxs-lookup"><span data-stu-id="95c77-111">The responses to requests for different items will be different because different items return different information based on the response shapes.</span></span>
  
> [!NOTE]
> <span data-ttu-id="95c77-112">项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="95c77-112">The item identifier has been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="95c77-113">Request 元素</span><span class="sxs-lookup"><span data-stu-id="95c77-113">Request elements</span></span>

<span data-ttu-id="95c77-114">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="95c77-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="95c77-115">GetItem</span><span class="sxs-lookup"><span data-stu-id="95c77-115">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="95c77-116">ItemShape</span><span class="sxs-lookup"><span data-stu-id="95c77-116">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="95c77-117">BaseShape</span><span class="sxs-lookup"><span data-stu-id="95c77-117">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="95c77-118">ItemIds</span><span class="sxs-lookup"><span data-stu-id="95c77-118">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="95c77-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="95c77-119">ItemId</span></span>](itemid.md)
    
## <a name="successful-getitem-contact-response"></a><span data-ttu-id="95c77-120">成功的 GetItem （联系人）响应</span><span class="sxs-lookup"><span data-stu-id="95c77-120">Successful GetItem (Contact) Response</span></span>

### <a name="description"></a><span data-ttu-id="95c77-121">Description</span><span class="sxs-lookup"><span data-stu-id="95c77-121">Description</span></span>

<span data-ttu-id="95c77-122">下面的代码示例演示了对**AllProperties**[BaseShape](baseshape.md)的成功的 GetItem 响应。</span><span class="sxs-lookup"><span data-stu-id="95c77-122">The following code example shows a successful GetItem response for the **AllProperties**[BaseShape](baseshape.md).</span></span>
  
### <a name="code"></a><span data-ttu-id="95c77-123">代码</span><span class="sxs-lookup"><span data-stu-id="95c77-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="95c77-124">备注</span><span class="sxs-lookup"><span data-stu-id="95c77-124">Comments</span></span>

<span data-ttu-id="95c77-125">项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="95c77-125">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="95c77-126">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="95c77-126">Successful response elements</span></span>

<span data-ttu-id="95c77-127">以下元素用于响应 GetItem 请求，其中包含联系人项目的**AllProperties**的响应形状。</span><span class="sxs-lookup"><span data-stu-id="95c77-127">The following elements are used in the response for a GetItem request with a response shape of **AllProperties** for a contact item.</span></span> 
  
- [<span data-ttu-id="95c77-128">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="95c77-128">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="95c77-129">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="95c77-129">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="95c77-130">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="95c77-130">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="95c77-131">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="95c77-131">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="95c77-132">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="95c77-132">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="95c77-133">Items</span><span class="sxs-lookup"><span data-stu-id="95c77-133">Items</span></span>](items.md)
    
- [<span data-ttu-id="95c77-134">联系人</span><span class="sxs-lookup"><span data-stu-id="95c77-134">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="95c77-135">ItemId</span><span class="sxs-lookup"><span data-stu-id="95c77-135">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="95c77-136">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="95c77-136">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="95c77-137">ItemClass</span><span class="sxs-lookup"><span data-stu-id="95c77-137">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="95c77-138">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="95c77-138">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="95c77-139">Body</span><span class="sxs-lookup"><span data-stu-id="95c77-139">Body</span></span>](body.md)
    
- [<span data-ttu-id="95c77-140">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="95c77-140">DateTimeReceived</span></span>](datetimereceived.md)
    
- [<span data-ttu-id="95c77-141">大小</span><span class="sxs-lookup"><span data-stu-id="95c77-141">Size</span></span>](size.md)
    
- [<span data-ttu-id="95c77-142">Importance</span><span class="sxs-lookup"><span data-stu-id="95c77-142">Importance</span></span>](importance.md)
    
- [<span data-ttu-id="95c77-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="95c77-143">IsSubmitted</span></span>](issubmitted.md)
    
- [<span data-ttu-id="95c77-144">IsDraft</span><span class="sxs-lookup"><span data-stu-id="95c77-144">IsDraft</span></span>](isdraft.md)
    
- [<span data-ttu-id="95c77-145">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="95c77-145">IsFromMe</span></span>](isfromme.md)
    
- [<span data-ttu-id="95c77-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="95c77-146">IsResend</span></span>](isresend.md)
    
- [<span data-ttu-id="95c77-147">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="95c77-147">IsUnmodified</span></span>](isunmodified.md)
    
- [<span data-ttu-id="95c77-148">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="95c77-148">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="95c77-149">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="95c77-149">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="95c77-150">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="95c77-150">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="95c77-151">Culture</span><span class="sxs-lookup"><span data-stu-id="95c77-151">Culture</span></span>](culture.md)
    
- [<span data-ttu-id="95c77-152">FileAs</span><span class="sxs-lookup"><span data-stu-id="95c77-152">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="95c77-153">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="95c77-153">FileAsMapping</span></span>](fileasmapping.md)
    
- [<span data-ttu-id="95c77-154">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="95c77-154">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="95c77-155">GivenName</span><span class="sxs-lookup"><span data-stu-id="95c77-155">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="95c77-156">缩写</span><span class="sxs-lookup"><span data-stu-id="95c77-156">Initials</span></span>](initials.md)
    
- [<span data-ttu-id="95c77-157">CompleteName</span><span class="sxs-lookup"><span data-stu-id="95c77-157">CompleteName</span></span>](completename.md)
    
- [<span data-ttu-id="95c77-158">FirstName</span><span class="sxs-lookup"><span data-stu-id="95c77-158">FirstName</span></span>](firstname.md)
    
- [<span data-ttu-id="95c77-159">LastName</span><span class="sxs-lookup"><span data-stu-id="95c77-159">LastName</span></span>](lastname.md)
    
- [<span data-ttu-id="95c77-160">FullName</span><span class="sxs-lookup"><span data-stu-id="95c77-160">FullName</span></span>](fullname.md)
    
- [<span data-ttu-id="95c77-161">CompanyName</span><span class="sxs-lookup"><span data-stu-id="95c77-161">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="95c77-162">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="95c77-162">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="95c77-163">条目（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="95c77-163">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="95c77-164">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="95c77-164">PhysicalAddresses</span></span>](physicaladdresses.md)
    
- [<span data-ttu-id="95c77-165">条目（PhysicalAddress）</span><span class="sxs-lookup"><span data-stu-id="95c77-165">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md)
    
- [<span data-ttu-id="95c77-166">地址</span><span class="sxs-lookup"><span data-stu-id="95c77-166">Street</span></span>](street.md)
    
- [<span data-ttu-id="95c77-167">市/县</span><span class="sxs-lookup"><span data-stu-id="95c77-167">City</span></span>](city.md)
    
- [<span data-ttu-id="95c77-168">State</span><span class="sxs-lookup"><span data-stu-id="95c77-168">State</span></span>](state-ex15websvcsotherref.md)
    
- [<span data-ttu-id="95c77-169">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="95c77-169">CountryOrRegion</span></span>](countryorregion.md)
    
- [<span data-ttu-id="95c77-170">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="95c77-170">PhoneNumbers</span></span>](phonenumbers.md)
    
- [<span data-ttu-id="95c77-171">条目（PhoneNumber）</span><span class="sxs-lookup"><span data-stu-id="95c77-171">Entry (PhoneNumber)</span></span>](entry-phonenumber.md)
    
- [<span data-ttu-id="95c77-172">JobTitle</span><span class="sxs-lookup"><span data-stu-id="95c77-172">JobTitle</span></span>](jobtitle.md)
    
- [<span data-ttu-id="95c77-173">姓氏</span><span class="sxs-lookup"><span data-stu-id="95c77-173">Surname</span></span>](surname.md)
    
## <a name="invalid-getitem-contact-request-example"></a><span data-ttu-id="95c77-174">无效的 GetItem （Contact）请求示例</span><span class="sxs-lookup"><span data-stu-id="95c77-174">Invalid GetItem (Contact) request example</span></span>

### <a name="description"></a><span data-ttu-id="95c77-175">Description</span><span class="sxs-lookup"><span data-stu-id="95c77-175">Description</span></span>

<span data-ttu-id="95c77-176">下面的代码示例演示一个无效请求。</span><span class="sxs-lookup"><span data-stu-id="95c77-176">The following code example shows an invalid request.</span></span>
  
### <a name="code"></a><span data-ttu-id="95c77-177">代码</span><span class="sxs-lookup"><span data-stu-id="95c77-177">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
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

### <a name="comments"></a><span data-ttu-id="95c77-178">备注</span><span class="sxs-lookup"><span data-stu-id="95c77-178">Comments</span></span>

<span data-ttu-id="95c77-179">项目标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="95c77-179">Item identifiers have been shortened to preserve readability.</span></span>
  
## <a name="getitem-contact-error-response"></a><span data-ttu-id="95c77-180">GetItem （联系人）错误响应</span><span class="sxs-lookup"><span data-stu-id="95c77-180">GetItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="95c77-181">Description</span><span class="sxs-lookup"><span data-stu-id="95c77-181">Description</span></span>

<span data-ttu-id="95c77-182">下面的代码示例演示对 GetItem （联系人）请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="95c77-182">The following code example shows an error response to a GetItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="95c77-183">代码</span><span class="sxs-lookup"><span data-stu-id="95c77-183">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="95c77-184">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="95c77-184">Error response elements</span></span>

<span data-ttu-id="95c77-185">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="95c77-185">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="95c77-186">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="95c77-186">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="95c77-187">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="95c77-187">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="95c77-188">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="95c77-188">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="95c77-189">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="95c77-189">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="95c77-190">MessageText</span><span class="sxs-lookup"><span data-stu-id="95c77-190">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="95c77-191">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="95c77-191">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="95c77-192">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="95c77-192">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="95c77-193">Items</span><span class="sxs-lookup"><span data-stu-id="95c77-193">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="95c77-194">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95c77-194">See also</span></span>



[<span data-ttu-id="95c77-195">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="95c77-195">GetItem operation</span></span>](getitem-operation.md)


- [<span data-ttu-id="95c77-196">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="95c77-196">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

