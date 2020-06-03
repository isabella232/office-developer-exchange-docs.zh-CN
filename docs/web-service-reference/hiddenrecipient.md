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
description: HiddenRecipient 元素指示收件人是由应对非特权用户隐藏的组织策略添加的。
ms.openlocfilehash: bfe57fabc02ff00c801672b71ccdb0bf1b916bd9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457639"
---
# <a name="hiddenrecipient"></a><span data-ttu-id="e2637-103">HiddenRecipient</span><span class="sxs-lookup"><span data-stu-id="e2637-103">HiddenRecipient</span></span>

<span data-ttu-id="e2637-104">**HiddenRecipient**元素指示收件人是由应对非特权用户隐藏的组织策略添加的。</span><span class="sxs-lookup"><span data-stu-id="e2637-104">The **HiddenRecipient** element indicates that the recipient was added by an organization policy that should be hidden from unprivileged users.</span></span> 
  
```XML
<HiddenRecipient>true | false</HiddenRecipient>
```

 <span data-ttu-id="e2637-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e2637-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2637-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e2637-106">Attributes and elements</span></span>

<span data-ttu-id="e2637-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e2637-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2637-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e2637-108">Attributes</span></span>

<span data-ttu-id="e2637-109">无。</span><span class="sxs-lookup"><span data-stu-id="e2637-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2637-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e2637-110">Child elements</span></span>

<span data-ttu-id="e2637-111">无。</span><span class="sxs-lookup"><span data-stu-id="e2637-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e2637-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e2637-112">Parent elements</span></span>

|<span data-ttu-id="e2637-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e2637-113">**Element**</span></span>|<span data-ttu-id="e2637-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e2637-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2637-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="e2637-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="e2637-116">包含收件人的单个事件的信息。</span><span class="sxs-lookup"><span data-stu-id="e2637-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e2637-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e2637-117">Text value</span></span>

<span data-ttu-id="e2637-118">此元素可以是**true** ，也可以是**false**。</span><span class="sxs-lookup"><span data-stu-id="e2637-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="e2637-119">**如果值为 true** ，则表示用户是由组织策略添加的;**如果值为 false** ，则表示组织策略未添加用户。</span><span class="sxs-lookup"><span data-stu-id="e2637-119">A value of **true** indicates that the user was added by an organization policy; a value of **false** indicates that the user was not added by an organization policy.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e2637-120">说明</span><span class="sxs-lookup"><span data-stu-id="e2637-120">Remarks</span></span>

<span data-ttu-id="e2637-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e2637-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2637-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="e2637-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2637-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="e2637-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e2637-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="e2637-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e2637-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="e2637-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="e2637-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="e2637-126">Validation File</span></span>  <br/> |<span data-ttu-id="e2637-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e2637-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e2637-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="e2637-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2637-129">False</span><span class="sxs-lookup"><span data-stu-id="e2637-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2637-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2637-130">See also</span></span>



- [<span data-ttu-id="e2637-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e2637-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

