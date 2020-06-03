---
title: 演讲
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: 演示者元素指定联机会议的演示者。
ms.openlocfilehash: 0236457020dfc4684569e84d3d54e357af00d102
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529908"
---
# <a name="presenters"></a><span data-ttu-id="114f6-103">演讲</span><span class="sxs-lookup"><span data-stu-id="114f6-103">Presenters</span></span>

<span data-ttu-id="114f6-104">**演示者**元素指定联机会议的演示者。</span><span class="sxs-lookup"><span data-stu-id="114f6-104">The **Presenters** element specifies the presenters for an online meeting.</span></span> 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 <span data-ttu-id="114f6-105">**PresentersType**</span><span class="sxs-lookup"><span data-stu-id="114f6-105">**PresentersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="114f6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="114f6-106">Attributes and elements</span></span>

<span data-ttu-id="114f6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="114f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="114f6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="114f6-108">Attributes</span></span>

<span data-ttu-id="114f6-109">无。</span><span class="sxs-lookup"><span data-stu-id="114f6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="114f6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="114f6-110">Child elements</span></span>

<span data-ttu-id="114f6-111">无。</span><span class="sxs-lookup"><span data-stu-id="114f6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="114f6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="114f6-112">Parent elements</span></span>

[<span data-ttu-id="114f6-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="114f6-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="114f6-114">文本值</span><span class="sxs-lookup"><span data-stu-id="114f6-114">Text value</span></span>

<span data-ttu-id="114f6-115">**演示者**元素的文本值是可以成为联机会议的演示者的用户的类型。</span><span class="sxs-lookup"><span data-stu-id="114f6-115">The text value of **Presenters** element is the type of users that can be a presenter for an online meeting.</span></span> <span data-ttu-id="114f6-116">下表介绍了**演示者**元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="114f6-116">The text values for the **Presenters** element are described in the following table.</span></span> 
  
<span data-ttu-id="114f6-117">**演示者元素文本值**</span><span class="sxs-lookup"><span data-stu-id="114f6-117">**Presenters element text values**</span></span>

|<span data-ttu-id="114f6-118">**值**</span><span class="sxs-lookup"><span data-stu-id="114f6-118">**Value**</span></span>|<span data-ttu-id="114f6-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="114f6-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="114f6-120">已禁用</span><span class="sxs-lookup"><span data-stu-id="114f6-120">Disabled</span></span>  <br/> |<span data-ttu-id="114f6-121">演示者已禁用。</span><span class="sxs-lookup"><span data-stu-id="114f6-121">Presenters are disabled.</span></span>  <br/> |
|<span data-ttu-id="114f6-122">内部</span><span class="sxs-lookup"><span data-stu-id="114f6-122">Internal</span></span>  <br/> |<span data-ttu-id="114f6-123">只有内部参与者可以成为演示者。</span><span class="sxs-lookup"><span data-stu-id="114f6-123">Only internal participants can be presenters.</span></span>  <br/> |
|<span data-ttu-id="114f6-124">每个人</span><span class="sxs-lookup"><span data-stu-id="114f6-124">Everyone</span></span>  <br/> |<span data-ttu-id="114f6-125">任何参与者都可以成为演示者。</span><span class="sxs-lookup"><span data-stu-id="114f6-125">Any participant can be a presenter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="114f6-126">备注</span><span class="sxs-lookup"><span data-stu-id="114f6-126">Remarks</span></span>

<span data-ttu-id="114f6-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="114f6-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="114f6-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="114f6-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="114f6-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="114f6-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="114f6-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="114f6-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="114f6-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="114f6-131">Schema name</span></span>  <br/> |<span data-ttu-id="114f6-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="114f6-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="114f6-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="114f6-133">Validation file</span></span>  <br/> |<span data-ttu-id="114f6-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="114f6-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="114f6-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="114f6-135">Can be empty</span></span>  <br/> ||
   

