---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: ReturnNewItemIds 元素指示是否在响应中返回新的项目的项标识符。
ms.openlocfilehash: 6d3bc83c05a82d6e448041167676f41c2620dcd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827232"
---
# <a name="returnnewitemids"></a><span data-ttu-id="f7bbd-103">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="f7bbd-103">ReturnNewItemIds</span></span>

<span data-ttu-id="f7bbd-104">**ReturnNewItemIds**元素指示是否在响应中返回新的项目的项标识符。</span><span class="sxs-lookup"><span data-stu-id="f7bbd-104">The **ReturnNewItemIds** element indicates whether the item identifiers of new items are returned in the response.</span></span> 
  
```XML
<ReturnNewItemIds/>
```

 <span data-ttu-id="f7bbd-105">**xs: boolean**</span><span class="sxs-lookup"><span data-stu-id="f7bbd-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7bbd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f7bbd-106">Attributes and elements</span></span>

<span data-ttu-id="f7bbd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f7bbd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7bbd-108">属性</span><span class="sxs-lookup"><span data-stu-id="f7bbd-108">Attributes</span></span>

<span data-ttu-id="f7bbd-109">无。</span><span class="sxs-lookup"><span data-stu-id="f7bbd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7bbd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f7bbd-110">Child elements</span></span>

<span data-ttu-id="f7bbd-111">无。</span><span class="sxs-lookup"><span data-stu-id="f7bbd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f7bbd-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f7bbd-112">Parent elements</span></span>

|<span data-ttu-id="f7bbd-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7bbd-113">**Element**</span></span>|<span data-ttu-id="f7bbd-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7bbd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7bbd-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="f7bbd-115">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="f7bbd-116">定义项目复制 Exchange 存储中的邮箱中的请求。</span><span class="sxs-lookup"><span data-stu-id="f7bbd-116">Defines a request to copy an item in a mailbox in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f7bbd-117">MoveItem</span><span class="sxs-lookup"><span data-stu-id="f7bbd-117">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="f7bbd-118">定义在 Exchange 存储中移动项目的请求。</span><span class="sxs-lookup"><span data-stu-id="f7bbd-118">Defines a request to move an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f7bbd-119">文本值</span><span class="sxs-lookup"><span data-stu-id="f7bbd-119">Text value</span></span>

<span data-ttu-id="f7bbd-120">文本值为**true**的**ReturnNewItemIds**元素指示返回的响应中的新的项标识符。</span><span class="sxs-lookup"><span data-stu-id="f7bbd-120">A text value of **true** for the **ReturnNewItemIds** element indicates that the new item identifiers are returned in the response.</span></span> <span data-ttu-id="f7bbd-121">如果值为**false**指示响应中的用户不能返回新的项标识符。</span><span class="sxs-lookup"><span data-stu-id="f7bbd-121">A value of **false** indicates that the new item identifiers are not returned in the response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f7bbd-122">备注</span><span class="sxs-lookup"><span data-stu-id="f7bbd-122">Remarks</span></span>

<span data-ttu-id="f7bbd-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f7bbd-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7bbd-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="f7bbd-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7bbd-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="f7bbd-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f7bbd-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="f7bbd-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f7bbd-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="f7bbd-127">Message schema</span></span>  <br/> |
|<span data-ttu-id="f7bbd-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="f7bbd-128">Validation File</span></span>  <br/> |<span data-ttu-id="f7bbd-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f7bbd-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f7bbd-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="f7bbd-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7bbd-131">False</span><span class="sxs-lookup"><span data-stu-id="f7bbd-131">False</span></span>  <br/> |
   

