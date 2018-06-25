---
title: IsAutomaticForward
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAutomaticForward
api_type:
- schema
ms.assetid: 6876b849-a648-482e-8934-93eb5a0c465f
description: IsAutomaticForward 元素指示是否必须按条件或例外的顺序应用自动转发传入消息。
ms.openlocfilehash: c2d44d6dce30cbf55e0c7673aaf41b114a3e2cd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825989"
---
# <a name="isautomaticforward"></a><span data-ttu-id="f181e-103">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="f181e-103">IsAutomaticForward</span></span>

<span data-ttu-id="f181e-104">**IsAutomaticForward**元素指示是否必须按条件或例外的顺序应用自动转发传入消息。</span><span class="sxs-lookup"><span data-stu-id="f181e-104">The **IsAutomaticForward** element indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span> 
  
```XML
<IsAutomaticForward/> true | false</IsAutomaticForward>
```

 <span data-ttu-id="f181e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f181e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f181e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f181e-106">Attributes and elements</span></span>

<span data-ttu-id="f181e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f181e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f181e-108">属性</span><span class="sxs-lookup"><span data-stu-id="f181e-108">Attributes</span></span>

<span data-ttu-id="f181e-109">无。</span><span class="sxs-lookup"><span data-stu-id="f181e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f181e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f181e-110">Child elements</span></span>

<span data-ttu-id="f181e-111">无。</span><span class="sxs-lookup"><span data-stu-id="f181e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f181e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f181e-112">Parent elements</span></span>

|<span data-ttu-id="f181e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f181e-113">**Element**</span></span>|<span data-ttu-id="f181e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f181e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f181e-115">条件</span><span class="sxs-lookup"><span data-stu-id="f181e-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="f181e-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="f181e-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="f181e-117">异常</span><span class="sxs-lookup"><span data-stu-id="f181e-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="f181e-118">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="f181e-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f181e-119">文本值</span><span class="sxs-lookup"><span data-stu-id="f181e-119">Text value</span></span>

<span data-ttu-id="f181e-120">文本值为**true**指示邮件必须按条件或例外的顺序应用自动转接。</span><span class="sxs-lookup"><span data-stu-id="f181e-120">A text value of **true** indicates that the message must be an automatic forward in order for the condition or exception to apply.</span></span> <span data-ttu-id="f181e-121">如果值为**false**指示邮件不得中的条件或例外的顺序应用自动转接。</span><span class="sxs-lookup"><span data-stu-id="f181e-121">A value of **false** indicates that the message must not be an automatic forward in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f181e-122">备注</span><span class="sxs-lookup"><span data-stu-id="f181e-122">Remarks</span></span>

<span data-ttu-id="f181e-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f181e-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f181e-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="f181e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f181e-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="f181e-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f181e-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="f181e-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f181e-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="f181e-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f181e-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="f181e-128">Validation File</span></span>  <br/> |<span data-ttu-id="f181e-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f181e-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f181e-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="f181e-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f181e-131">True</span><span class="sxs-lookup"><span data-stu-id="f181e-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f181e-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f181e-132">See also</span></span>



- [<span data-ttu-id="f181e-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f181e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

