---
title: ContactSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactSource
api_type:
- schema
ms.assetid: 500b0423-864e-4cde-a39b-6b5b06d1aa6a
description: ContactSource 元素描述联系人是否位于 Exchange 存储区或 Active Directory 域服务（AD DS）中。
ms.openlocfilehash: 5447dedf199c5ad6b944aa33e6dca03e83a3c340
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462708"
---
# <a name="contactsource"></a><span data-ttu-id="b37b6-103">ContactSource</span><span class="sxs-lookup"><span data-stu-id="b37b6-103">ContactSource</span></span>

<span data-ttu-id="b37b6-104">**ContactSource**元素描述联系人是否位于 Exchange 存储区或 Active Directory 域服务（AD DS）中。</span><span class="sxs-lookup"><span data-stu-id="b37b6-104">The **ContactSource** element describes whether the contact is located in the Exchange store or Active Directory Domain Services (AD DS).</span></span> 
  
```xml
<ContactSource/>
```

 <span data-ttu-id="b37b6-105">**ContactSourceType**</span><span class="sxs-lookup"><span data-stu-id="b37b6-105">**ContactSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b37b6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b37b6-106">Attributes and elements</span></span>

<span data-ttu-id="b37b6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b37b6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b37b6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b37b6-108">Attributes</span></span>

<span data-ttu-id="b37b6-109">无。</span><span class="sxs-lookup"><span data-stu-id="b37b6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b37b6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b37b6-110">Child elements</span></span>

<span data-ttu-id="b37b6-111">无。</span><span class="sxs-lookup"><span data-stu-id="b37b6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b37b6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b37b6-112">Parent elements</span></span>

|<span data-ttu-id="b37b6-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b37b6-113">**Element**</span></span>|<span data-ttu-id="b37b6-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b37b6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b37b6-115">联系人</span><span class="sxs-lookup"><span data-stu-id="b37b6-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="b37b6-116">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="b37b6-116">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b37b6-117">DistributionList</span><span class="sxs-lookup"><span data-stu-id="b37b6-117">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="b37b6-118">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="b37b6-118">Represents a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b37b6-119">文本值</span><span class="sxs-lookup"><span data-stu-id="b37b6-119">Text value</span></span>

<span data-ttu-id="b37b6-120">以下是此元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="b37b6-120">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="b37b6-121">ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="b37b6-121">ActiveDirectory</span></span>
    
- <span data-ttu-id="b37b6-122">应用商店</span><span class="sxs-lookup"><span data-stu-id="b37b6-122">Store</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b37b6-123">说明</span><span class="sxs-lookup"><span data-stu-id="b37b6-123">Remarks</span></span>

<span data-ttu-id="b37b6-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b37b6-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b37b6-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="b37b6-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b37b6-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="b37b6-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b37b6-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="b37b6-127">Schema name</span></span>  <br/> |<span data-ttu-id="b37b6-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="b37b6-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="b37b6-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="b37b6-129">Validation file</span></span>  <br/> |<span data-ttu-id="b37b6-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b37b6-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b37b6-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="b37b6-131">Can be empty</span></span>  <br/> |<span data-ttu-id="b37b6-132">False</span><span class="sxs-lookup"><span data-stu-id="b37b6-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b37b6-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b37b6-133">See also</span></span>



- [<span data-ttu-id="b37b6-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b37b6-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

