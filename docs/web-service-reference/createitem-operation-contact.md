---
title: CreateItem operation，（联系人）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 417e994b-0a17-4c24-9527-04796b80b029
description: CreateItem operation，用于在 Exchange 存储中创建的联系人。
ms.openlocfilehash: 05e4715f3c6675401ae7afac852395f7459c02c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753660"
---
# <a name="createitem-operation-contact"></a><span data-ttu-id="8476c-103">CreateItem operation，（联系人）</span><span class="sxs-lookup"><span data-stu-id="8476c-103">CreateItem operation (contact)</span></span>

<span data-ttu-id="8476c-104">CreateItem operation，用于在 Exchange 存储中创建的联系人。</span><span class="sxs-lookup"><span data-stu-id="8476c-104">The CreateItem operation is used to create contacts in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8476c-105">注解</span><span class="sxs-lookup"><span data-stu-id="8476c-105">Remarks</span></span>

<span data-ttu-id="8476c-106">不支持私有通讯组列表的创建。</span><span class="sxs-lookup"><span data-stu-id="8476c-106">The creation of private distribution lists is not supported.</span></span> <span data-ttu-id="8476c-107">[CompleteName](completename.md)容器内的所有属性都是只读的因此无法在联系人项目上设置。</span><span class="sxs-lookup"><span data-stu-id="8476c-107">All properties within the [CompleteName](completename.md) container are read-only and cannot be set on a contact item.</span></span> 
  
## <a name="createitem-request-example"></a><span data-ttu-id="8476c-108">CreateItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="8476c-108">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="8476c-109">说明</span><span class="sxs-lookup"><span data-stu-id="8476c-109">Description</span></span>

<span data-ttu-id="8476c-110">一个有效的 CreateItem SOAP 请求的下面的示例演示如何在默认联系人文件夹中创建一个联系人。</span><span class="sxs-lookup"><span data-stu-id="8476c-110">The following example of a valid CreateItem SOAP request shows how to create a contact in the default Contacts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="8476c-111">代码</span><span class="sxs-lookup"><span data-stu-id="8476c-111">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" >
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="contacts"/>
      </SavedItemFolderId>
      <Items>
        <t:Contact>
          <t:FileAs>SampleContact</t:FileAs>
          <t:GivenName>Tanja</t:GivenName>
          <t:CompanyName>Blue Yonder Airlines</t:CompanyName>
          <t:EmailAddresses>
            <t:Entry Key="EmailAddress1">tplate@example.com</t:Entry>
          </t:EmailAddresses>
          <t:PhysicalAddresses>
            <t:Entry Key="Business">
              <t:Street>1234 56th Ave</t:Street>
              <t:City>La Habra</t:City>
              <t:State>CA</t:State>
              <t: CountryOrRegion>USA</t: CountryOrRegion>
            </t:Entry>
          </t:PhysicalAddresses>
          <t:PhoneNumbers>
            <t:Entry Key="BusinessPhone">4255550199</t:Entry>
          </t:PhoneNumbers>
          <t:JobTitle>Manager</t:JobTitle>
          <t:Surname>Plate</t:Surname>
        </t:Contact>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="8476c-112">请求元素</span><span class="sxs-lookup"><span data-stu-id="8476c-112">Request elements</span></span>

<span data-ttu-id="8476c-113">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="8476c-113">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="8476c-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="8476c-114">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="8476c-115">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="8476c-115">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="8476c-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="8476c-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="8476c-117">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="8476c-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="8476c-118">Contact</span><span class="sxs-lookup"><span data-stu-id="8476c-118">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="8476c-119">FileAs</span><span class="sxs-lookup"><span data-stu-id="8476c-119">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="8476c-120">GivenName</span><span class="sxs-lookup"><span data-stu-id="8476c-120">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="8476c-121">公司名称</span><span class="sxs-lookup"><span data-stu-id="8476c-121">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="8476c-122">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="8476c-122">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="8476c-123">条目 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="8476c-123">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="8476c-124">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="8476c-124">PhysicalAddresses</span></span>](physicaladdresses.md)
    
