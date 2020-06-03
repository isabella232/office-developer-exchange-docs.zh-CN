---
title: MovedItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: MovedItemId 元素指定 MarkAsJunk 操作移动的项的标识符。
ms.openlocfilehash: 5cf8800ec672278691348bbcd8c6c8cc7a12905b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468612"
---
# <a name="moveditemid"></a><span data-ttu-id="7b3d6-103">MovedItemId</span><span class="sxs-lookup"><span data-stu-id="7b3d6-103">MovedItemId</span></span>

<span data-ttu-id="7b3d6-104">**MovedItemId**元素指定**MarkAsJunk**操作移动的项的标识符。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-104">The **MovedItemId** element specifies the identifier of the item that was moved by the **MarkAsJunk** operation.</span></span> 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="7b3d6-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="7b3d6-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b3d6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7b3d6-106">Attributes and elements</span></span>

<span data-ttu-id="7b3d6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b3d6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7b3d6-108">Attributes</span></span>

|<span data-ttu-id="7b3d6-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="7b3d6-109">**Attribute**</span></span>|<span data-ttu-id="7b3d6-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b3d6-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b3d6-111">Id</span><span class="sxs-lookup"><span data-stu-id="7b3d6-111">Id</span></span>  <br/> |<span data-ttu-id="7b3d6-112">**Id**属性的值是由**MarkAsJunk**操作移动的项的项标识符。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-112">The value of the **Id** attribute is the item identifier of the item that is moved by the **MarkAsJunk** operation.</span></span> <span data-ttu-id="7b3d6-113">移动后项目标识符将保持不变。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-113">The item identifier will remain the same after the move.</span></span>  <br/> |
|<span data-ttu-id="7b3d6-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="7b3d6-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="7b3d6-115">**ChangeKey**属性的值是已移动项的更改键。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-115">The value of the **ChangeKey** attribute is the change key of the moved item.</span></span> <span data-ttu-id="7b3d6-116">在**MarkAsJunk**操作移动项目之后更改密钥更改。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-116">The change key changes after the item is moved by the **MarkAsJunk** operation.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7b3d6-117">子元素</span><span class="sxs-lookup"><span data-stu-id="7b3d6-117">Child elements</span></span>

<span data-ttu-id="7b3d6-118">无。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7b3d6-119">父元素</span><span class="sxs-lookup"><span data-stu-id="7b3d6-119">Parent elements</span></span>

[<span data-ttu-id="7b3d6-120">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7b3d6-120">MarkAsJunkResponseMessage</span></span>](markasjunkresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="7b3d6-121">备注</span><span class="sxs-lookup"><span data-stu-id="7b3d6-121">Remarks</span></span>

<span data-ttu-id="7b3d6-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7b3d6-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7b3d6-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b3d6-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="7b3d6-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b3d6-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="7b3d6-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7b3d6-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="7b3d6-126">Schema name</span></span>  <br/> |<span data-ttu-id="7b3d6-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="7b3d6-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7b3d6-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="7b3d6-128">Validation file</span></span>  <br/> |<span data-ttu-id="7b3d6-129">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="7b3d6-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7b3d6-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="7b3d6-130">Can be empty</span></span>  <br/> ||
   

