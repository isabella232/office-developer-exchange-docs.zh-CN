---
title: AccessLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 09475586-00fa-4e82-a915-5ca263ab4d1c
description: AccessLevel 元素指定联机会议的访问级别。
ms.openlocfilehash: 3c1375ef37ea666c6c4fafce7daa46ae0d0a2696
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462337"
---
# <a name="accesslevel"></a><span data-ttu-id="c7ef3-103">AccessLevel</span><span class="sxs-lookup"><span data-stu-id="c7ef3-103">AccessLevel</span></span>

<span data-ttu-id="c7ef3-104">**AccessLevel**元素指定联机会议的访问级别。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-104">The **AccessLevel** element specifies the access level for an online meeting.</span></span> 
  
```XML
<AccessLevel/>
```

 <span data-ttu-id="c7ef3-105">**OnlineMeetingSettingsType**</span><span class="sxs-lookup"><span data-stu-id="c7ef3-105">**OnlineMeetingSettingsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7ef3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c7ef3-106">Attributes and elements</span></span>

<span data-ttu-id="c7ef3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7ef3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c7ef3-108">Attributes</span></span>

<span data-ttu-id="c7ef3-109">无。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7ef3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c7ef3-110">Child elements</span></span>

<span data-ttu-id="c7ef3-111">无。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7ef3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c7ef3-112">Parent elements</span></span>

|<span data-ttu-id="c7ef3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c7ef3-113">**Element**</span></span>|<span data-ttu-id="c7ef3-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="c7ef3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7ef3-115">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="c7ef3-115">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md) <br/> |<span data-ttu-id="c7ef3-116">指定联机会议的设置。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-116">Specifies the settings for online meetings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c7ef3-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c7ef3-117">Text value</span></span>

<span data-ttu-id="c7ef3-118">下表列出了**AccessLevel**元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-118">The following table lists the text values for the **AccessLevel** element.</span></span> 
  
<span data-ttu-id="c7ef3-119">**AccessLevel 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="c7ef3-119">**AccessLevel element text values**</span></span>

|<span data-ttu-id="c7ef3-120">**值**</span><span class="sxs-lookup"><span data-stu-id="c7ef3-120">**Value**</span></span>|<span data-ttu-id="c7ef3-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="c7ef3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7ef3-122">每个人</span><span class="sxs-lookup"><span data-stu-id="c7ef3-122">Everyone</span></span>  <br/> |<span data-ttu-id="c7ef3-123">访问级别全部打开。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-123">The access level is open to all.</span></span>  <br/> |
|<span data-ttu-id="c7ef3-124">内部</span><span class="sxs-lookup"><span data-stu-id="c7ef3-124">Internal</span></span>  <br/> |<span data-ttu-id="c7ef3-125">访问级别仅为 "仅限内部"。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-125">The access level is internal only.</span></span>  <br/> |
|<span data-ttu-id="c7ef3-126">获</span><span class="sxs-lookup"><span data-stu-id="c7ef3-126">Invited</span></span>  <br/> |<span data-ttu-id="c7ef3-127">访问级别仅受邀请参与者。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-127">The access level is invited participants only.</span></span>  <br/> |
|<span data-ttu-id="c7ef3-128">已锁定</span><span class="sxs-lookup"><span data-stu-id="c7ef3-128">Locked</span></span>  <br/> |<span data-ttu-id="c7ef3-129">访问级别被锁定。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-129">The access level is locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7ef3-130">说明</span><span class="sxs-lookup"><span data-stu-id="c7ef3-130">Remarks</span></span>

<span data-ttu-id="c7ef3-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="c7ef3-132">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c7ef3-132">This element was introduced in Exchange Server 2013.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7ef3-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="c7ef3-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7ef3-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="c7ef3-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7ef3-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="c7ef3-135">Schema name</span></span>  <br/> |<span data-ttu-id="c7ef3-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="c7ef3-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="c7ef3-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="c7ef3-137">Validation file</span></span>  <br/> |<span data-ttu-id="c7ef3-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c7ef3-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7ef3-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="c7ef3-139">Can be empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c7ef3-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c7ef3-140">See also</span></span>

- [<span data-ttu-id="c7ef3-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c7ef3-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

