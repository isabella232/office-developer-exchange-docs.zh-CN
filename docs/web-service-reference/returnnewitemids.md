---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: ReturnNewItemIds 元素指示是否在响应中返回新项的项标识符。
ms.openlocfilehash: 003676c4c034454aa551e42bf3af976183117b8c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465112"
---
# <a name="returnnewitemids"></a><span data-ttu-id="cd923-103">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="cd923-103">ReturnNewItemIds</span></span>

<span data-ttu-id="cd923-104">**ReturnNewItemIds**元素指示是否在响应中返回新项的项标识符。</span><span class="sxs-lookup"><span data-stu-id="cd923-104">The **ReturnNewItemIds** element indicates whether the item identifiers of new items are returned in the response.</span></span> 
  
```XML
<ReturnNewItemIds/>
```

 <span data-ttu-id="cd923-105">**xs： boolean**</span><span class="sxs-lookup"><span data-stu-id="cd923-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd923-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cd923-106">Attributes and elements</span></span>

<span data-ttu-id="cd923-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd923-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd923-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cd923-108">Attributes</span></span>

<span data-ttu-id="cd923-109">无。</span><span class="sxs-lookup"><span data-stu-id="cd923-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd923-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cd923-110">Child elements</span></span>

<span data-ttu-id="cd923-111">无。</span><span class="sxs-lookup"><span data-stu-id="cd923-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd923-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cd923-112">Parent elements</span></span>

|<span data-ttu-id="cd923-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cd923-113">**Element**</span></span>|<span data-ttu-id="cd923-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cd923-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd923-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="cd923-115">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="cd923-116">定义对 Exchange 存储中的邮箱中的项目进行复制的请求。</span><span class="sxs-lookup"><span data-stu-id="cd923-116">Defines a request to copy an item in a mailbox in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cd923-117">MoveItem</span><span class="sxs-lookup"><span data-stu-id="cd923-117">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="cd923-118">定义在 Exchange 存储中移动项目的请求。</span><span class="sxs-lookup"><span data-stu-id="cd923-118">Defines a request to move an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cd923-119">文本值</span><span class="sxs-lookup"><span data-stu-id="cd923-119">Text value</span></span>

<span data-ttu-id="cd923-120">如果**ReturnNewItemIds**元素的文本值为**true** ，则表示在响应中返回新的项目标识符。</span><span class="sxs-lookup"><span data-stu-id="cd923-120">A text value of **true** for the **ReturnNewItemIds** element indicates that the new item identifiers are returned in the response.</span></span> <span data-ttu-id="cd923-121">**如果值为 false** ，则表示响应中不返回新的项目标识符。</span><span class="sxs-lookup"><span data-stu-id="cd923-121">A value of **false** indicates that the new item identifiers are not returned in the response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cd923-122">备注</span><span class="sxs-lookup"><span data-stu-id="cd923-122">Remarks</span></span>

<span data-ttu-id="cd923-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cd923-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd923-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="cd923-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd923-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="cd923-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd923-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="cd923-126">Schema Name</span></span>  <br/> |<span data-ttu-id="cd923-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="cd923-127">Message schema</span></span>  <br/> |
|<span data-ttu-id="cd923-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="cd923-128">Validation File</span></span>  <br/> |<span data-ttu-id="cd923-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cd923-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd923-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="cd923-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd923-131">False</span><span class="sxs-lookup"><span data-stu-id="cd923-131">False</span></span>  <br/> |
   

