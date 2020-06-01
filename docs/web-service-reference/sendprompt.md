---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: SendPrompt 元素指定允许用于投票选项的操作类型。
ms.openlocfilehash: 98ffc69cdc94c3f7b9c325bee0c1ebaeb407ee96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462099"
---
# <a name="sendprompt"></a><span data-ttu-id="80b50-103">SendPrompt</span><span class="sxs-lookup"><span data-stu-id="80b50-103">SendPrompt</span></span>

<span data-ttu-id="80b50-104">**SendPrompt**元素指定允许用于投票选项的操作类型。</span><span class="sxs-lookup"><span data-stu-id="80b50-104">The **SendPrompt** element specifies the type of action allowed for a voting option.</span></span> 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 <span data-ttu-id="80b50-105">**SendPromptType**</span><span class="sxs-lookup"><span data-stu-id="80b50-105">**SendPromptType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80b50-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="80b50-106">Attributes and elements</span></span>

<span data-ttu-id="80b50-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="80b50-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80b50-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="80b50-108">Attributes</span></span>

<span data-ttu-id="80b50-109">无。</span><span class="sxs-lookup"><span data-stu-id="80b50-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80b50-110">子元素</span><span class="sxs-lookup"><span data-stu-id="80b50-110">Child elements</span></span>

<span data-ttu-id="80b50-111">无。</span><span class="sxs-lookup"><span data-stu-id="80b50-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="80b50-112">父元素</span><span class="sxs-lookup"><span data-stu-id="80b50-112">Parent elements</span></span>

[<span data-ttu-id="80b50-113">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="80b50-113">VotingOptionData</span></span>](votingoptiondata.md)
  
## <a name="text-value"></a><span data-ttu-id="80b50-114">文本值</span><span class="sxs-lookup"><span data-stu-id="80b50-114">Text value</span></span>

<span data-ttu-id="80b50-115">**SendPrompt**元素的文本值是投票选项操作。</span><span class="sxs-lookup"><span data-stu-id="80b50-115">The text value of the **SendPrompt** element is a voting option action.</span></span> <span data-ttu-id="80b50-116">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="80b50-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="80b50-117">**值**</span><span class="sxs-lookup"><span data-stu-id="80b50-117">**Value**</span></span>|<span data-ttu-id="80b50-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="80b50-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80b50-119">无</span><span class="sxs-lookup"><span data-stu-id="80b50-119">None</span></span>  <br/> |<span data-ttu-id="80b50-120">无操作。</span><span class="sxs-lookup"><span data-stu-id="80b50-120">No action.</span></span>  <br/> |
|<span data-ttu-id="80b50-121">发送</span><span class="sxs-lookup"><span data-stu-id="80b50-121">Send</span></span>  <br/> |<span data-ttu-id="80b50-122">将立即发送响应。</span><span class="sxs-lookup"><span data-stu-id="80b50-122">The response is sent immediately.</span></span>  <br/> |
|<span data-ttu-id="80b50-123">VotingOption</span><span class="sxs-lookup"><span data-stu-id="80b50-123">VotingOption</span></span>  <br/> |<span data-ttu-id="80b50-124">审批者可以在批准或拒绝时输入注释。</span><span class="sxs-lookup"><span data-stu-id="80b50-124">The approver can enter comments while approving or rejecting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80b50-125">说明</span><span class="sxs-lookup"><span data-stu-id="80b50-125">Remarks</span></span>

<span data-ttu-id="80b50-126">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="80b50-126">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="80b50-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="80b50-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80b50-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="80b50-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80b50-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="80b50-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="80b50-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="80b50-130">Schema Name</span></span>  <br/> |<span data-ttu-id="80b50-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="80b50-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="80b50-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="80b50-132">Validation File</span></span>  <br/> |<span data-ttu-id="80b50-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="80b50-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="80b50-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="80b50-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="80b50-135">True</span><span class="sxs-lookup"><span data-stu-id="80b50-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80b50-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80b50-136">See also</span></span>



[<span data-ttu-id="80b50-137">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="80b50-137">VotingOptionData</span></span>](votingoptiondata.md)


- [<span data-ttu-id="80b50-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="80b50-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

