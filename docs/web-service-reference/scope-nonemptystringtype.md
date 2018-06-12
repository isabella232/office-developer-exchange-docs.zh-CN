---
title: 范围 (NonEmptyStringType)
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
description: Scope 元素指定的邮件跟踪报告的范围。
ms.openlocfilehash: 534ed23916a60b246c7cb5be4a59d086980a7c37
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827280"
---
# <a name="scope-nonemptystringtype"></a><span data-ttu-id="feffa-103">范围 (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="feffa-103">Scope (NonEmptyStringType)</span></span>

<span data-ttu-id="feffa-104">**Scope**元素指定的邮件跟踪报告的范围。</span><span class="sxs-lookup"><span data-stu-id="feffa-104">The **Scope** element specifies the scope of the message tracking report.</span></span> 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 <span data-ttu-id="feffa-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="feffa-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="feffa-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="feffa-106">Attributes and elements</span></span>

<span data-ttu-id="feffa-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="feffa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="feffa-108">属性</span><span class="sxs-lookup"><span data-stu-id="feffa-108">Attributes</span></span>

<span data-ttu-id="feffa-109">无。</span><span class="sxs-lookup"><span data-stu-id="feffa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="feffa-110">子元素</span><span class="sxs-lookup"><span data-stu-id="feffa-110">Child elements</span></span>

<span data-ttu-id="feffa-111">无。</span><span class="sxs-lookup"><span data-stu-id="feffa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="feffa-112">父元素</span><span class="sxs-lookup"><span data-stu-id="feffa-112">Parent elements</span></span>

<span data-ttu-id="feffa-113">[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)</span><span class="sxs-lookup"><span data-stu-id="feffa-113">[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="feffa-114">文本值</span><span class="sxs-lookup"><span data-stu-id="feffa-114">Text value</span></span>

<span data-ttu-id="feffa-115">下表列出了可能的**范围**元素的值。</span><span class="sxs-lookup"><span data-stu-id="feffa-115">The following table lists the possible values for the **Scope** element.</span></span> 
  
|<span data-ttu-id="feffa-116">**值**</span><span class="sxs-lookup"><span data-stu-id="feffa-116">**Value**</span></span>|<span data-ttu-id="feffa-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="feffa-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="feffa-118">组织</span><span class="sxs-lookup"><span data-stu-id="feffa-118">Organization</span></span>  <br/> |<span data-ttu-id="feffa-119">邮件跟踪范围跨越组织。</span><span class="sxs-lookup"><span data-stu-id="feffa-119">The message tracking scopes spans across an organization.</span></span>  <br/> |
|<span data-ttu-id="feffa-120">林</span><span class="sxs-lookup"><span data-stu-id="feffa-120">Forest</span></span>  <br/> |<span data-ttu-id="feffa-121">邮件跟踪范围跨跨林。</span><span class="sxs-lookup"><span data-stu-id="feffa-121">The message tracking scopes spans across a forest.</span></span>  <br/> |
|<span data-ttu-id="feffa-122">网站</span><span class="sxs-lookup"><span data-stu-id="feffa-122">Site</span></span>  <br/> |<span data-ttu-id="feffa-123">邮件跟踪范围跨整个网站。</span><span class="sxs-lookup"><span data-stu-id="feffa-123">The message tracking scopes spans across a site.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="feffa-124">备注</span><span class="sxs-lookup"><span data-stu-id="feffa-124">Remarks</span></span>

<span data-ttu-id="feffa-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="feffa-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="feffa-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="feffa-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="feffa-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="feffa-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="feffa-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="feffa-128">Schema Name</span></span>  <br/> |<span data-ttu-id="feffa-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="feffa-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="feffa-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="feffa-130">Validation File</span></span>  <br/> |<span data-ttu-id="feffa-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="feffa-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="feffa-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="feffa-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="feffa-133">False</span><span class="sxs-lookup"><span data-stu-id="feffa-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="feffa-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="feffa-134">See also</span></span>



- [<span data-ttu-id="feffa-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="feffa-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
