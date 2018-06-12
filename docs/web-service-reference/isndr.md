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
description: IsNDR 元素指示传入邮件是否必须以未送达报告 (Ndr) 中的条件或例外应用的顺序。
ms.openlocfilehash: 651590d055a0532c904dbf6c481dca2f899d673f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826056"
---
# <a name="isndr"></a><span data-ttu-id="8f4ea-103">IsNDR</span><span class="sxs-lookup"><span data-stu-id="8f4ea-103">IsNDR</span></span>

<span data-ttu-id="8f4ea-104">**IsNDR**元素指示传入邮件是否必须以未送达报告 (Ndr) 中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="8f4ea-104">The **IsNDR** element indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsNDR>true | false</IsNDR>
```

 <span data-ttu-id="8f4ea-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f4ea-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8f4ea-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8f4ea-106">Attributes and elements</span></span>

<span data-ttu-id="8f4ea-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8f4ea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8f4ea-108">属性</span><span class="sxs-lookup"><span data-stu-id="8f4ea-108">Attributes</span></span>

<span data-ttu-id="8f4ea-109">无。</span><span class="sxs-lookup"><span data-stu-id="8f4ea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8f4ea-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8f4ea-110">Child elements</span></span>

<span data-ttu-id="8f4ea-111">无。</span><span class="sxs-lookup"><span data-stu-id="8f4ea-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8f4ea-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8f4ea-112">Parent elements</span></span>

|<span data-ttu-id="8f4ea-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8f4ea-113">**Element**</span></span>|<span data-ttu-id="8f4ea-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8f4ea-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f4ea-115">条件</span><span class="sxs-lookup"><span data-stu-id="8f4ea-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="8f4ea-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="8f4ea-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="8f4ea-117">异常</span><span class="sxs-lookup"><span data-stu-id="8f4ea-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="8f4ea-118">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="8f4ea-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8f4ea-119">文本值</span><span class="sxs-lookup"><span data-stu-id="8f4ea-119">Text value</span></span>

<span data-ttu-id="8f4ea-120">文本值为**true**指示邮件必须 NDR 中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="8f4ea-120">A text value of **true** indicates that the message must be an NDR in order for the condition or exception to apply.</span></span> <span data-ttu-id="8f4ea-121">如果值为**false**指示邮件不得 NDR 中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="8f4ea-121">A value of **false** indicates that the message must not be an NDR in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8f4ea-122">备注</span><span class="sxs-lookup"><span data-stu-id="8f4ea-122">Remarks</span></span>

<span data-ttu-id="8f4ea-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8f4ea-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f4ea-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="8f4ea-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f4ea-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="8f4ea-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8f4ea-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="8f4ea-126">Schema Name</span></span>  <br/> |<span data-ttu-id="8f4ea-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="8f4ea-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8f4ea-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="8f4ea-128">Validation File</span></span>  <br/> |<span data-ttu-id="8f4ea-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8f4ea-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8f4ea-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="8f4ea-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="8f4ea-131">True</span><span class="sxs-lookup"><span data-stu-id="8f4ea-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8f4ea-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8f4ea-132">See also</span></span>



- [<span data-ttu-id="8f4ea-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8f4ea-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

