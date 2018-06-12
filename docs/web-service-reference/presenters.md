---
title: 演示者
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: 演示者元素指定的联机会议的演示者。
ms.openlocfilehash: f62b458759e0d8199c98827602d6c3fe16aebeea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826875"
---
# <a name="presenters"></a><span data-ttu-id="acab3-103">演示者</span><span class="sxs-lookup"><span data-stu-id="acab3-103">Presenters</span></span>

<span data-ttu-id="acab3-104">**演示者**元素指定的联机会议的演示者。</span><span class="sxs-lookup"><span data-stu-id="acab3-104">The **Presenters** element specifies the presenters for an online meeting.</span></span> 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 <span data-ttu-id="acab3-105">**PresentersType**</span><span class="sxs-lookup"><span data-stu-id="acab3-105">**PresentersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="acab3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="acab3-106">Attributes and elements</span></span>

<span data-ttu-id="acab3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="acab3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acab3-108">属性</span><span class="sxs-lookup"><span data-stu-id="acab3-108">Attributes</span></span>

<span data-ttu-id="acab3-109">无。</span><span class="sxs-lookup"><span data-stu-id="acab3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acab3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="acab3-110">Child elements</span></span>

<span data-ttu-id="acab3-111">无。</span><span class="sxs-lookup"><span data-stu-id="acab3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="acab3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="acab3-112">Parent elements</span></span>

[<span data-ttu-id="acab3-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="acab3-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="acab3-114">文本值</span><span class="sxs-lookup"><span data-stu-id="acab3-114">Text value</span></span>

<span data-ttu-id="acab3-115">**演示者**元素的文本值的用户可以在联机会议的演示者的类型。</span><span class="sxs-lookup"><span data-stu-id="acab3-115">The text value of **Presenters** element is the type of users that can be a presenter for an online meeting.</span></span> <span data-ttu-id="acab3-116">下表中介绍的**演示者**元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="acab3-116">The text values for the **Presenters** element are described in the following table.</span></span> 
  
<span data-ttu-id="acab3-117">**演示者元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="acab3-117">**Presenters element text values**</span></span>

|<span data-ttu-id="acab3-118">**值**</span><span class="sxs-lookup"><span data-stu-id="acab3-118">**Value**</span></span>|<span data-ttu-id="acab3-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="acab3-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="acab3-120">已禁用</span><span class="sxs-lookup"><span data-stu-id="acab3-120">Disabled</span></span>  <br/> |<span data-ttu-id="acab3-121">演示者将被禁用。</span><span class="sxs-lookup"><span data-stu-id="acab3-121">Presenters are disabled.</span></span>  <br/> |
|<span data-ttu-id="acab3-122">内部</span><span class="sxs-lookup"><span data-stu-id="acab3-122">Internal</span></span>  <br/> |<span data-ttu-id="acab3-123">仅内部的参与者可以是演示者。</span><span class="sxs-lookup"><span data-stu-id="acab3-123">Only internal participants can be presenters.</span></span>  <br/> |
|<span data-ttu-id="acab3-124">所有人</span><span class="sxs-lookup"><span data-stu-id="acab3-124">Everyone</span></span>  <br/> |<span data-ttu-id="acab3-125">任何参与者都可以成为演示者。</span><span class="sxs-lookup"><span data-stu-id="acab3-125">Any participant can be a presenter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acab3-126">备注</span><span class="sxs-lookup"><span data-stu-id="acab3-126">Remarks</span></span>

<span data-ttu-id="acab3-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="acab3-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="acab3-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="acab3-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acab3-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="acab3-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acab3-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="acab3-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="acab3-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="acab3-131">Schema name</span></span>  <br/> |<span data-ttu-id="acab3-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="acab3-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="acab3-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="acab3-133">Validation file</span></span>  <br/> |<span data-ttu-id="acab3-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="acab3-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="acab3-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="acab3-135">Can be empty</span></span>  <br/> ||
   

