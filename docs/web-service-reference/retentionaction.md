---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: RetentionAction 元素指定对带有保留标记的项目执行的操作。
ms.openlocfilehash: c16988413e732ddc3cd6ebc355cb73c4d96550c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465231"
---
# <a name="retentionaction"></a><span data-ttu-id="0801b-103">RetentionAction</span><span class="sxs-lookup"><span data-stu-id="0801b-103">RetentionAction</span></span>

<span data-ttu-id="0801b-104">**RetentionAction**元素指定对带有保留标记的项目执行的操作。</span><span class="sxs-lookup"><span data-stu-id="0801b-104">The **RetentionAction** element specifies the action performed on items with the retention tag.</span></span> 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 <span data-ttu-id="0801b-105">**RetentionActionType**</span><span class="sxs-lookup"><span data-stu-id="0801b-105">**RetentionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0801b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0801b-106">Attributes and elements</span></span>

<span data-ttu-id="0801b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0801b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0801b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0801b-108">Attributes</span></span>

<span data-ttu-id="0801b-109">无。</span><span class="sxs-lookup"><span data-stu-id="0801b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0801b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0801b-110">Child elements</span></span>

<span data-ttu-id="0801b-111">无。</span><span class="sxs-lookup"><span data-stu-id="0801b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0801b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0801b-112">Parent elements</span></span>

[<span data-ttu-id="0801b-113">Get-retentionpolicytag</span><span class="sxs-lookup"><span data-stu-id="0801b-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="0801b-114">文本值</span><span class="sxs-lookup"><span data-stu-id="0801b-114">Text value</span></span>

<span data-ttu-id="0801b-115">**RetentionAction**元素的文本值是对项目执行的操作。</span><span class="sxs-lookup"><span data-stu-id="0801b-115">The text value of the **RetentionAction** element is the action performed on items.</span></span> <span data-ttu-id="0801b-116">以下列表包含**RetentionAction**元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="0801b-116">The following list contains the text values for the **RetentionAction** element.</span></span> 
  
> <span data-ttu-id="0801b-117">**无**-对项目不执行任何操作。</span><span class="sxs-lookup"><span data-stu-id="0801b-117">**None** - No action is performed on the item.</span></span> 
    
> <span data-ttu-id="0801b-118">**MoveToDeletedItems** -将项目移动到默认的 "已删除邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="0801b-118">**MoveToDeletedItems** - The item is moved to the default Deleted Items folder.</span></span> 
    
> <span data-ttu-id="0801b-119">**MoveToFolder** -将项目移动到指定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="0801b-119">**MoveToFolder** - The item is moved to a specified folder.</span></span> 
    
> <span data-ttu-id="0801b-120">**DeleteAndAllowRecovery** -将删除该项目并将其放入转储程序中。</span><span class="sxs-lookup"><span data-stu-id="0801b-120">**DeleteAndAllowRecovery** - The item is deleted and put into the Dumpster.</span></span> 
    
> <span data-ttu-id="0801b-121">**PermanentlyDelete** -项目从邮箱中永久删除。</span><span class="sxs-lookup"><span data-stu-id="0801b-121">**PermanentlyDelete** - The item is permanently deleted from the mailbox.</span></span> 
    
> <span data-ttu-id="0801b-122">**MarkAsPastRetentionLimit** -项目被标记为已超过保留时间限制。</span><span class="sxs-lookup"><span data-stu-id="0801b-122">**MarkAsPastRetentionLimit** - The item is marked as having exceeded the retention time limit.</span></span> 
    
> <span data-ttu-id="0801b-123">**MoveToArchive** -将项目移动到存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="0801b-123">**MoveToArchive** - The item is moved to the archive mailbox.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0801b-124">备注</span><span class="sxs-lookup"><span data-stu-id="0801b-124">Remarks</span></span>

<span data-ttu-id="0801b-125">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0801b-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0801b-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0801b-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0801b-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="0801b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0801b-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="0801b-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0801b-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="0801b-129">Schema name</span></span>  <br/> |<span data-ttu-id="0801b-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="0801b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="0801b-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="0801b-131">Validation file</span></span>  <br/> |<span data-ttu-id="0801b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0801b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0801b-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="0801b-133">Can be empty</span></span>  <br/> ||
   

