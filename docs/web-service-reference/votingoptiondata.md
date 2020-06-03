---
title: VotingOptionData
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 387328ae-4dcc-4230-8e4b-01d7894bbce2
description: VotingOptionData 元素指定有关每个投票选项的信息。
ms.openlocfilehash: f4240dc5c5d88e4964087b80e9081b93b41eed94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468647"
---
# <a name="votingoptiondata"></a><span data-ttu-id="1a1cb-103">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="1a1cb-103">VotingOptionData</span></span>

<span data-ttu-id="1a1cb-104">**VotingOptionData**元素指定有关每个投票选项的信息。</span><span class="sxs-lookup"><span data-stu-id="1a1cb-104">The **VotingOptionData** element specifies information about each voting option.</span></span> 
  
```XML
<VotingOptionData>
   <DisplayName/>
   <SendPrompt/>
</VotingOptionData>
```

 <span data-ttu-id="1a1cb-105">**VotingOptionDataType**</span><span class="sxs-lookup"><span data-stu-id="1a1cb-105">**VotingOptionDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a1cb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1a1cb-106">Attributes and elements</span></span>

<span data-ttu-id="1a1cb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1a1cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a1cb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1a1cb-108">Attributes</span></span>

<span data-ttu-id="1a1cb-109">无。</span><span class="sxs-lookup"><span data-stu-id="1a1cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a1cb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1a1cb-110">Child elements</span></span>

<span data-ttu-id="1a1cb-111">[DisplayName （VotingOptionDataType）](displayname-votingoptiondatatype.md)  | [SendPrompt](sendprompt.md)</span><span class="sxs-lookup"><span data-stu-id="1a1cb-111">[DisplayName (VotingOptionDataType)](displayname-votingoptiondatatype.md) | [SendPrompt](sendprompt.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1a1cb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1a1cb-112">Parent elements</span></span>

[<span data-ttu-id="1a1cb-113">UserOptions</span><span class="sxs-lookup"><span data-stu-id="1a1cb-113">UserOptions</span></span>](useroptions.md)
  
## <a name="remarks"></a><span data-ttu-id="1a1cb-114">说明</span><span class="sxs-lookup"><span data-stu-id="1a1cb-114">Remarks</span></span>

<span data-ttu-id="1a1cb-115">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1a1cb-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="1a1cb-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1a1cb-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a1cb-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1a1cb-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a1cb-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1a1cb-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1a1cb-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1a1cb-119">Schema Name</span></span>  <br/> |<span data-ttu-id="1a1cb-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="1a1cb-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1a1cb-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1a1cb-121">Validation File</span></span>  <br/> |<span data-ttu-id="1a1cb-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1a1cb-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1a1cb-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1a1cb-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="1a1cb-124">True</span><span class="sxs-lookup"><span data-stu-id="1a1cb-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a1cb-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1a1cb-125">See also</span></span>



[<span data-ttu-id="1a1cb-126">UserOptions</span><span class="sxs-lookup"><span data-stu-id="1a1cb-126">UserOptions</span></span>](useroptions.md)


- [<span data-ttu-id="1a1cb-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1a1cb-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

