---
title: IsApprovalRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsApprovalRequest
api_type:
- schema
ms.assetid: 293ed01b-f6a4-4459-819c-933bbfaa2dd7
description: IsApprovalRequest 元素指示传入邮件是否必须审批请求中的条件或例外应用的顺序。
ms.openlocfilehash: 45b0836efff3ec9fe644cbaeb7ea7192346422bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825984"
---
# <a name="isapprovalrequest"></a><span data-ttu-id="ba9c0-103">IsApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="ba9c0-103">IsApprovalRequest</span></span>

<span data-ttu-id="ba9c0-104">**IsApprovalRequest**元素指示传入邮件是否必须审批请求中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="ba9c0-104">The **IsApprovalRequest** element indicates whether incoming messages must be approval requests in order for the condition or exception to apply.</span></span> 
  
```XML
<IsApprovalRequest/>
```

 <span data-ttu-id="ba9c0-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ba9c0-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba9c0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ba9c0-106">Attributes and elements</span></span>

<span data-ttu-id="ba9c0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ba9c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba9c0-108">属性</span><span class="sxs-lookup"><span data-stu-id="ba9c0-108">Attributes</span></span>

<span data-ttu-id="ba9c0-109">无。</span><span class="sxs-lookup"><span data-stu-id="ba9c0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba9c0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ba9c0-110">Child elements</span></span>

<span data-ttu-id="ba9c0-111">无。</span><span class="sxs-lookup"><span data-stu-id="ba9c0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba9c0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ba9c0-112">Parent elements</span></span>

|<span data-ttu-id="ba9c0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba9c0-113">**Element**</span></span>|<span data-ttu-id="ba9c0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba9c0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba9c0-115">条件</span><span class="sxs-lookup"><span data-stu-id="ba9c0-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="ba9c0-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="ba9c0-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="ba9c0-117">异常</span><span class="sxs-lookup"><span data-stu-id="ba9c0-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="ba9c0-118">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="ba9c0-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba9c0-119">文本值</span><span class="sxs-lookup"><span data-stu-id="ba9c0-119">Text value</span></span>

<span data-ttu-id="ba9c0-120">文本值为**true**指示邮件必须审批请求中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="ba9c0-120">A text value of **true** indicates that the message must be an approval request in order for the condition or exception to apply.</span></span> <span data-ttu-id="ba9c0-121">如果值为**false**指示邮件不得审批请求中的条件或例外应用的顺序。</span><span class="sxs-lookup"><span data-stu-id="ba9c0-121">A value of **false** indicates that the message must not be an approval request in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba9c0-122">备注</span><span class="sxs-lookup"><span data-stu-id="ba9c0-122">Remarks</span></span>

<span data-ttu-id="ba9c0-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ba9c0-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba9c0-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="ba9c0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba9c0-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="ba9c0-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ba9c0-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="ba9c0-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ba9c0-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="ba9c0-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ba9c0-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="ba9c0-128">Validation File</span></span>  <br/> |<span data-ttu-id="ba9c0-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ba9c0-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ba9c0-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="ba9c0-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba9c0-131">True</span><span class="sxs-lookup"><span data-stu-id="ba9c0-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba9c0-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ba9c0-132">See also</span></span>



- [<span data-ttu-id="ba9c0-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ba9c0-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

