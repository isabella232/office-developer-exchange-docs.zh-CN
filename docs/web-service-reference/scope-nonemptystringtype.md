---
title: 范围（NonEmptyStringType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Scope
api_type:
- schema
ms.assetid: 7efb6fd9-1615-469e-96f6-0f7846ad9b44
description: Scope 元素指定邮件跟踪报告的范围。
ms.openlocfilehash: f86f6198e84e094e61ee569f6d005549316bbb9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466939"
---
# <a name="scope-nonemptystringtype"></a><span data-ttu-id="4d736-103">范围（NonEmptyStringType）</span><span class="sxs-lookup"><span data-stu-id="4d736-103">Scope (NonEmptyStringType)</span></span>

<span data-ttu-id="4d736-104">**Scope**元素指定邮件跟踪报告的范围。</span><span class="sxs-lookup"><span data-stu-id="4d736-104">The **Scope** element specifies the scope of the message tracking report.</span></span> 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 <span data-ttu-id="4d736-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="4d736-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d736-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4d736-106">Attributes and elements</span></span>

<span data-ttu-id="4d736-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4d736-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d736-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4d736-108">Attributes</span></span>

<span data-ttu-id="4d736-109">无。</span><span class="sxs-lookup"><span data-stu-id="4d736-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d736-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4d736-110">Child elements</span></span>

<span data-ttu-id="4d736-111">无。</span><span class="sxs-lookup"><span data-stu-id="4d736-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4d736-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4d736-112">Parent elements</span></span>

<span data-ttu-id="4d736-113">[FindMessageTrackingReport](findmessagetrackingreport.md)  | [GetMessageTrackingReport](getmessagetrackingreport.md)</span><span class="sxs-lookup"><span data-stu-id="4d736-113">[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4d736-114">文本值</span><span class="sxs-lookup"><span data-stu-id="4d736-114">Text value</span></span>

<span data-ttu-id="4d736-115">下表列出了**Scope**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="4d736-115">The following table lists the possible values for the **Scope** element.</span></span> 
  
|<span data-ttu-id="4d736-116">**值**</span><span class="sxs-lookup"><span data-stu-id="4d736-116">**Value**</span></span>|<span data-ttu-id="4d736-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d736-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d736-118">组织</span><span class="sxs-lookup"><span data-stu-id="4d736-118">Organization</span></span>  <br/> |<span data-ttu-id="4d736-119">邮件跟踪作用域跨越整个组织。</span><span class="sxs-lookup"><span data-stu-id="4d736-119">The message tracking scopes spans across an organization.</span></span>  <br/> |
|<span data-ttu-id="4d736-120">林</span><span class="sxs-lookup"><span data-stu-id="4d736-120">Forest</span></span>  <br/> |<span data-ttu-id="4d736-121">邮件跟踪作用域跨林分布。</span><span class="sxs-lookup"><span data-stu-id="4d736-121">The message tracking scopes spans across a forest.</span></span>  <br/> |
|<span data-ttu-id="4d736-122">Site</span><span class="sxs-lookup"><span data-stu-id="4d736-122">Site</span></span>  <br/> |<span data-ttu-id="4d736-123">邮件跟踪作用域跨越一个站点。</span><span class="sxs-lookup"><span data-stu-id="4d736-123">The message tracking scopes spans across a site.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d736-124">说明</span><span class="sxs-lookup"><span data-stu-id="4d736-124">Remarks</span></span>

<span data-ttu-id="4d736-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4d736-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d736-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="4d736-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d736-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="4d736-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4d736-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="4d736-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4d736-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="4d736-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4d736-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="4d736-130">Validation File</span></span>  <br/> |<span data-ttu-id="4d736-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4d736-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4d736-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="4d736-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="4d736-133">False</span><span class="sxs-lookup"><span data-stu-id="4d736-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d736-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d736-134">See also</span></span>



- [<span data-ttu-id="4d736-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4d736-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

