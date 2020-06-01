---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: IsUndecidedApprovalRequest 元素指定是否已对审批请求邮件执行操作。
ms.openlocfilehash: 0949cf64b8583c4b3fa5a1700475f01cc480f69f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458171"
---
# <a name="isundecidedapprovalrequest"></a><span data-ttu-id="cd298-103">IsUndecidedApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="cd298-103">IsUndecidedApprovalRequest</span></span>

<span data-ttu-id="cd298-104">**IsUndecidedApprovalRequest**元素指定是否已对审批请求邮件执行操作。</span><span class="sxs-lookup"><span data-stu-id="cd298-104">The **IsUndecidedApprovalRequest** element specifies whether an approval request message has been acted on.</span></span> 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 <span data-ttu-id="cd298-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cd298-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd298-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cd298-106">Attributes and elements</span></span>

<span data-ttu-id="cd298-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd298-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd298-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cd298-108">Attributes</span></span>

<span data-ttu-id="cd298-109">无。</span><span class="sxs-lookup"><span data-stu-id="cd298-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd298-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cd298-110">Child elements</span></span>

<span data-ttu-id="cd298-111">无。</span><span class="sxs-lookup"><span data-stu-id="cd298-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd298-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cd298-112">Parent elements</span></span>

[<span data-ttu-id="cd298-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="cd298-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="cd298-114">文本值</span><span class="sxs-lookup"><span data-stu-id="cd298-114">Text value</span></span>

<span data-ttu-id="cd298-115">如果尚未处理审批请求邮件，则**IsUndecidedApprovalRequest**元素的文本值为**true** 。</span><span class="sxs-lookup"><span data-stu-id="cd298-115">The text value of the **IsUndecidedApprovalRequest** element is **true** if an approval request message has not been acted on.</span></span> <span data-ttu-id="cd298-116">**如果值为 false** ，则表示已决定批准请求。</span><span class="sxs-lookup"><span data-stu-id="cd298-116">A value of **false** indicates that the approval request has been decided.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cd298-117">说明</span><span class="sxs-lookup"><span data-stu-id="cd298-117">Remarks</span></span>

<span data-ttu-id="cd298-118">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cd298-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="cd298-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cd298-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd298-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="cd298-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd298-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="cd298-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cd298-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="cd298-122">Schema Name</span></span>  <br/> |<span data-ttu-id="cd298-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="cd298-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="cd298-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="cd298-124">Validation File</span></span>  <br/> |<span data-ttu-id="cd298-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cd298-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cd298-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="cd298-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd298-127">True</span><span class="sxs-lookup"><span data-stu-id="cd298-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd298-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cd298-128">See also</span></span>



[<span data-ttu-id="cd298-129">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="cd298-129">ApprovalRequestData</span></span>](approvalrequestdata.md)


- [<span data-ttu-id="cd298-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cd298-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

