---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: BlockExternalImages 元素指定是否在 HTML 文本正文中阻止外部图像。
ms.openlocfilehash: 73342316024ebe476a0e35f14157befc80edcf83
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527402"
---
# <a name="blockexternalimages"></a><span data-ttu-id="18691-103">BlockExternalImages</span><span class="sxs-lookup"><span data-stu-id="18691-103">BlockExternalImages</span></span>

<span data-ttu-id="18691-104">**BlockExternalImages**元素指定是否在 HTML 文本正文中阻止外部图像。</span><span class="sxs-lookup"><span data-stu-id="18691-104">The **BlockExternalImages** element specifies whether external images are blocked in HTML text bodies.</span></span> 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
```

 <span data-ttu-id="18691-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="18691-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18691-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="18691-106">Attributes and elements</span></span>

<span data-ttu-id="18691-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="18691-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18691-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="18691-108">Attributes</span></span>

<span data-ttu-id="18691-109">无。</span><span class="sxs-lookup"><span data-stu-id="18691-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18691-110">子元素</span><span class="sxs-lookup"><span data-stu-id="18691-110">Child elements</span></span>

<span data-ttu-id="18691-111">无。</span><span class="sxs-lookup"><span data-stu-id="18691-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="18691-112">父元素</span><span class="sxs-lookup"><span data-stu-id="18691-112">Parent elements</span></span>

|<span data-ttu-id="18691-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="18691-113">**Element**</span></span>|<span data-ttu-id="18691-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="18691-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18691-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="18691-115">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="18691-116">标识要包括在 GetFolder、FindFolder 或 SyncFolderHierarchy 响应中的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="18691-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span>  <br/> |
|[<span data-ttu-id="18691-117">ItemShape</span><span class="sxs-lookup"><span data-stu-id="18691-117">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="18691-118">标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="18691-118">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="18691-119">文本值</span><span class="sxs-lookup"><span data-stu-id="18691-119">Text value</span></span>

<span data-ttu-id="18691-120">**BlockExternalImages**元素的文本值为**true**表示外部图像在 HTML 正文中被阻止。</span><span class="sxs-lookup"><span data-stu-id="18691-120">A text value of **true** for **BlockExternalImages** element indicates that external images are blocked in HTML bodies.</span></span> <span data-ttu-id="18691-121">**如果值为 false** ，则表示允许外部图像。</span><span class="sxs-lookup"><span data-stu-id="18691-121">A value of **false** indicates that external images are allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="18691-122">备注</span><span class="sxs-lookup"><span data-stu-id="18691-122">Remarks</span></span>

<span data-ttu-id="18691-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="18691-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="18691-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="18691-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18691-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="18691-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18691-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="18691-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="18691-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="18691-127">Schema Name</span></span>  <br/> |<span data-ttu-id="18691-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="18691-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="18691-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="18691-129">Validation File</span></span>  <br/> |<span data-ttu-id="18691-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="18691-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="18691-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="18691-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="18691-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18691-132">See also</span></span>



- [<span data-ttu-id="18691-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="18691-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

