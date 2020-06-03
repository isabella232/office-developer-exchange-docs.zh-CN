---
title: State （TeamMailboxLifecycleStateType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: State 元素包含在网站邮箱上设置的生命周期状态。
ms.openlocfilehash: 597946b48649d997f8dd57823b4e0fcc091a6f84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465161"
---
# <a name="state-teammailboxlifecyclestatetype"></a><span data-ttu-id="e068a-103">State （TeamMailboxLifecycleStateType）</span><span class="sxs-lookup"><span data-stu-id="e068a-103">State (TeamMailboxLifecycleStateType)</span></span>

<span data-ttu-id="e068a-104">**State**元素包含在网站邮箱上设置的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="e068a-104">The **State** element contains the lifecycle state that is set on a site mailbox.</span></span> 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

<span data-ttu-id="e068a-105">**TeamMailboxLifecycleStateType**</span><span class="sxs-lookup"><span data-stu-id="e068a-105">**TeamMailboxLifecycleStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e068a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e068a-106">Attributes and elements</span></span>

<span data-ttu-id="e068a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e068a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e068a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e068a-108">Attributes</span></span>

<span data-ttu-id="e068a-109">无。</span><span class="sxs-lookup"><span data-stu-id="e068a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e068a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e068a-110">Child elements</span></span>

<span data-ttu-id="e068a-111">无。</span><span class="sxs-lookup"><span data-stu-id="e068a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e068a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e068a-112">Parent elements</span></span>

[<span data-ttu-id="e068a-113">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="e068a-113">SetTeamMailbox</span></span>](setteammailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="e068a-114">文本值</span><span class="sxs-lookup"><span data-stu-id="e068a-114">Text value</span></span>

<span data-ttu-id="e068a-115">**State**元素的文本值是在网站邮箱上设置的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="e068a-115">The text value of the **State** element is the lifecycle state that is set on a site mailbox.</span></span> <span data-ttu-id="e068a-116">**活动**的文本值表示网站邮箱处于活动使用状态。</span><span class="sxs-lookup"><span data-stu-id="e068a-116">A text value of **Active** indicates that a site mailbox is in active use.</span></span> <span data-ttu-id="e068a-117">"**已关闭**" 文本值表示网站邮箱已关闭，未处于活动使用状态。</span><span class="sxs-lookup"><span data-stu-id="e068a-117">A text value of **Closed** indicates that a site mailbox has been closed and is not in active use.</span></span> <span data-ttu-id="e068a-118">未**链接**的文本值表示网站邮箱未链接到基于 web 的协作环境。</span><span class="sxs-lookup"><span data-stu-id="e068a-118">A text value of **Unlinked** indicates that a site mailbox is not linked to a web-based collaboration environment.</span></span> <span data-ttu-id="e068a-119">**活动**、**闭合**和**PendingDelete**值是互斥的，但未**链接**的值不与其他值互斥。</span><span class="sxs-lookup"><span data-stu-id="e068a-119">The **Active**, **Closed**, and **PendingDelete** values are mutually exclusive, but the **Unlinked** value is not mutually exclusive of the other values.</span></span> <span data-ttu-id="e068a-120">文本值为**PendingDelete**表示网站邮箱正在等待删除。</span><span class="sxs-lookup"><span data-stu-id="e068a-120">A text value of **PendingDelete** indicates that a site mailbox is pending deletion.</span></span> <span data-ttu-id="e068a-121">必须先关闭网站邮箱，然后才能将其设置为**PendingDelete**。</span><span class="sxs-lookup"><span data-stu-id="e068a-121">A site mailbox has to be closed before it can be set as **PendingDelete**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e068a-122">备注</span><span class="sxs-lookup"><span data-stu-id="e068a-122">Remarks</span></span>

<span data-ttu-id="e068a-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e068a-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e068a-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e068a-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e068a-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="e068a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e068a-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="e068a-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e068a-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="e068a-127">Schema name</span></span>  <br/> |<span data-ttu-id="e068a-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="e068a-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e068a-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="e068a-129">Validation file</span></span>  <br/> |<span data-ttu-id="e068a-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e068a-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e068a-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="e068a-131">Can be empty</span></span>  <br/> ||
   

