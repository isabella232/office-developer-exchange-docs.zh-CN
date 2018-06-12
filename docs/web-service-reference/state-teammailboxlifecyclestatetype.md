---
title: 状态 (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: 状态元素包含对网站邮箱设置的生命周期状态。
ms.openlocfilehash: accd70d36cc34e7364387b98a2e94c56b91f012f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827571"
---
# <a name="state-teammailboxlifecyclestatetype"></a><span data-ttu-id="a3ec9-103">状态 (TeamMailboxLifecycleStateType)</span><span class="sxs-lookup"><span data-stu-id="a3ec9-103">State (TeamMailboxLifecycleStateType)</span></span>

<span data-ttu-id="a3ec9-104">**状态**元素包含对网站邮箱设置的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-104">The **State** element contains the lifecycle state that is set on a site mailbox.</span></span> 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

<span data-ttu-id="a3ec9-105">**TeamMailboxLifecycleStateType**</span><span class="sxs-lookup"><span data-stu-id="a3ec9-105">**TeamMailboxLifecycleStateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a3ec9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a3ec9-106">Attributes and elements</span></span>

<span data-ttu-id="a3ec9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3ec9-108">属性</span><span class="sxs-lookup"><span data-stu-id="a3ec9-108">Attributes</span></span>

<span data-ttu-id="a3ec9-109">无。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3ec9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a3ec9-110">Child elements</span></span>

<span data-ttu-id="a3ec9-111">无。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a3ec9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a3ec9-112">Parent elements</span></span>

[<span data-ttu-id="a3ec9-113">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="a3ec9-113">SetTeamMailbox</span></span>](setteammailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="a3ec9-114">文本值</span><span class="sxs-lookup"><span data-stu-id="a3ec9-114">Text value</span></span>

<span data-ttu-id="a3ec9-115">**状态**元素的文本值是站点邮箱设置的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-115">The text value of the **State** element is the lifecycle state that is set on a site mailbox.</span></span> <span data-ttu-id="a3ec9-116">**活动**的文本值指示站点邮箱正在使用中。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-116">A text value of **Active** indicates that a site mailbox is in active use.</span></span> <span data-ttu-id="a3ec9-117">**已关闭**文本值表示的站点邮箱已关闭，并不是正在使用中。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-117">A text value of **Closed** indicates that a site mailbox has been closed and is not in active use.</span></span> <span data-ttu-id="a3ec9-118">**未链接**文本值表示的站点邮箱不链接到的基于 web 的协作环境。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-118">A text value of **Unlinked** indicates that a site mailbox is not linked to a web-based collaboration environment.</span></span> <span data-ttu-id="a3ec9-119">**活动**、**已关闭**，和**PendingDelete**值都是互斥的但**未链接**值不互相互斥其他值。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-119">The **Active**, **Closed**, and **PendingDelete** values are mutually exclusive, but the **Unlinked** value is not mutually exclusive of the other values.</span></span> <span data-ttu-id="a3ec9-120">**PendingDelete**文本值指示站点邮箱当前删除未决。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-120">A text value of **PendingDelete** indicates that a site mailbox is pending deletion.</span></span> <span data-ttu-id="a3ec9-121">站点邮箱具有要关闭之前可以将其设置为**PendingDelete**。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-121">A site mailbox has to be closed before it can be set as **PendingDelete**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3ec9-122">备注</span><span class="sxs-lookup"><span data-stu-id="a3ec9-122">Remarks</span></span>

<span data-ttu-id="a3ec9-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a3ec9-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a3ec9-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3ec9-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="a3ec9-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3ec9-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="a3ec9-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a3ec9-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="a3ec9-127">Schema name</span></span>  <br/> |<span data-ttu-id="a3ec9-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="a3ec9-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a3ec9-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="a3ec9-129">Validation file</span></span>  <br/> |<span data-ttu-id="a3ec9-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a3ec9-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a3ec9-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="a3ec9-131">Can be empty</span></span>  <br/> ||
   

