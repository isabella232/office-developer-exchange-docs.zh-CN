---
title: IsNDR
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNDR
api_type:
- schema
ms.assetid: 194f5836-7793-463a-a090-4386d1c2487a
description: IsNDR 元素指示传入的邮件是否必须为未送达报告（Ndr），以便条件或例外情况适用。
ms.openlocfilehash: 3476331ccece347686b7f98edf49df5d48b8562e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458157"
---
# <a name="isndr"></a><span data-ttu-id="34783-103">IsNDR</span><span class="sxs-lookup"><span data-stu-id="34783-103">IsNDR</span></span>

<span data-ttu-id="34783-104">**IsNDR**元素指示传入的邮件是否必须为未送达报告（ndr），以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="34783-104">The **IsNDR** element indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsNDR>true | false</IsNDR>
```

 <span data-ttu-id="34783-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="34783-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34783-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="34783-106">Attributes and elements</span></span>

<span data-ttu-id="34783-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="34783-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34783-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="34783-108">Attributes</span></span>

<span data-ttu-id="34783-109">无。</span><span class="sxs-lookup"><span data-stu-id="34783-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34783-110">子元素</span><span class="sxs-lookup"><span data-stu-id="34783-110">Child elements</span></span>

<span data-ttu-id="34783-111">无。</span><span class="sxs-lookup"><span data-stu-id="34783-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="34783-112">父元素</span><span class="sxs-lookup"><span data-stu-id="34783-112">Parent elements</span></span>

|<span data-ttu-id="34783-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="34783-113">**Element**</span></span>|<span data-ttu-id="34783-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="34783-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34783-115">条件</span><span class="sxs-lookup"><span data-stu-id="34783-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="34783-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="34783-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="34783-117">异常</span><span class="sxs-lookup"><span data-stu-id="34783-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="34783-118">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="34783-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="34783-119">文本值</span><span class="sxs-lookup"><span data-stu-id="34783-119">Text value</span></span>

<span data-ttu-id="34783-120">如果文本值为**true** ，则表示邮件必须为 NDR，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="34783-120">A text value of **true** indicates that the message must be an NDR in order for the condition or exception to apply.</span></span> <span data-ttu-id="34783-121">如果值为**false** ，则表示邮件不得为 NDR，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="34783-121">A value of **false** indicates that the message must not be an NDR in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="34783-122">说明</span><span class="sxs-lookup"><span data-stu-id="34783-122">Remarks</span></span>

<span data-ttu-id="34783-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="34783-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34783-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="34783-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34783-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="34783-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="34783-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="34783-126">Schema Name</span></span>  <br/> |<span data-ttu-id="34783-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="34783-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="34783-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="34783-128">Validation File</span></span>  <br/> |<span data-ttu-id="34783-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="34783-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="34783-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="34783-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="34783-131">True</span><span class="sxs-lookup"><span data-stu-id="34783-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34783-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="34783-132">See also</span></span>



- [<span data-ttu-id="34783-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="34783-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

