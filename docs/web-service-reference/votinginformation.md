---
title: VotingInformation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: VotingInformation 元素指定投票邮件和审批请求邮件 whereApproveandRejectare 投票选项的投票信息。
ms.openlocfilehash: d946ba8c71d19c8cbb1befbe8c4e43e93590ccae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467744"
---
# <a name="votinginformation"></a><span data-ttu-id="4b31d-103">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="4b31d-103">VotingInformation</span></span>

<span data-ttu-id="4b31d-104">**VotingInformation**元素指定投票邮件和审批请求邮件中的投票信息，其中 "批准" 和 "拒绝" 是投票选项。</span><span class="sxs-lookup"><span data-stu-id="4b31d-104">The **VotingInformation** element specifies voting information on a voting message and approval request message where "Approve" and "Reject" are the voting options.</span></span> 
  
```XML
<VotingInformation
   <UserOptions/>
   <VotingResponse/>
</VotingInformation>
```

 <span data-ttu-id="4b31d-105">**VotingInformationType**</span><span class="sxs-lookup"><span data-stu-id="4b31d-105">**VotingInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4b31d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4b31d-106">Attributes and elements</span></span>

<span data-ttu-id="4b31d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4b31d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b31d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4b31d-108">Attributes</span></span>

<span data-ttu-id="4b31d-109">无。</span><span class="sxs-lookup"><span data-stu-id="4b31d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b31d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4b31d-110">Child elements</span></span>

<span data-ttu-id="4b31d-111">[UserOptions](useroptions.md)  | [VotingResponse](votingresponse.md)</span><span class="sxs-lookup"><span data-stu-id="4b31d-111">[UserOptions](useroptions.md) | [VotingResponse](votingresponse.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4b31d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4b31d-112">Parent elements</span></span>

[<span data-ttu-id="4b31d-113">邮件</span><span class="sxs-lookup"><span data-stu-id="4b31d-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="4b31d-114">说明</span><span class="sxs-lookup"><span data-stu-id="4b31d-114">Remarks</span></span>

<span data-ttu-id="4b31d-115">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4b31d-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="4b31d-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4b31d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b31d-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="4b31d-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b31d-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="4b31d-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4b31d-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="4b31d-119">Schema Name</span></span>  <br/> |<span data-ttu-id="4b31d-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="4b31d-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="4b31d-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="4b31d-121">Validation File</span></span>  <br/> |<span data-ttu-id="4b31d-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4b31d-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4b31d-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="4b31d-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b31d-124">True</span><span class="sxs-lookup"><span data-stu-id="4b31d-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b31d-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b31d-125">See also</span></span>



[<span data-ttu-id="4b31d-126">邮件</span><span class="sxs-lookup"><span data-stu-id="4b31d-126">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="4b31d-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4b31d-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

