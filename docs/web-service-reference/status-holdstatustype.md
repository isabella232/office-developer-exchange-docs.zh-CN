---
title: 状态 (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: Status 元素指定邮箱的保留状态。
ms.openlocfilehash: c40dc865d2b305ac86fa40d536e2d516a14260ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827579"
---
# <a name="status-holdstatustype"></a><span data-ttu-id="a5faa-103">状态 (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="a5faa-103">Status (HoldStatusType)</span></span>

<span data-ttu-id="a5faa-104">**Status**元素指定邮箱的保留状态。</span><span class="sxs-lookup"><span data-stu-id="a5faa-104">The **Status** element specifies the hold status for a mailbox.</span></span> 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 <span data-ttu-id="a5faa-105">**HoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="a5faa-105">**HoldStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a5faa-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a5faa-106">Attributes and elements</span></span>

<span data-ttu-id="a5faa-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a5faa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5faa-108">属性</span><span class="sxs-lookup"><span data-stu-id="a5faa-108">Attributes</span></span>

<span data-ttu-id="a5faa-109">无。</span><span class="sxs-lookup"><span data-stu-id="a5faa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5faa-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a5faa-110">Child elements</span></span>

<span data-ttu-id="a5faa-111">无。</span><span class="sxs-lookup"><span data-stu-id="a5faa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a5faa-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a5faa-112">Parent elements</span></span>

[<span data-ttu-id="a5faa-113">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="a5faa-113">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
  
## <a name="text-value"></a><span data-ttu-id="a5faa-114">文本值</span><span class="sxs-lookup"><span data-stu-id="a5faa-114">Text value</span></span>

<span data-ttu-id="a5faa-115">**Status**元素的文本值是邮箱的保留状态。</span><span class="sxs-lookup"><span data-stu-id="a5faa-115">The text value of the **Status** element is the hold status of a mailbox.</span></span> <span data-ttu-id="a5faa-116">**Status**元素可以具有以下列表中的值。</span><span class="sxs-lookup"><span data-stu-id="a5faa-116">The **Status** element can have the values in the following list.</span></span> 
  
> <span data-ttu-id="a5faa-117">NotOnHold-邮箱不是置于保持状态。</span><span class="sxs-lookup"><span data-stu-id="a5faa-117">NotOnHold - The mailbox is not on hold.</span></span>
    
> <span data-ttu-id="a5faa-118">挂起的邮箱是挂起正在发出或发布置于保持状态。</span><span class="sxs-lookup"><span data-stu-id="a5faa-118">Pending - The mailbox is pending either being placed or released on hold.</span></span> 
    
> <span data-ttu-id="a5faa-119">OnHold-保留已成功应用于邮箱。</span><span class="sxs-lookup"><span data-stu-id="a5faa-119">OnHold - The hold was successfully applied to the mailbox.</span></span> 
    
> <span data-ttu-id="a5faa-120">PartialHold-保留已成功应用到某些邮箱而不是为所有邮箱。</span><span class="sxs-lookup"><span data-stu-id="a5faa-120">PartialHold - The hold was successfully applied to some mailboxes but not to all mailboxes.</span></span>
    
> <span data-ttu-id="a5faa-121">保留项失败-未能应用于邮箱。</span><span class="sxs-lookup"><span data-stu-id="a5faa-121">Failed - The hold failed to apply to the mailbox.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5faa-122">备注</span><span class="sxs-lookup"><span data-stu-id="a5faa-122">Remarks</span></span>

<span data-ttu-id="a5faa-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a5faa-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a5faa-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a5faa-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5faa-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="a5faa-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5faa-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="a5faa-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a5faa-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="a5faa-127">Schema name</span></span>  <br/> |<span data-ttu-id="a5faa-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="a5faa-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="a5faa-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="a5faa-129">Validation file</span></span>  <br/> |<span data-ttu-id="a5faa-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a5faa-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a5faa-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="a5faa-131">Can be empty</span></span>  <br/> ||
   

