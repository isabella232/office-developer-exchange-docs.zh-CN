---
title: MovedItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: MovedItemId 元素指定 MarkAsJunk 操作已移动项目的标识符。
ms.openlocfilehash: 17e20e8ca81f97b419fc4a2b413e21322e828ec9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826484"
---
# <a name="moveditemid"></a><span data-ttu-id="deac4-103">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="deac4-103">MovedItemId</span></span>

<span data-ttu-id="deac4-104">**MovedItemId**元素指定**MarkAsJunk**操作已移动项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="deac4-104">The **MovedItemId** element specifies the identifier of the item that was moved by the **MarkAsJunk** operation.</span></span> 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="deac4-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="deac4-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="deac4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="deac4-106">Attributes and elements</span></span>

<span data-ttu-id="deac4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="deac4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="deac4-108">属性</span><span class="sxs-lookup"><span data-stu-id="deac4-108">Attributes</span></span>

|<span data-ttu-id="deac4-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="deac4-109">**Attribute**</span></span>|<span data-ttu-id="deac4-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="deac4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="deac4-111">Id</span><span class="sxs-lookup"><span data-stu-id="deac4-111">Id</span></span>  <br/> |<span data-ttu-id="deac4-112">**Id**属性的值是**MarkAsJunk**操作移动项的项标识符。</span><span class="sxs-lookup"><span data-stu-id="deac4-112">The value of the **Id** attribute is the item identifier of the item that is moved by the **MarkAsJunk** operation.</span></span> <span data-ttu-id="deac4-113">项标识符将保持相同后移动。</span><span class="sxs-lookup"><span data-stu-id="deac4-113">The item identifier will remain the same after the move.</span></span>  <br/> |
|<span data-ttu-id="deac4-114">更改密钥</span><span class="sxs-lookup"><span data-stu-id="deac4-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="deac4-115">**更改密钥**属性的值是项的已移动的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="deac4-115">The value of the **ChangeKey** attribute is the change key of the moved item.</span></span> <span data-ttu-id="deac4-116">更改密钥更改后**MarkAsJunk**操作移动该项目。</span><span class="sxs-lookup"><span data-stu-id="deac4-116">The change key changes after the item is moved by the **MarkAsJunk** operation.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="deac4-117">子元素</span><span class="sxs-lookup"><span data-stu-id="deac4-117">Child elements</span></span>

<span data-ttu-id="deac4-118">无。</span><span class="sxs-lookup"><span data-stu-id="deac4-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="deac4-119">父元素</span><span class="sxs-lookup"><span data-stu-id="deac4-119">Parent elements</span></span>

[<span data-ttu-id="deac4-120">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="deac4-120">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="deac4-121">备注</span><span class="sxs-lookup"><span data-stu-id="deac4-121">Remarks</span></span>

<span data-ttu-id="deac4-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="deac4-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="deac4-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="deac4-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="deac4-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="deac4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="deac4-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="deac4-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="deac4-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="deac4-126">Schema name</span></span>  <br/> |<span data-ttu-id="deac4-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="deac4-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="deac4-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="deac4-128">Validation file</span></span>  <br/> |<span data-ttu-id="deac4-129">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="deac4-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="deac4-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="deac4-130">Can be empty</span></span>  <br/> ||
   

