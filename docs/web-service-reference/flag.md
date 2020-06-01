---
title: 指示
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b47bc74-a60d-4308-8674-5d52444a1753
description: Flag 元素指定邮箱项目的标志。
ms.openlocfilehash: 7229a26181ee9baf80be5c32c0ef99483310ccb3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466260"
---
# <a name="flag"></a><span data-ttu-id="8742e-103">指示</span><span class="sxs-lookup"><span data-stu-id="8742e-103">Flag</span></span>

<span data-ttu-id="8742e-104">**Flag**元素指定邮箱项目的标志。</span><span class="sxs-lookup"><span data-stu-id="8742e-104">The **Flag** element specifies a flag on a mailbox item.</span></span> 
  
```XML
<Flag>
    <FlagStatus/>
    <StartDate/>
    <DueDate/>
    <CompleteDate/>
</Flag>
```

 <span data-ttu-id="8742e-105">**FlagType**</span><span class="sxs-lookup"><span data-stu-id="8742e-105">**FlagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8742e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8742e-106">Attributes and elements</span></span>

<span data-ttu-id="8742e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8742e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8742e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8742e-108">Attributes</span></span>

<span data-ttu-id="8742e-109">无。</span><span class="sxs-lookup"><span data-stu-id="8742e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8742e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8742e-110">Child elements</span></span>

|<span data-ttu-id="8742e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8742e-111">**Element**</span></span>|<span data-ttu-id="8742e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8742e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8742e-113">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="8742e-113">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="8742e-114">包含当前文件夹中的项目的汇总标志状态。</span><span class="sxs-lookup"><span data-stu-id="8742e-114">Contains the aggregated flag status for items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="8742e-115">StartDate</span><span class="sxs-lookup"><span data-stu-id="8742e-115">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="8742e-116">表示项目的开始日期。</span><span class="sxs-lookup"><span data-stu-id="8742e-116">Represents the start date of an item.</span></span>  <br/> |
|[<span data-ttu-id="8742e-117">DueDate</span><span class="sxs-lookup"><span data-stu-id="8742e-117">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="8742e-118">表示项目的截止日期。</span><span class="sxs-lookup"><span data-stu-id="8742e-118">Represents the date when an item is due.</span></span>  <br/> |
|[<span data-ttu-id="8742e-119">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="8742e-119">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="8742e-120">表示项目完成的日期。</span><span class="sxs-lookup"><span data-stu-id="8742e-120">Represents the date on which an item was completed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8742e-121">父元素</span><span class="sxs-lookup"><span data-stu-id="8742e-121">Parent elements</span></span>

|<span data-ttu-id="8742e-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="8742e-122">**Element**</span></span>|<span data-ttu-id="8742e-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="8742e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8742e-124">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="8742e-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="8742e-125">包含要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="8742e-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="8742e-126">项</span><span class="sxs-lookup"><span data-stu-id="8742e-126">Item</span></span>](item.md) <br/> |<span data-ttu-id="8742e-127">表示 Exchange 存储中的一般项目。</span><span class="sxs-lookup"><span data-stu-id="8742e-127">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8742e-128">备注</span><span class="sxs-lookup"><span data-stu-id="8742e-128">Remarks</span></span>

<span data-ttu-id="8742e-129">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8742e-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8742e-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8742e-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8742e-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="8742e-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8742e-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="8742e-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8742e-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="8742e-133">Schema Name</span></span>  <br/> |<span data-ttu-id="8742e-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="8742e-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="8742e-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="8742e-135">Validation File</span></span>  <br/> |<span data-ttu-id="8742e-136">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="8742e-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8742e-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="8742e-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8742e-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8742e-138">See also</span></span>



- [<span data-ttu-id="8742e-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8742e-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

