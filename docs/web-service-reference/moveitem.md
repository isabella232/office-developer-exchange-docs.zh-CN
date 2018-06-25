---
title: MoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: a4593377-22dd-415f-b01d-387389ef650f
description: MoveItem 元素定义将项目移动 Exchange 存储中的请求。
ms.openlocfilehash: cd7f35bdabe8a596f4c186df1c8cd54e0ea1c540
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826486"
---
# <a name="moveitem"></a><span data-ttu-id="560d0-103">MoveItem</span><span class="sxs-lookup"><span data-stu-id="560d0-103">MoveItem</span></span>

<span data-ttu-id="560d0-104">**MoveItem**元素定义将项目移动 Exchange 存储中的请求。</span><span class="sxs-lookup"><span data-stu-id="560d0-104">The **MoveItem** element defines a request to move an item in the Exchange store.</span></span> 
  
```XML
<MoveItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</MoveItem>
```

 <span data-ttu-id="560d0-105">**MoveItemType**</span><span class="sxs-lookup"><span data-stu-id="560d0-105">**MoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="560d0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="560d0-106">Attributes and elements</span></span>

<span data-ttu-id="560d0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="560d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="560d0-108">属性</span><span class="sxs-lookup"><span data-stu-id="560d0-108">Attributes</span></span>

<span data-ttu-id="560d0-109">无。</span><span class="sxs-lookup"><span data-stu-id="560d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="560d0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="560d0-110">Child elements</span></span>

|<span data-ttu-id="560d0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="560d0-111">**Element**</span></span>|<span data-ttu-id="560d0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="560d0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="560d0-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="560d0-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="560d0-114">代表移动项的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="560d0-114">Represents the destination folder for a moved item.</span></span>  <br/> |
|[<span data-ttu-id="560d0-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="560d0-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="560d0-116">包含要移动到[ToFolderId](tofolderid.md)元素所表示的文件夹的标识项目的数组。</span><span class="sxs-lookup"><span data-stu-id="560d0-116">Contains an array of identified items to move to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="560d0-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="560d0-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="560d0-118">指示是否在响应中返回新的项目的项标识符。</span><span class="sxs-lookup"><span data-stu-id="560d0-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="560d0-119">父元素</span><span class="sxs-lookup"><span data-stu-id="560d0-119">Parent elements</span></span>

<span data-ttu-id="560d0-120">无。</span><span class="sxs-lookup"><span data-stu-id="560d0-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="560d0-121">文本值</span><span class="sxs-lookup"><span data-stu-id="560d0-121">Text value</span></span>

<span data-ttu-id="560d0-122">无。</span><span class="sxs-lookup"><span data-stu-id="560d0-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="560d0-123">备注</span><span class="sxs-lookup"><span data-stu-id="560d0-123">Remarks</span></span>

<span data-ttu-id="560d0-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="560d0-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="560d0-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="560d0-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="560d0-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="560d0-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="560d0-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="560d0-127">Schema Name</span></span>  <br/> |<span data-ttu-id="560d0-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="560d0-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="560d0-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="560d0-129">Validation File</span></span>  <br/> |<span data-ttu-id="560d0-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="560d0-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="560d0-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="560d0-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="560d0-132">False</span><span class="sxs-lookup"><span data-stu-id="560d0-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="560d0-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="560d0-133">See also</span></span>



[<span data-ttu-id="560d0-134">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="560d0-134">MoveItem operation</span></span>](moveitem-operation.md)


- [<span data-ttu-id="560d0-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="560d0-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

