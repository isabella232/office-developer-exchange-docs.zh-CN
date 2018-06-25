---
title: EntityExtractionResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: EntityExtractionResult 元素指定项目的 EntityExtractionResult 属性。
ms.openlocfilehash: ef99629beb95f1e1123569fa99e3f495c1b56e95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754139"
---
# <a name="entityextractionresult"></a><span data-ttu-id="db22e-103">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="db22e-103">EntityExtractionResult</span></span>

<span data-ttu-id="db22e-104">**EntityExtractionResult**元素指定项目的**EntityExtractionResult**属性。</span><span class="sxs-lookup"><span data-stu-id="db22e-104">The **EntityExtractionResult** element specifies the **EntityExtractionResult** property of an item.</span></span> 
  
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

 <span data-ttu-id="db22e-105">**EntityExtractionResultType**</span><span class="sxs-lookup"><span data-stu-id="db22e-105">**EntityExtractionResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db22e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="db22e-106">Attributes and elements</span></span>

<span data-ttu-id="db22e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="db22e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db22e-108">属性</span><span class="sxs-lookup"><span data-stu-id="db22e-108">Attributes</span></span>

<span data-ttu-id="db22e-109">无。</span><span class="sxs-lookup"><span data-stu-id="db22e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db22e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="db22e-110">Child elements</span></span>

|<span data-ttu-id="db22e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="db22e-111">**Element**</span></span>|<span data-ttu-id="db22e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="db22e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db22e-113">地址 (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="db22e-113">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="db22e-114">指定**AddressEntity**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="db22e-114">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
|[<span data-ttu-id="db22e-115">MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="db22e-115">MeetingSuggestions</span></span>](meetingsuggestions.md) <br/> |<span data-ttu-id="db22e-116">指定**MeetingSuggestion**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="db22e-116">Specifies an array of **MeetingSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="db22e-117">TaskSuggestions</span><span class="sxs-lookup"><span data-stu-id="db22e-117">TaskSuggestions</span></span>](tasksuggestions.md) <br/> |<span data-ttu-id="db22e-118">指定**TaskSuggestion**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="db22e-118">Specifies an array of **TaskSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="db22e-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="db22e-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="db22e-120">指定电子邮件地址实体的数组。</span><span class="sxs-lookup"><span data-stu-id="db22e-120">Specifies an array of email address entities.</span></span>  <br/> |
|[<span data-ttu-id="db22e-121">联系人 (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="db22e-121">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="db22e-122">指定联系人的数组。</span><span class="sxs-lookup"><span data-stu-id="db22e-122">Specifies an array of contacts.</span></span>  <br/> |
|[<span data-ttu-id="db22e-123">Url (ArrayOfUrlEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="db22e-123">Urls (ArrayOfUrlEntitiesType)</span></span>](urls-arrayofurlentitiestype.md) <br/> |<span data-ttu-id="db22e-124">指定的 Url 的数组。</span><span class="sxs-lookup"><span data-stu-id="db22e-124">Specifies an array of URLs.</span></span>  <br/> |
|[<span data-ttu-id="db22e-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="db22e-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span></span>](phonenumbers-arrayofphoneentitiestype.md) <br/> |<span data-ttu-id="db22e-126">指定电话号码的数组。</span><span class="sxs-lookup"><span data-stu-id="db22e-126">Specifies an array of phone numbers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="db22e-127">父元素</span><span class="sxs-lookup"><span data-stu-id="db22e-127">Parent elements</span></span>

|<span data-ttu-id="db22e-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="db22e-128">**Element**</span></span>|<span data-ttu-id="db22e-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="db22e-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db22e-130">Item</span><span class="sxs-lookup"><span data-stu-id="db22e-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="db22e-131">表示 Exchange 存储中的泛型项。</span><span class="sxs-lookup"><span data-stu-id="db22e-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db22e-132">备注</span><span class="sxs-lookup"><span data-stu-id="db22e-132">Remarks</span></span>

<span data-ttu-id="db22e-133">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="db22e-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="db22e-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="db22e-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db22e-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="db22e-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db22e-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="db22e-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="db22e-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="db22e-137">Schema Name</span></span>  <br/> |<span data-ttu-id="db22e-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="db22e-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="db22e-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="db22e-139">Validation File</span></span>  <br/> |<span data-ttu-id="db22e-140">types.xsd</span><span class="sxs-lookup"><span data-stu-id="db22e-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="db22e-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="db22e-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="db22e-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="db22e-142">See also</span></span>



- [<span data-ttu-id="db22e-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="db22e-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

