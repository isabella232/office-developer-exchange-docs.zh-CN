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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826484"
---
# <a name="moveditemid"></a><span data-ttu-id="f748d-103">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="f748d-103">MovedItemId</span></span>

<span data-ttu-id="f748d-104">**MovedItemId**元素指定**MarkAsJunk**操作已移动项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="f748d-104">The **MovedItemId** element specifies the identifier of the item that was moved by the **MarkAsJunk** operation.</span></span> 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="f748d-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="f748d-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f748d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f748d-106">Attributes and elements</span></span>

<span data-ttu-id="f748d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f748d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f748d-108">属性</span><span class="sxs-lookup"><span data-stu-id="f748d-108">Attributes</span></span>

|<span data-ttu-id="f748d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f748d-109">**Attribute**</span></span>|<span data-ttu-id="f748d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f748d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f748d-111">Id</span><span class="sxs-lookup"><span data-stu-id="f748d-111">Id</span></span>  <br/> |<span data-ttu-id="f748d-112">**Id**属性的值是**MarkAsJunk**操作移动项的项标识符。</span><span class="sxs-lookup"><span data-stu-id="f748d-112">The value of the **Id** attribute is the item identifier of the item that is moved by the **MarkAsJunk** operation.</span></span> <span data-ttu-id="f748d-113">项标识符将保持相同后移动。</span><span class="sxs-lookup"><span data-stu-id="f748d-113">The item identifier will remain the same after the move.</span></span>  <br/> |
|<span data-ttu-id="f748d-114">更改密钥</span><span class="sxs-lookup"><span data-stu-id="f748d-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="f748d-115">**更改密钥**属性的值是项的已移动的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="f748d-115">The value of the **ChangeKey** attribute is the change key of the moved item.</span></span> <span data-ttu-id="f748d-116">更改密钥更改后**MarkAsJunk**操作移动该项目。</span><span class="sxs-lookup"><span data-stu-id="f748d-116">The change key changes after the item is moved by the **MarkAsJunk** operation.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f748d-117">子元素</span><span class="sxs-lookup"><span data-stu-id="f748d-117">Child elements</span></span>

<span data-ttu-id="f748d-118">无。</span><span class="sxs-lookup"><span data-stu-id="f748d-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f748d-119">父元素</span><span class="sxs-lookup"><span data-stu-id="f748d-119">Parent elements</span></span>

[<span data-ttu-id="f748d-120">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f748d-120">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="f748d-121">备注</span><span class="sxs-lookup"><span data-stu-id="f748d-121">Remarks</span></span>

<span data-ttu-id="f748d-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f748d-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f748d-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f748d-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f748d-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="f748d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f748d-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="f748d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f748d-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="f748d-126">Schema name</span></span>  <br/> |<span data-ttu-id="f748d-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="f748d-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f748d-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="f748d-128">Validation file</span></span>  <br/> |<span data-ttu-id="f748d-129">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f748d-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f748d-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="f748d-130">Can be empty</span></span>  <br/> ||
   

