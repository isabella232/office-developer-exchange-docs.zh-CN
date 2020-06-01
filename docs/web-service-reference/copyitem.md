---
title: CopyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItem
api_type:
- schema
ms.assetid: ffb4c13e-e7ea-4e6b-87a0-509ce5371100
description: CopyItem 元素定义一个请求，以在 Exchange 存储区中复制邮箱中的项目。
ms.openlocfilehash: b9af1670fd580107de08ad3b950191399436388d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458500"
---
# <a name="copyitem"></a><span data-ttu-id="14cb6-103">CopyItem</span><span class="sxs-lookup"><span data-stu-id="14cb6-103">CopyItem</span></span>

<span data-ttu-id="14cb6-104">**CopyItem**元素定义一个请求，以在 Exchange 存储区中复制邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="14cb6-104">The **CopyItem** element defines a request to copy an item in a mailbox in the Exchange store.</span></span> 
  
```XML
<CopyItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</CopyItem>
```

 <span data-ttu-id="14cb6-105">**CopyItemType**</span><span class="sxs-lookup"><span data-stu-id="14cb6-105">**CopyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14cb6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="14cb6-106">Attributes and elements</span></span>

<span data-ttu-id="14cb6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="14cb6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14cb6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="14cb6-108">Attributes</span></span>

<span data-ttu-id="14cb6-109">无。</span><span class="sxs-lookup"><span data-stu-id="14cb6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14cb6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="14cb6-110">Child elements</span></span>

|<span data-ttu-id="14cb6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="14cb6-111">**Element**</span></span>|<span data-ttu-id="14cb6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="14cb6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14cb6-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="14cb6-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="14cb6-114">表示复制的项的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="14cb6-114">Represents the destination folder for a copied item.</span></span>  <br/> |
|[<span data-ttu-id="14cb6-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="14cb6-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="14cb6-116">包含要复制到[ToFolderId](tofolderid.md)元素所表示的文件夹中的已标识项的数组。</span><span class="sxs-lookup"><span data-stu-id="14cb6-116">Contains an array of identified items to copy to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="14cb6-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="14cb6-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="14cb6-118">指示响应中是否返回新项的项标识符。</span><span class="sxs-lookup"><span data-stu-id="14cb6-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="14cb6-119">父元素</span><span class="sxs-lookup"><span data-stu-id="14cb6-119">Parent elements</span></span>

<span data-ttu-id="14cb6-120">无。</span><span class="sxs-lookup"><span data-stu-id="14cb6-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="14cb6-121">说明</span><span class="sxs-lookup"><span data-stu-id="14cb6-121">Remarks</span></span>

<span data-ttu-id="14cb6-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="14cb6-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14cb6-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="14cb6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14cb6-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="14cb6-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="14cb6-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="14cb6-125">Schema Name</span></span>  <br/> |<span data-ttu-id="14cb6-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="14cb6-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="14cb6-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="14cb6-127">Validation File</span></span>  <br/> |<span data-ttu-id="14cb6-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="14cb6-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="14cb6-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="14cb6-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="14cb6-130">False</span><span class="sxs-lookup"><span data-stu-id="14cb6-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14cb6-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="14cb6-131">See also</span></span>



[<span data-ttu-id="14cb6-132">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="14cb6-132">CopyItem operation</span></span>](copyitem-operation.md)


- [<span data-ttu-id="14cb6-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="14cb6-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

