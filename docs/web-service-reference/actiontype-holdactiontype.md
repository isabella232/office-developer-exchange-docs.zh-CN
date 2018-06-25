---
title: ActionType (HoldActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f50449b9-e73b-43c5-af96-6433bf434dce
description: ActionType 元素指示的保留操作的类型。
ms.openlocfilehash: cb1cfa8a1306c4a6cacf5c82824d19cab57e7941
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753094"
---
# <a name="actiontype-holdactiontype"></a><span data-ttu-id="fa6c0-103">ActionType (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="fa6c0-103">ActionType (HoldActionType)</span></span>

<span data-ttu-id="fa6c0-104">**ActionType**元素指示的保留操作的类型。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-104">The **ActionType** element indicates the type of action for the hold.</span></span> 
  
```XML
<ActionType> Create | Update | Remove </ActionType>
```

 <span data-ttu-id="fa6c0-105">**HoldActionType**</span><span class="sxs-lookup"><span data-stu-id="fa6c0-105">**HoldActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa6c0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa6c0-106">Attributes and elements</span></span>

<span data-ttu-id="fa6c0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa6c0-108">属性</span><span class="sxs-lookup"><span data-stu-id="fa6c0-108">Attributes</span></span>

<span data-ttu-id="fa6c0-109">无。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa6c0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fa6c0-110">Child elements</span></span>

<span data-ttu-id="fa6c0-111">无。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa6c0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fa6c0-112">Parent elements</span></span>

[<span data-ttu-id="fa6c0-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="fa6c0-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="fa6c0-114">文本值</span><span class="sxs-lookup"><span data-stu-id="fa6c0-114">Text value</span></span>

<span data-ttu-id="fa6c0-115">**ActionType**元素的文本值是设置对邮箱的保留项的类型。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-115">The text value of the **ActionType** element is the type of hold set on a mailbox.</span></span> <span data-ttu-id="fa6c0-116">**创建**文本值指示将创建邮箱保留。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-116">A text value of **Create** indicates that a mailbox hold will be created.</span></span> <span data-ttu-id="fa6c0-117">**更新**的文本值指示将更新邮箱保留。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-117">A text value of **Update** indicates that a mailbox hold will be updated.</span></span> <span data-ttu-id="fa6c0-118">**删除**文本值指示邮箱保留项将被删除。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-118">A text value of **Remove** indicates that a mailbox hold will be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa6c0-119">备注</span><span class="sxs-lookup"><span data-stu-id="fa6c0-119">Remarks</span></span>

<span data-ttu-id="fa6c0-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa6c0-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fa6c0-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa6c0-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa6c0-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa6c0-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa6c0-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa6c0-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa6c0-124">Schema name</span></span>  <br/> |<span data-ttu-id="fa6c0-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="fa6c0-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa6c0-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa6c0-126">Validation file</span></span>  <br/> |<span data-ttu-id="fa6c0-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa6c0-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa6c0-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa6c0-128">Can be empty</span></span>  <br/> |<span data-ttu-id="fa6c0-129">false</span><span class="sxs-lookup"><span data-stu-id="fa6c0-129">false</span></span>  <br/> |
   

