---
title: 联系人 (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: 联系人元素指定在统一联系人存储库中的联系人。
ms.openlocfilehash: f1593da78a46851c7db43abc567eb66c0c74e0f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753494"
---
# <a name="contact-contacttype"></a><span data-ttu-id="0b39f-103">联系人 (ContactType)</span><span class="sxs-lookup"><span data-stu-id="0b39f-103">Contact (ContactType)</span></span>

<span data-ttu-id="0b39f-104">**联系人**元素指定统一联系人存储库中的联系人。</span><span class="sxs-lookup"><span data-stu-id="0b39f-104">The **Contact** element specifies a contact in the Unified Contact Store.</span></span> 
  
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

 <span data-ttu-id="0b39f-105">**ContactType**</span><span class="sxs-lookup"><span data-stu-id="0b39f-105">**ContactType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b39f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0b39f-106">Attributes and elements</span></span>

<span data-ttu-id="0b39f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0b39f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b39f-108">属性</span><span class="sxs-lookup"><span data-stu-id="0b39f-108">Attributes</span></span>

<span data-ttu-id="0b39f-109">无。</span><span class="sxs-lookup"><span data-stu-id="0b39f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b39f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0b39f-110">Child elements</span></span>

|<span data-ttu-id="0b39f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0b39f-111">**Element**</span></span>|<span data-ttu-id="0b39f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0b39f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b39f-113">PersonName</span><span class="sxs-lookup"><span data-stu-id="0b39f-113">PersonName</span></span>](personname.md) <br/> |<span data-ttu-id="0b39f-114">指定某人的姓名。</span><span class="sxs-lookup"><span data-stu-id="0b39f-114">Specifies the name of an individual.</span></span>  <br/> |
|[<span data-ttu-id="0b39f-115">BusinessName</span><span class="sxs-lookup"><span data-stu-id="0b39f-115">BusinessName</span></span>](businessname.md) <br/> |<span data-ttu-id="0b39f-116">指定业务的名称。</span><span class="sxs-lookup"><span data-stu-id="0b39f-116">Specifies the name of a business.</span></span>  <br/> |
|[<span data-ttu-id="0b39f-117">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="0b39f-117">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="0b39f-118">表示联系人的电话号码的集合。</span><span class="sxs-lookup"><span data-stu-id="0b39f-118">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="0b39f-119">Urls</span><span class="sxs-lookup"><span data-stu-id="0b39f-119">Urls</span></span>](urls.md) <br/> |<span data-ttu-id="0b39f-120">指定的 Url 为角色外的数组。</span><span class="sxs-lookup"><span data-stu-id="0b39f-120">Specifies an array of URLs for a persona.</span></span>  <br/> |
|[<span data-ttu-id="0b39f-121">EmailAddresses (ArrayOfExtractedEmailAddresses)</span><span class="sxs-lookup"><span data-stu-id="0b39f-121">EmailAddresses (ArrayOfExtractedEmailAddresses)</span></span>](emailaddresses-arrayofextractedemailaddresses.md) <br/> |<span data-ttu-id="0b39f-122">指定数组提取电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="0b39f-122">Specifies an array of extracted email addresses.</span></span>  <br/> |
|[<span data-ttu-id="0b39f-123">地址 (ArrayOfAddressesType)</span><span class="sxs-lookup"><span data-stu-id="0b39f-123">Addresses (ArrayOfAddressesType)</span></span>](addresses-arrayofaddressestype.md) <br/> |<span data-ttu-id="0b39f-124">指定**地址**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="0b39f-124">Specifies an array of **Address** elements.</span></span>  <br/> |
|[<span data-ttu-id="0b39f-125">ContactString</span><span class="sxs-lookup"><span data-stu-id="0b39f-125">ContactString</span></span>](contactstring.md) <br/> |<span data-ttu-id="0b39f-126">指定联系人的显示名称。</span><span class="sxs-lookup"><span data-stu-id="0b39f-126">Specifies the display name of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0b39f-127">父元素</span><span class="sxs-lookup"><span data-stu-id="0b39f-127">Parent elements</span></span>

|<span data-ttu-id="0b39f-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="0b39f-128">**Element**</span></span>|<span data-ttu-id="0b39f-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="0b39f-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b39f-130">联系人 (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="0b39f-130">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="0b39f-131">指定联系人的数组。</span><span class="sxs-lookup"><span data-stu-id="0b39f-131">Specifies an array of contacts.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b39f-132">备注</span><span class="sxs-lookup"><span data-stu-id="0b39f-132">Remarks</span></span>

<span data-ttu-id="0b39f-133">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0b39f-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0b39f-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0b39f-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b39f-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="0b39f-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b39f-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="0b39f-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0b39f-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="0b39f-137">Schema Name</span></span>  <br/> |<span data-ttu-id="0b39f-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="0b39f-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="0b39f-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="0b39f-139">Validation File</span></span>  <br/> |<span data-ttu-id="0b39f-140">types.xsd</span><span class="sxs-lookup"><span data-stu-id="0b39f-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0b39f-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="0b39f-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0b39f-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0b39f-142">See also</span></span>



- [<span data-ttu-id="0b39f-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0b39f-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

