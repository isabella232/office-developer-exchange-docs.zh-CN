---
title: EntityExtractionResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: EntityExtractionResult 元素指定项的 EntityExtractionResult 属性。
ms.openlocfilehash: f2f069717a5862adff3349090c35f95499d135f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456953"
---
# <a name="entityextractionresult"></a><span data-ttu-id="2eb83-103">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="2eb83-103">EntityExtractionResult</span></span>

<span data-ttu-id="2eb83-104">**EntityExtractionResult**元素指定项的**EntityExtractionResult**属性。</span><span class="sxs-lookup"><span data-stu-id="2eb83-104">The **EntityExtractionResult** element specifies the **EntityExtractionResult** property of an item.</span></span> 
  
```XML
<EntityExtractionResult>
    <Addresses/>
    <MeetingSuggestions/>
    <TaskSuggestions/>
    <EmailAddresses/>
    <Contacts/>
    <Urls/>
    <PhoneNumbers/>
</EntityExtractionResult>
```

 <span data-ttu-id="2eb83-105">**EntityExtractionResultType**</span><span class="sxs-lookup"><span data-stu-id="2eb83-105">**EntityExtractionResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2eb83-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2eb83-106">Attributes and elements</span></span>

<span data-ttu-id="2eb83-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2eb83-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2eb83-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2eb83-108">Attributes</span></span>

<span data-ttu-id="2eb83-109">无。</span><span class="sxs-lookup"><span data-stu-id="2eb83-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2eb83-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2eb83-110">Child elements</span></span>

|<span data-ttu-id="2eb83-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2eb83-111">**Element**</span></span>|<span data-ttu-id="2eb83-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2eb83-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2eb83-113">地址（ArrayOfAddressEntitiesType）</span><span class="sxs-lookup"><span data-stu-id="2eb83-113">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="2eb83-114">指定**AddressEntity**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="2eb83-114">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
|[<span data-ttu-id="2eb83-115">MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="2eb83-115">MeetingSuggestions</span></span>](meetingsuggestions.md) <br/> |<span data-ttu-id="2eb83-116">指定**MeetingSuggestion**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="2eb83-116">Specifies an array of **MeetingSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="2eb83-117">TaskSuggestions</span><span class="sxs-lookup"><span data-stu-id="2eb83-117">TaskSuggestions</span></span>](tasksuggestions.md) <br/> |<span data-ttu-id="2eb83-118">指定**TaskSuggestion**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="2eb83-118">Specifies an array of **TaskSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="2eb83-119">EmailAddresses （ArrayOfEmailAddressEntitiesType）</span><span class="sxs-lookup"><span data-stu-id="2eb83-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="2eb83-120">指定电子邮件地址实体的数组。</span><span class="sxs-lookup"><span data-stu-id="2eb83-120">Specifies an array of email address entities.</span></span>  <br/> |
|[<span data-ttu-id="2eb83-121">联系人（ArrayOfContactsType）</span><span class="sxs-lookup"><span data-stu-id="2eb83-121">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="2eb83-122">指定联系人数组。</span><span class="sxs-lookup"><span data-stu-id="2eb83-122">Specifies an array of contacts.</span></span>  <br/> |
|[<span data-ttu-id="2eb83-123">Url （ArrayOfUrlEntitiesType）</span><span class="sxs-lookup"><span data-stu-id="2eb83-123">Urls (ArrayOfUrlEntitiesType)</span></span>](urls-arrayofurlentitiestype.md) <br/> |<span data-ttu-id="2eb83-124">指定 Url 的数组。</span><span class="sxs-lookup"><span data-stu-id="2eb83-124">Specifies an array of URLs.</span></span>  <br/> |
|[<span data-ttu-id="2eb83-125">PhoneNumbers （ArrayOfPhoneEntitiesType）</span><span class="sxs-lookup"><span data-stu-id="2eb83-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span></span>](phonenumbers-arrayofphoneentitiestype.md) <br/> |<span data-ttu-id="2eb83-126">指定电话号码的数组。</span><span class="sxs-lookup"><span data-stu-id="2eb83-126">Specifies an array of phone numbers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2eb83-127">父元素</span><span class="sxs-lookup"><span data-stu-id="2eb83-127">Parent elements</span></span>

|<span data-ttu-id="2eb83-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="2eb83-128">**Element**</span></span>|<span data-ttu-id="2eb83-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="2eb83-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2eb83-130">Item</span><span class="sxs-lookup"><span data-stu-id="2eb83-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="2eb83-131">表示 Exchange 存储中的一般项目。</span><span class="sxs-lookup"><span data-stu-id="2eb83-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2eb83-132">备注</span><span class="sxs-lookup"><span data-stu-id="2eb83-132">Remarks</span></span>

<span data-ttu-id="2eb83-133">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2eb83-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2eb83-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2eb83-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2eb83-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="2eb83-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2eb83-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="2eb83-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2eb83-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="2eb83-137">Schema Name</span></span>  <br/> |<span data-ttu-id="2eb83-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="2eb83-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="2eb83-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="2eb83-139">Validation File</span></span>  <br/> |<span data-ttu-id="2eb83-140">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="2eb83-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2eb83-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="2eb83-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2eb83-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2eb83-142">See also</span></span>



- [<span data-ttu-id="2eb83-143">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2eb83-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

