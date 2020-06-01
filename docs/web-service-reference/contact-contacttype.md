---
title: Contact （ContactType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: Contact 元素指定统一联系人存储库中的联系人。
ms.openlocfilehash: e8ebc28456f8bfc26f5d790ac9ff278930041ea0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461518"
---
# <a name="contact-contacttype"></a><span data-ttu-id="77c5b-103">Contact （ContactType）</span><span class="sxs-lookup"><span data-stu-id="77c5b-103">Contact (ContactType)</span></span>

<span data-ttu-id="77c5b-104">**Contact**元素指定统一联系人存储库中的联系人。</span><span class="sxs-lookup"><span data-stu-id="77c5b-104">The **Contact** element specifies a contact in the Unified Contact Store.</span></span> 
  
```XML
<Contact>
    <PersonName></PersonName>
    <BusinessName></BusinessName>
    <PhoneNumbers></PhoneNumbers>
    <Urls></Urls>
    <EmailAddresses></EmailAddresses>
    <Addresses></Addesses>    <ContactString></ContactString
</Contact>
```

 <span data-ttu-id="77c5b-105">**ContactType**</span><span class="sxs-lookup"><span data-stu-id="77c5b-105">**ContactType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77c5b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="77c5b-106">Attributes and elements</span></span>

<span data-ttu-id="77c5b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="77c5b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77c5b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="77c5b-108">Attributes</span></span>

<span data-ttu-id="77c5b-109">无。</span><span class="sxs-lookup"><span data-stu-id="77c5b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77c5b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="77c5b-110">Child elements</span></span>

|<span data-ttu-id="77c5b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="77c5b-111">**Element**</span></span>|<span data-ttu-id="77c5b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="77c5b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77c5b-113">Contact.personname</span><span class="sxs-lookup"><span data-stu-id="77c5b-113">PersonName</span></span>](personname.md) <br/> |<span data-ttu-id="77c5b-114">指定个人的名称。</span><span class="sxs-lookup"><span data-stu-id="77c5b-114">Specifies the name of an individual.</span></span>  <br/> |
|[<span data-ttu-id="77c5b-115">BusinessName</span><span class="sxs-lookup"><span data-stu-id="77c5b-115">BusinessName</span></span>](businessname.md) <br/> |<span data-ttu-id="77c5b-116">指定企业的名称。</span><span class="sxs-lookup"><span data-stu-id="77c5b-116">Specifies the name of a business.</span></span>  <br/> |
|[<span data-ttu-id="77c5b-117">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="77c5b-117">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="77c5b-118">表示联系人的电话号码的集合。</span><span class="sxs-lookup"><span data-stu-id="77c5b-118">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="77c5b-119">Urls</span><span class="sxs-lookup"><span data-stu-id="77c5b-119">Urls</span></span>](urls.md) <br/> |<span data-ttu-id="77c5b-120">指定角色的 Url 数组。</span><span class="sxs-lookup"><span data-stu-id="77c5b-120">Specifies an array of URLs for a persona.</span></span>  <br/> |
|[<span data-ttu-id="77c5b-121">EmailAddresses （ArrayOfExtractedEmailAddresses）</span><span class="sxs-lookup"><span data-stu-id="77c5b-121">EmailAddresses (ArrayOfExtractedEmailAddresses)</span></span>](emailaddresses-arrayofextractedemailaddresses.md) <br/> |<span data-ttu-id="77c5b-122">指定已提取的电子邮件地址数组。</span><span class="sxs-lookup"><span data-stu-id="77c5b-122">Specifies an array of extracted email addresses.</span></span>  <br/> |
|[<span data-ttu-id="77c5b-123">地址（ArrayOfAddressesType）</span><span class="sxs-lookup"><span data-stu-id="77c5b-123">Addresses (ArrayOfAddressesType)</span></span>](addresses-arrayofaddressestype.md) <br/> |<span data-ttu-id="77c5b-124">指定**Address**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="77c5b-124">Specifies an array of **Address** elements.</span></span>  <br/> |
|[<span data-ttu-id="77c5b-125">ContactString</span><span class="sxs-lookup"><span data-stu-id="77c5b-125">ContactString</span></span>](contactstring.md) <br/> |<span data-ttu-id="77c5b-126">指定联系人的显示名称。</span><span class="sxs-lookup"><span data-stu-id="77c5b-126">Specifies the display name of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="77c5b-127">父元素</span><span class="sxs-lookup"><span data-stu-id="77c5b-127">Parent elements</span></span>

|<span data-ttu-id="77c5b-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="77c5b-128">**Element**</span></span>|<span data-ttu-id="77c5b-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="77c5b-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77c5b-130">联系人（ArrayOfContactsType）</span><span class="sxs-lookup"><span data-stu-id="77c5b-130">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="77c5b-131">指定联系人数组。</span><span class="sxs-lookup"><span data-stu-id="77c5b-131">Specifies an array of contacts.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77c5b-132">备注</span><span class="sxs-lookup"><span data-stu-id="77c5b-132">Remarks</span></span>

<span data-ttu-id="77c5b-133">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="77c5b-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="77c5b-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="77c5b-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77c5b-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="77c5b-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77c5b-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="77c5b-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="77c5b-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="77c5b-137">Schema Name</span></span>  <br/> |<span data-ttu-id="77c5b-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="77c5b-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="77c5b-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="77c5b-139">Validation File</span></span>  <br/> |<span data-ttu-id="77c5b-140">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="77c5b-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="77c5b-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="77c5b-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="77c5b-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77c5b-142">See also</span></span>



- [<span data-ttu-id="77c5b-143">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="77c5b-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

