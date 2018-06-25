---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: RetentionAction 元素指定与保留标记的项上执行的操作。
ms.openlocfilehash: 54a1038f2e56aad66f89522423ccfbd69dc44a80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827215"
---
# <a name="retentionaction"></a><span data-ttu-id="ec289-103">RetentionAction</span><span class="sxs-lookup"><span data-stu-id="ec289-103">RetentionAction</span></span>

<span data-ttu-id="ec289-104">**RetentionAction**元素指定与保留标记的项上执行的操作。</span><span class="sxs-lookup"><span data-stu-id="ec289-104">The **RetentionAction** element specifies the action performed on items with the retention tag.</span></span> 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 <span data-ttu-id="ec289-105">**RetentionActionType**</span><span class="sxs-lookup"><span data-stu-id="ec289-105">**RetentionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec289-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ec289-106">Attributes and elements</span></span>

<span data-ttu-id="ec289-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ec289-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec289-108">属性</span><span class="sxs-lookup"><span data-stu-id="ec289-108">Attributes</span></span>

<span data-ttu-id="ec289-109">无。</span><span class="sxs-lookup"><span data-stu-id="ec289-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec289-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ec289-110">Child elements</span></span>

<span data-ttu-id="ec289-111">无。</span><span class="sxs-lookup"><span data-stu-id="ec289-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ec289-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ec289-112">Parent elements</span></span>

[<span data-ttu-id="ec289-113">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="ec289-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="ec289-114">文本值</span><span class="sxs-lookup"><span data-stu-id="ec289-114">Text value</span></span>

<span data-ttu-id="ec289-115">**RetentionAction**元素的文本值是在项目上执行的操作。</span><span class="sxs-lookup"><span data-stu-id="ec289-115">The text value of the **RetentionAction** element is the action performed on items.</span></span> <span data-ttu-id="ec289-116">下面的列表包含**RetentionAction**元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="ec289-116">The following list contains the text values for the **RetentionAction** element.</span></span> 
  
> <span data-ttu-id="ec289-117">项目上执行**无**-任何操作。</span><span class="sxs-lookup"><span data-stu-id="ec289-117">**None** - No action is performed on the item.</span></span> 
    
> <span data-ttu-id="ec289-118">**MoveToDeletedItems** -项目移动到默认删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec289-118">**MoveToDeletedItems** - The item is moved to the default Deleted Items folder.</span></span> 
    
> <span data-ttu-id="ec289-119">**MoveToFolder** -项目移动到指定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec289-119">**MoveToFolder** - The item is moved to a specified folder.</span></span> 
    
> <span data-ttu-id="ec289-120">**DeleteAndAllowRecovery** -项目被删除，并置于转储程序。</span><span class="sxs-lookup"><span data-stu-id="ec289-120">**DeleteAndAllowRecovery** - The item is deleted and put into the Dumpster.</span></span> 
    
> <span data-ttu-id="ec289-121">从邮箱永久删除**PermanentlyDelete** -项目。</span><span class="sxs-lookup"><span data-stu-id="ec289-121">**PermanentlyDelete** - The item is permanently deleted from the mailbox.</span></span> 
    
> <span data-ttu-id="ec289-122">**MarkAsPastRetentionLimit** -项目标记为具有超过保留时间限制。</span><span class="sxs-lookup"><span data-stu-id="ec289-122">**MarkAsPastRetentionLimit** - The item is marked as having exceeded the retention time limit.</span></span> 
    
> <span data-ttu-id="ec289-123">**MoveToArchive** -项目移动到存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="ec289-123">**MoveToArchive** - The item is moved to the archive mailbox.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ec289-124">备注</span><span class="sxs-lookup"><span data-stu-id="ec289-124">Remarks</span></span>

<span data-ttu-id="ec289-125">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ec289-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ec289-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ec289-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec289-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="ec289-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec289-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="ec289-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ec289-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="ec289-129">Schema name</span></span>  <br/> |<span data-ttu-id="ec289-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="ec289-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="ec289-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="ec289-131">Validation file</span></span>  <br/> |<span data-ttu-id="ec289-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ec289-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ec289-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="ec289-133">Can be empty</span></span>  <br/> ||
   

