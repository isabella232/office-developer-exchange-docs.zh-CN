---
title: 状态（HoldStatusType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: Status 元素指定邮箱的保留状态。
ms.openlocfilehash: cecfdfaf67b00b6f8cf02188e7a4df7062a732e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459985"
---
# <a name="status-holdstatustype"></a><span data-ttu-id="351c5-103">状态（HoldStatusType）</span><span class="sxs-lookup"><span data-stu-id="351c5-103">Status (HoldStatusType)</span></span>

<span data-ttu-id="351c5-104">**Status**元素指定邮箱的保留状态。</span><span class="sxs-lookup"><span data-stu-id="351c5-104">The **Status** element specifies the hold status for a mailbox.</span></span> 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 <span data-ttu-id="351c5-105">**HoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="351c5-105">**HoldStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="351c5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="351c5-106">Attributes and elements</span></span>

<span data-ttu-id="351c5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="351c5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="351c5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="351c5-108">Attributes</span></span>

<span data-ttu-id="351c5-109">无。</span><span class="sxs-lookup"><span data-stu-id="351c5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="351c5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="351c5-110">Child elements</span></span>

<span data-ttu-id="351c5-111">无。</span><span class="sxs-lookup"><span data-stu-id="351c5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="351c5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="351c5-112">Parent elements</span></span>

[<span data-ttu-id="351c5-113">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="351c5-113">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
  
## <a name="text-value"></a><span data-ttu-id="351c5-114">文本值</span><span class="sxs-lookup"><span data-stu-id="351c5-114">Text value</span></span>

<span data-ttu-id="351c5-115">**Status**元素的文本值是邮箱的保留状态。</span><span class="sxs-lookup"><span data-stu-id="351c5-115">The text value of the **Status** element is the hold status of a mailbox.</span></span> <span data-ttu-id="351c5-116">**Status**元素的值可以是下表中的值。</span><span class="sxs-lookup"><span data-stu-id="351c5-116">The **Status** element can have the values in the following list.</span></span> 
  
> <span data-ttu-id="351c5-117">NotOnHold-邮箱未处于保留状态。</span><span class="sxs-lookup"><span data-stu-id="351c5-117">NotOnHold - The mailbox is not on hold.</span></span>
    
> <span data-ttu-id="351c5-118">待处理-邮箱挂起或处于保留状态。</span><span class="sxs-lookup"><span data-stu-id="351c5-118">Pending - The mailbox is pending either being placed or released on hold.</span></span> 
    
> <span data-ttu-id="351c5-119">OnHold-已成功将保留应用到邮箱。</span><span class="sxs-lookup"><span data-stu-id="351c5-119">OnHold - The hold was successfully applied to the mailbox.</span></span> 
    
> <span data-ttu-id="351c5-120">PartialHold-已成功将保留应用于某些邮箱，而不是所有邮箱。</span><span class="sxs-lookup"><span data-stu-id="351c5-120">PartialHold - The hold was successfully applied to some mailboxes but not to all mailboxes.</span></span>
    
> <span data-ttu-id="351c5-121">失败-保留无法应用于邮箱。</span><span class="sxs-lookup"><span data-stu-id="351c5-121">Failed - The hold failed to apply to the mailbox.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="351c5-122">备注</span><span class="sxs-lookup"><span data-stu-id="351c5-122">Remarks</span></span>

<span data-ttu-id="351c5-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="351c5-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="351c5-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="351c5-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="351c5-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="351c5-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="351c5-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="351c5-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="351c5-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="351c5-127">Schema name</span></span>  <br/> |<span data-ttu-id="351c5-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="351c5-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="351c5-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="351c5-129">Validation file</span></span>  <br/> |<span data-ttu-id="351c5-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="351c5-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="351c5-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="351c5-131">Can be empty</span></span>  <br/> ||
   

