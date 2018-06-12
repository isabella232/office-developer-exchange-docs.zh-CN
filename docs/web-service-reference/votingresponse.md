---
title: VotingResponse
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7dae4db5-28d3-4b81-b071-458c814c36b9
description: VotingResponse 元素指定提交的投票。 此元素是仅在投票请求邮件响应，不对 エ ・ 复 ハ 审批存在。
ms.openlocfilehash: 865b24a4f7ec1cc7b53d4928b04f071cddf5fbfc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838532"
---
# <a name="votingresponse"></a><span data-ttu-id="af856-104">VotingResponse</span><span class="sxs-lookup"><span data-stu-id="af856-104">VotingResponse</span></span>

<span data-ttu-id="af856-105">**VotingResponse**元素指定提交的投票。</span><span class="sxs-lookup"><span data-stu-id="af856-105">The **VotingResponse** element specifies the submitted vote.</span></span> <span data-ttu-id="af856-106">此元素是仅在投票请求邮件响应，不对 エ ・ 复 ハ 审批存在。</span><span class="sxs-lookup"><span data-stu-id="af856-106">This element is only present on responses to voting request messages, not on responses to approvals.</span></span> 
  
```XML
<VotingResponse />
```

 <span data-ttu-id="af856-107">**string**</span><span class="sxs-lookup"><span data-stu-id="af856-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af856-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="af856-108">Attributes and elements</span></span>

<span data-ttu-id="af856-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="af856-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af856-110">属性</span><span class="sxs-lookup"><span data-stu-id="af856-110">Attributes</span></span>

<span data-ttu-id="af856-111">无。</span><span class="sxs-lookup"><span data-stu-id="af856-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af856-112">子元素</span><span class="sxs-lookup"><span data-stu-id="af856-112">Child elements</span></span>

<span data-ttu-id="af856-113">无。</span><span class="sxs-lookup"><span data-stu-id="af856-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af856-114">父元素</span><span class="sxs-lookup"><span data-stu-id="af856-114">Parent elements</span></span>

[<span data-ttu-id="af856-115">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="af856-115">VotingInformation</span></span>](votinginformation.md)
  
## <a name="text-value"></a><span data-ttu-id="af856-116">文本值</span><span class="sxs-lookup"><span data-stu-id="af856-116">Text value</span></span>

<span data-ttu-id="af856-117">**VotingResponse**元素的文本值为提交投票。</span><span class="sxs-lookup"><span data-stu-id="af856-117">The text value of the **VotingResponse** element is the vote submitted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="af856-118">备注</span><span class="sxs-lookup"><span data-stu-id="af856-118">Remarks</span></span>

<span data-ttu-id="af856-119">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="af856-119">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="af856-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="af856-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af856-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="af856-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af856-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="af856-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af856-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="af856-123">Schema Name</span></span>  <br/> |<span data-ttu-id="af856-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="af856-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="af856-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="af856-125">Validation File</span></span>  <br/> |<span data-ttu-id="af856-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="af856-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af856-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="af856-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="af856-128">True</span><span class="sxs-lookup"><span data-stu-id="af856-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af856-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af856-129">See also</span></span>



[<span data-ttu-id="af856-130">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="af856-130">VotingInformation</span></span>](votinginformation.md)


- [<span data-ttu-id="af856-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="af856-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

