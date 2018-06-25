---
title: HiddenRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HiddenRecipient
api_type:
- schema
ms.assetid: a8209f75-0070-4424-8dcd-273cfd192728
description: HiddenRecipient 元素指示收件人已添加应从未经授权的用户隐藏组织策略。
ms.openlocfilehash: 73b2e3e39c675cf3e2bc56105b1e76009d4a2451
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825810"
---
# <a name="hiddenrecipient"></a><span data-ttu-id="d1de2-103">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="d1de2-103">HiddenRecipient</span></span>

<span data-ttu-id="d1de2-104">**HiddenRecipient**元素指示收件人已添加应从未经授权的用户隐藏组织策略。</span><span class="sxs-lookup"><span data-stu-id="d1de2-104">The **HiddenRecipient** element indicates that the recipient was added by an organization policy that should be hidden from unprivileged users.</span></span> 
  
```XML
<HiddenRecipient>true | false</HiddenRecipient>
```

 <span data-ttu-id="d1de2-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d1de2-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1de2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d1de2-106">Attributes and elements</span></span>

<span data-ttu-id="d1de2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d1de2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1de2-108">属性</span><span class="sxs-lookup"><span data-stu-id="d1de2-108">Attributes</span></span>

<span data-ttu-id="d1de2-109">无。</span><span class="sxs-lookup"><span data-stu-id="d1de2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1de2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d1de2-110">Child elements</span></span>

<span data-ttu-id="d1de2-111">无。</span><span class="sxs-lookup"><span data-stu-id="d1de2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1de2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d1de2-112">Parent elements</span></span>

|<span data-ttu-id="d1de2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d1de2-113">**Element**</span></span>|<span data-ttu-id="d1de2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d1de2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1de2-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="d1de2-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="d1de2-116">包含收件人为一个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="d1de2-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d1de2-117">文本值</span><span class="sxs-lookup"><span data-stu-id="d1de2-117">Text value</span></span>

<span data-ttu-id="d1de2-118">此元素可以是**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="d1de2-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="d1de2-119">值为**true**指示用户已添加通过组织的策略。如果值为**false**指示用户没有被添加组织策略。</span><span class="sxs-lookup"><span data-stu-id="d1de2-119">A value of **true** indicates that the user was added by an organization policy; a value of **false** indicates that the user was not added by an organization policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d1de2-120">备注</span><span class="sxs-lookup"><span data-stu-id="d1de2-120">Remarks</span></span>

<span data-ttu-id="d1de2-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d1de2-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1de2-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="d1de2-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1de2-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="d1de2-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1de2-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="d1de2-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d1de2-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="d1de2-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1de2-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="d1de2-126">Validation File</span></span>  <br/> |<span data-ttu-id="d1de2-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1de2-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1de2-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="d1de2-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1de2-129">False</span><span class="sxs-lookup"><span data-stu-id="d1de2-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1de2-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d1de2-130">See also</span></span>



- [<span data-ttu-id="d1de2-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d1de2-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

