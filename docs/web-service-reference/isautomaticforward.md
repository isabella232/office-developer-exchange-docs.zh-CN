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
description: IsAutomaticForward 元素指示传入的邮件是否必须自动转发，以便条件或例外情况适用。
ms.openlocfilehash: 800d38bab30245d88b3c09609e6235e6de8fed25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455574"
---
# <a name="isautomaticforward"></a><span data-ttu-id="de897-103">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="de897-103">IsAutomaticForward</span></span>

<span data-ttu-id="de897-104">**IsAutomaticForward**元素指示传入的邮件是否必须自动转发，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="de897-104">The **IsAutomaticForward** element indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span> 
  
```XML
<IsAutomaticForward/> true | false</IsAutomaticForward>
```

 <span data-ttu-id="de897-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="de897-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de897-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="de897-106">Attributes and elements</span></span>

<span data-ttu-id="de897-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="de897-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de897-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="de897-108">Attributes</span></span>

<span data-ttu-id="de897-109">无。</span><span class="sxs-lookup"><span data-stu-id="de897-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de897-110">子元素</span><span class="sxs-lookup"><span data-stu-id="de897-110">Child elements</span></span>

<span data-ttu-id="de897-111">无。</span><span class="sxs-lookup"><span data-stu-id="de897-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="de897-112">父元素</span><span class="sxs-lookup"><span data-stu-id="de897-112">Parent elements</span></span>

|<span data-ttu-id="de897-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="de897-113">**Element**</span></span>|<span data-ttu-id="de897-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="de897-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de897-115">条件</span><span class="sxs-lookup"><span data-stu-id="de897-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="de897-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="de897-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="de897-117">异常</span><span class="sxs-lookup"><span data-stu-id="de897-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="de897-118">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="de897-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="de897-119">文本值</span><span class="sxs-lookup"><span data-stu-id="de897-119">Text value</span></span>

<span data-ttu-id="de897-120">如果文本值为**true** ，则表示该邮件必须为 "自动转发"，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="de897-120">A text value of **true** indicates that the message must be an automatic forward in order for the condition or exception to apply.</span></span> <span data-ttu-id="de897-121">如果值为**false** ，则表示邮件不得为自动转发，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="de897-121">A value of **false** indicates that the message must not be an automatic forward in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="de897-122">说明</span><span class="sxs-lookup"><span data-stu-id="de897-122">Remarks</span></span>

<span data-ttu-id="de897-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="de897-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de897-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="de897-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de897-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="de897-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="de897-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="de897-126">Schema Name</span></span>  <br/> |<span data-ttu-id="de897-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="de897-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="de897-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="de897-128">Validation File</span></span>  <br/> |<span data-ttu-id="de897-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="de897-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="de897-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="de897-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="de897-131">True</span><span class="sxs-lookup"><span data-stu-id="de897-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de897-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="de897-132">See also</span></span>



- [<span data-ttu-id="de897-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="de897-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

