---
title: IsAutomaticReply
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAutomaticReply
api_type:
- schema
ms.assetid: 280e9baf-199d-422c-8fdf-1d0751a3e77d
description: IsAutomaticReply 元素指示是否必须按条件或例外的顺序应用的自动答复传入消息。
ms.openlocfilehash: 3f26b947313b8c53f70e2a89b9a6bdd17840a055
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825995"
---
# <a name="isautomaticreply"></a><span data-ttu-id="77448-103">IsAutomaticReply</span><span class="sxs-lookup"><span data-stu-id="77448-103">IsAutomaticReply</span></span>

<span data-ttu-id="77448-104">**IsAutomaticReply**元素指示是否必须按条件或例外的顺序应用的自动答复传入消息。</span><span class="sxs-lookup"><span data-stu-id="77448-104">The **IsAutomaticReply** element indicates whether incoming messages must be automatic replies in order for the condition or exception to apply.</span></span> 
  
```XML
<IsAutomaticReply> true | false</IsAutomaticReply>
```

 <span data-ttu-id="77448-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="77448-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77448-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="77448-106">Attributes and elements</span></span>

<span data-ttu-id="77448-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="77448-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77448-108">属性</span><span class="sxs-lookup"><span data-stu-id="77448-108">Attributes</span></span>

<span data-ttu-id="77448-109">无。</span><span class="sxs-lookup"><span data-stu-id="77448-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77448-110">子元素</span><span class="sxs-lookup"><span data-stu-id="77448-110">Child elements</span></span>

<span data-ttu-id="77448-111">无。</span><span class="sxs-lookup"><span data-stu-id="77448-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="77448-112">父元素</span><span class="sxs-lookup"><span data-stu-id="77448-112">Parent elements</span></span>

|<span data-ttu-id="77448-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="77448-113">**Element**</span></span>|<span data-ttu-id="77448-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="77448-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77448-115">条件</span><span class="sxs-lookup"><span data-stu-id="77448-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="77448-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="77448-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="77448-117">异常</span><span class="sxs-lookup"><span data-stu-id="77448-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="77448-118">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="77448-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="77448-119">文本值</span><span class="sxs-lookup"><span data-stu-id="77448-119">Text value</span></span>

<span data-ttu-id="77448-120">文本值为**true**指示邮件必须自动回复中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="77448-120">A text value of **true** indicates that the message must be an automatic reply in order for the condition or exception to apply.</span></span> <span data-ttu-id="77448-121">如果值为**false**指示邮件不必为自动回复中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="77448-121">A value of **false** indicates that the message does not have to be an automatic reply in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="77448-122">备注</span><span class="sxs-lookup"><span data-stu-id="77448-122">Remarks</span></span>

<span data-ttu-id="77448-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="77448-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77448-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="77448-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77448-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="77448-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="77448-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="77448-126">Schema Name</span></span>  <br/> |<span data-ttu-id="77448-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="77448-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="77448-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="77448-128">Validation File</span></span>  <br/> |<span data-ttu-id="77448-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="77448-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="77448-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="77448-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="77448-131">True</span><span class="sxs-lookup"><span data-stu-id="77448-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77448-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77448-132">See also</span></span>



- [<span data-ttu-id="77448-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="77448-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