- [<span data-ttu-id="8476c-125">条目 (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="8476c-125">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md)
    
- [<span data-ttu-id="8476c-126">街道</span><span class="sxs-lookup"><span data-stu-id="8476c-126">Street</span></span>](street.md)
    
- [<span data-ttu-id="8476c-127">市/县</span><span class="sxs-lookup"><span data-stu-id="8476c-127">City</span></span>](city.md)
    
- [<span data-ttu-id="8476c-128">State</span><span class="sxs-lookup"><span data-stu-id="8476c-128">State</span></span>](state-ex15websvcsotherref.md)
    
- [<span data-ttu-id="8476c-129">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="8476c-129">CountryOrRegion</span></span>](countryorregion.md)
    
- [<span data-ttu-id="8476c-130">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="8476c-130">PhoneNumbers</span></span>](phonenumbers.md)
    
- [<span data-ttu-id="8476c-131">条目 (PhoneNumber)</span><span class="sxs-lookup"><span data-stu-id="8476c-131">Entry (PhoneNumber)</span></span>](entry-phonenumber.md)
    
- [<span data-ttu-id="8476c-132">JobTitle</span><span class="sxs-lookup"><span data-stu-id="8476c-132">JobTitle</span></span>](jobtitle.md)
    
- [<span data-ttu-id="8476c-133">姓</span><span class="sxs-lookup"><span data-stu-id="8476c-133">Surname</span></span>](surname.md)
    
## <a name="successful-createitem-request"></a><span data-ttu-id="8476c-134">成功 CreateItem 请求</span><span class="sxs-lookup"><span data-stu-id="8476c-134">Successful CreateItem Request</span></span>

### <a name="description"></a><span data-ttu-id="8476c-135">说明</span><span class="sxs-lookup"><span data-stu-id="8476c-135">Description</span></span>

<span data-ttu-id="8476c-136">下面的示例演示创建联系人 CreateItem 请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="8476c-136">The following example shows a successful response to the CreateItem request that created a contact.</span></span> <span data-ttu-id="8476c-137">本示例中，则响应中包含新创建的项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="8476c-137">In this example, the response contains the identifier of the newly created item.</span></span>
  
### <a name="code"></a><span data-ttu-id="8476c-138">代码</span><span class="sxs-lookup"><span data-stu-id="8476c-138">Code</span></span>

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
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAtA=" ChangeKey="EQAAAB" />
            </t:Contact>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="8476c-139">注释</span><span class="sxs-lookup"><span data-stu-id="8476c-139">Comments</span></span>

<span data-ttu-id="8476c-140">已缩短的项标识符，若要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="8476c-140">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="8476c-141">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="8476c-141">Successful response elements</span></span>

<span data-ttu-id="8476c-142">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="8476c-142">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="8476c-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8476c-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8476c-144">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="8476c-144">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="8476c-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8476c-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8476c-146">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8476c-146">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="8476c-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8476c-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8476c-148">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="8476c-148">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="8476c-149">Contact</span><span class="sxs-lookup"><span data-stu-id="8476c-149">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="8476c-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="8476c-150">ItemId</span></span>](itemid.md)
    
## <a name="invalid-createitem-request-example"></a><span data-ttu-id="8476c-151">无效的 CreateItem 请求示例</span><span class="sxs-lookup"><span data-stu-id="8476c-151">Invalid CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="8476c-152">说明</span><span class="sxs-lookup"><span data-stu-id="8476c-152">Description</span></span>

<span data-ttu-id="8476c-153">下面的示例演示请求包含有效的 XML，但不兼容的说明。</span><span class="sxs-lookup"><span data-stu-id="8476c-153">The following example shows a request that contains valid XML but incompatible instructions.</span></span> <span data-ttu-id="8476c-154">搜索文件夹中无法创建联系人。</span><span class="sxs-lookup"><span data-stu-id="8476c-154">A contact cannot be created in a search folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="8476c-155">代码</span><span class="sxs-lookup"><span data-stu-id="8476c-155">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns='http://schemas.microsoft.com/exchange/services/2006/messages'>
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id='searchfolders'/>
      </SavedItemFolderId>
      <Items>
        <t:Contact>
          <t:ItemClass>IPM.Contact</t:ItemClass>
        </t:Contact>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="createitem-contact-error-response"></a><span data-ttu-id="8476c-156">CreateItem （联系人） 错误响应</span><span class="sxs-lookup"><span data-stu-id="8476c-156">CreateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="8476c-157">说明</span><span class="sxs-lookup"><span data-stu-id="8476c-157">Description</span></span>

<span data-ttu-id="8476c-158">下面的示例演示对 CreateItem （联系人） 请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="8476c-158">The following example shows an error response to a CreateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="8476c-159">代码</span><span class="sxs-lookup"><span data-stu-id="8476c-159">Code</span></span>

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
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>Cannot create a contact in a non-contact Folder.</m:MessageText>
          <m:ResponseCode>ErrorCannotCreateContactInNonContactFolder</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="8476c-160">错误响应元素</span><span class="sxs-lookup"><span data-stu-id="8476c-160">Error response elements</span></span>

<span data-ttu-id="8476c-161">错误响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="8476c-161">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="8476c-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8476c-162">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="8476c-163">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="8476c-163">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="8476c-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8476c-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="8476c-165">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8476c-165">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="8476c-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="8476c-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="8476c-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="8476c-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="8476c-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="8476c-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="8476c-169">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="8476c-169">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
## <a name="see-also"></a><span data-ttu-id="8476c-170">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8476c-170">See also</span></span>



[<span data-ttu-id="8476c-171">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="8476c-171">CreateItem operation</span></span>](createitem-operation.md)

