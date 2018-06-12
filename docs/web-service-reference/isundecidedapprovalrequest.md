---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: IsUndecidedApprovalRequest 元素指定的审批请求邮件是否已作用于。
ms.openlocfilehash: 82b4624df5b2fe7ca212fdf76248e1ccfa3a081f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826127"
---
# <a name="isundecidedapprovalrequest"></a><span data-ttu-id="9fa32-103">IsUndecidedApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="9fa32-103">IsUndecidedApprovalRequest</span></span>

<span data-ttu-id="9fa32-104">**IsUndecidedApprovalRequest**元素指定的审批请求邮件是否已作用于。</span><span class="sxs-lookup"><span data-stu-id="9fa32-104">The **IsUndecidedApprovalRequest** element specifies whether an approval request message has been acted on.</span></span> 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 <span data-ttu-id="9fa32-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9fa32-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fa32-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9fa32-106">Attributes and elements</span></span>

<span data-ttu-id="9fa32-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9fa32-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fa32-108">属性</span><span class="sxs-lookup"><span data-stu-id="9fa32-108">Attributes</span></span>

<span data-ttu-id="9fa32-109">无。</span><span class="sxs-lookup"><span data-stu-id="9fa32-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fa32-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9fa32-110">Child elements</span></span>

<span data-ttu-id="9fa32-111">无。</span><span class="sxs-lookup"><span data-stu-id="9fa32-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9fa32-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9fa32-112">Parent elements</span></span>

[<span data-ttu-id="9fa32-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="9fa32-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="9fa32-114">文本值</span><span class="sxs-lookup"><span data-stu-id="9fa32-114">Text value</span></span>

<span data-ttu-id="9fa32-115">如果审批请求消息不作用于**IsUndecidedApprovalRequest**元素的文本值 **，则返回 true** 。</span><span class="sxs-lookup"><span data-stu-id="9fa32-115">The text value of the **IsUndecidedApprovalRequest** element is **true** if an approval request message has not been acted on.</span></span> <span data-ttu-id="9fa32-116">如果值为**false**指示审批请求，已决定。</span><span class="sxs-lookup"><span data-stu-id="9fa32-116">A value of **false** indicates that the approval request has been decided.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9fa32-117">备注</span><span class="sxs-lookup"><span data-stu-id="9fa32-117">Remarks</span></span>

<span data-ttu-id="9fa32-118">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9fa32-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="9fa32-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9fa32-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fa32-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="9fa32-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fa32-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="9fa32-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9fa32-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="9fa32-122">Schema Name</span></span>  <br/> |<span data-ttu-id="9fa32-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="9fa32-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="9fa32-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="9fa32-124">Validation File</span></span>  <br/> |<span data-ttu-id="9fa32-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9fa32-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9fa32-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="9fa32-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fa32-127">True</span><span class="sxs-lookup"><span data-stu-id="9fa32-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fa32-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9fa32-128">See also</span></span>



[<span data-ttu-id="9fa32-129">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="9fa32-129">ApprovalRequestData</span></span>](approvalrequestdata.md)


- [<span data-ttu-id="9fa32-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9fa32-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

