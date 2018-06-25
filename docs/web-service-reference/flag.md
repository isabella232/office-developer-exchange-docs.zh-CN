---
title: 标志
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b47bc74-a60d-4308-8674-5d52444a1753
description: 标志元素指定邮箱项目上的标志。
ms.openlocfilehash: f30f435e8f064d7165ae52de737bbd75b0546206
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754375"
---
# <a name="flag"></a><span data-ttu-id="99dcc-103">标志</span><span class="sxs-lookup"><span data-stu-id="99dcc-103">Flag</span></span>

<span data-ttu-id="99dcc-104">**标志**元素指定邮箱项目上的标志。</span><span class="sxs-lookup"><span data-stu-id="99dcc-104">The **Flag** element specifies a flag on a mailbox item.</span></span> 
  
```XML
<Flag>
    <FlagStatus/>
    <StartDate/>
    <DueDate/>
    <CompleteDate/>
</Flag>
```

 <span data-ttu-id="99dcc-105">**FlagType**</span><span class="sxs-lookup"><span data-stu-id="99dcc-105">**FlagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99dcc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="99dcc-106">Attributes and elements</span></span>

<span data-ttu-id="99dcc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="99dcc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99dcc-108">属性</span><span class="sxs-lookup"><span data-stu-id="99dcc-108">Attributes</span></span>

<span data-ttu-id="99dcc-109">无。</span><span class="sxs-lookup"><span data-stu-id="99dcc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99dcc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="99dcc-110">Child elements</span></span>

|<span data-ttu-id="99dcc-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="99dcc-111">**Element**</span></span>|<span data-ttu-id="99dcc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="99dcc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99dcc-113">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="99dcc-113">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="99dcc-114">包含当前文件夹中的项目的聚合的标志状态。</span><span class="sxs-lookup"><span data-stu-id="99dcc-114">Contains the aggregated flag status for items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="99dcc-115">StartDate</span><span class="sxs-lookup"><span data-stu-id="99dcc-115">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="99dcc-116">表示项目的开始日期。</span><span class="sxs-lookup"><span data-stu-id="99dcc-116">Represents the start date of an item.</span></span>  <br/> |
|[<span data-ttu-id="99dcc-117">DueDate</span><span class="sxs-lookup"><span data-stu-id="99dcc-117">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="99dcc-118">表示项目的到期日期。</span><span class="sxs-lookup"><span data-stu-id="99dcc-118">Represents the date when an item is due.</span></span>  <br/> |
|[<span data-ttu-id="99dcc-119">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="99dcc-119">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="99dcc-120">代表已完成项目的日期。</span><span class="sxs-lookup"><span data-stu-id="99dcc-120">Represents the date on which an item was completed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99dcc-121">父元素</span><span class="sxs-lookup"><span data-stu-id="99dcc-121">Parent elements</span></span>

|<span data-ttu-id="99dcc-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="99dcc-122">**Element**</span></span>|<span data-ttu-id="99dcc-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="99dcc-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99dcc-124">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="99dcc-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="99dcc-125">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="99dcc-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="99dcc-126">Item</span><span class="sxs-lookup"><span data-stu-id="99dcc-126">Item</span></span>](item.md) <br/> |<span data-ttu-id="99dcc-127">表示 Exchange 存储中的泛型项。</span><span class="sxs-lookup"><span data-stu-id="99dcc-127">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99dcc-128">备注</span><span class="sxs-lookup"><span data-stu-id="99dcc-128">Remarks</span></span>

<span data-ttu-id="99dcc-129">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="99dcc-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="99dcc-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="99dcc-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99dcc-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="99dcc-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99dcc-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="99dcc-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="99dcc-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="99dcc-133">Schema Name</span></span>  <br/> |<span data-ttu-id="99dcc-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="99dcc-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="99dcc-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="99dcc-135">Validation File</span></span>  <br/> |<span data-ttu-id="99dcc-136">types.xsd</span><span class="sxs-lookup"><span data-stu-id="99dcc-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="99dcc-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="99dcc-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="99dcc-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="99dcc-138">See also</span></span>



- [<span data-ttu-id="99dcc-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="99dcc-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

