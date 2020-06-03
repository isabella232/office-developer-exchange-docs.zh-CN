---
title: VotingResponse
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7dae4db5-28d3-4b81-b071-458c814c36b9
description: VotingResponse 元素指定提交的投票。 此元素只显示对投票请求邮件的响应，而不是对审批的响应。
ms.openlocfilehash: ed7caff79d1ff2946800630c167350fe866e29dc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466463"
---
# <a name="votingresponse"></a><span data-ttu-id="70423-104">VotingResponse</span><span class="sxs-lookup"><span data-stu-id="70423-104">VotingResponse</span></span>

<span data-ttu-id="70423-105">**VotingResponse**元素指定提交的投票。</span><span class="sxs-lookup"><span data-stu-id="70423-105">The **VotingResponse** element specifies the submitted vote.</span></span> <span data-ttu-id="70423-106">此元素只显示对投票请求邮件的响应，而不是对审批的响应。</span><span class="sxs-lookup"><span data-stu-id="70423-106">This element is only present on responses to voting request messages, not on responses to approvals.</span></span> 
  
```XML
<VotingResponse />
```

 <span data-ttu-id="70423-107">**string**</span><span class="sxs-lookup"><span data-stu-id="70423-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70423-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="70423-108">Attributes and elements</span></span>

<span data-ttu-id="70423-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="70423-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70423-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="70423-110">Attributes</span></span>

<span data-ttu-id="70423-111">无。</span><span class="sxs-lookup"><span data-stu-id="70423-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70423-112">子元素</span><span class="sxs-lookup"><span data-stu-id="70423-112">Child elements</span></span>

<span data-ttu-id="70423-113">无。</span><span class="sxs-lookup"><span data-stu-id="70423-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="70423-114">父元素</span><span class="sxs-lookup"><span data-stu-id="70423-114">Parent elements</span></span>

[<span data-ttu-id="70423-115">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="70423-115">VotingInformation</span></span>](votinginformation.md)
  
## <a name="text-value"></a><span data-ttu-id="70423-116">文本值</span><span class="sxs-lookup"><span data-stu-id="70423-116">Text value</span></span>

<span data-ttu-id="70423-117">**VotingResponse**元素的文本值是提交的投票。</span><span class="sxs-lookup"><span data-stu-id="70423-117">The text value of the **VotingResponse** element is the vote submitted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="70423-118">说明</span><span class="sxs-lookup"><span data-stu-id="70423-118">Remarks</span></span>

<span data-ttu-id="70423-119">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="70423-119">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="70423-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="70423-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70423-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="70423-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70423-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="70423-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70423-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="70423-123">Schema Name</span></span>  <br/> |<span data-ttu-id="70423-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="70423-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="70423-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="70423-125">Validation File</span></span>  <br/> |<span data-ttu-id="70423-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="70423-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="70423-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="70423-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="70423-128">True</span><span class="sxs-lookup"><span data-stu-id="70423-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70423-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70423-129">See also</span></span>



[<span data-ttu-id="70423-130">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="70423-130">VotingInformation</span></span>](votinginformation.md)


- [<span data-ttu-id="70423-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="70423-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

