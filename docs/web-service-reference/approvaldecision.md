---
title: ApprovalDecision
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5e7c5687-cb9e-4f0b-ac8f-b82591914a39
description: ApprovalDecision 元素指定在审批请求邮件上做出的决定。
ms.openlocfilehash: a8dc168edec882ba97cdea764f8d20c71ed85f8a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463445"
---
# <a name="approvaldecision"></a><span data-ttu-id="3414b-103">ApprovalDecision</span><span class="sxs-lookup"><span data-stu-id="3414b-103">ApprovalDecision</span></span>

<span data-ttu-id="3414b-104">**ApprovalDecision**元素指定在审批请求邮件上做出的决定。</span><span class="sxs-lookup"><span data-stu-id="3414b-104">The **ApprovalDecision** element specifies the decision made on an approval request message.</span></span> 
  
```XML
<ApprovalDecision> 1 | 2 </ApprovalDecision>
```

 <span data-ttu-id="3414b-105">**int**</span><span class="sxs-lookup"><span data-stu-id="3414b-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3414b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3414b-106">Attributes and elements</span></span>

<span data-ttu-id="3414b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3414b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3414b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3414b-108">Attributes</span></span>

<span data-ttu-id="3414b-109">无。</span><span class="sxs-lookup"><span data-stu-id="3414b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3414b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3414b-110">Child elements</span></span>

<span data-ttu-id="3414b-111">无。</span><span class="sxs-lookup"><span data-stu-id="3414b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3414b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3414b-112">Parent elements</span></span>

[<span data-ttu-id="3414b-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="3414b-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="3414b-114">文本值</span><span class="sxs-lookup"><span data-stu-id="3414b-114">Text value</span></span>

<span data-ttu-id="3414b-115">**ApprovalDecision**元素的文本值为1（如果已批准），如果被拒绝，则为2。</span><span class="sxs-lookup"><span data-stu-id="3414b-115">The text value of the **ApprovalDecision** element is 1 if approved and 2 if rejected.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3414b-116">说明</span><span class="sxs-lookup"><span data-stu-id="3414b-116">Remarks</span></span>

<span data-ttu-id="3414b-117">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3414b-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="3414b-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3414b-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3414b-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="3414b-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3414b-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="3414b-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3414b-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="3414b-121">Schema Name</span></span>  <br/> |<span data-ttu-id="3414b-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="3414b-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="3414b-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="3414b-123">Validation File</span></span>  <br/> |<span data-ttu-id="3414b-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3414b-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3414b-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="3414b-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="3414b-126">True</span><span class="sxs-lookup"><span data-stu-id="3414b-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3414b-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3414b-127">See also</span></span>

- [<span data-ttu-id="3414b-128">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="3414b-128">ApprovalRequestData</span></span>](approvalrequestdata.md)
- [<span data-ttu-id="3414b-129">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3414b-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

