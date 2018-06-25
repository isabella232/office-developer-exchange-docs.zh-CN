---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: BlockExternalImages 元素指定的 HTML 文本正文中是否阻止外部图像。
ms.openlocfilehash: 41ab2ec7ec1c24ccbbef037ef1e27431c1fe6811
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753330"
---
# <a name="blockexternalimages"></a><span data-ttu-id="4ca98-103">BlockExternalImages</span><span class="sxs-lookup"><span data-stu-id="4ca98-103">BlockExternalImages</span></span>

<span data-ttu-id="4ca98-104">**BlockExternalImages**元素指定的 HTML 文本正文中是否阻止外部图像。</span><span class="sxs-lookup"><span data-stu-id="4ca98-104">The **BlockExternalImages** element specifies whether external images are blocked in HTML text bodies.</span></span> 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
```

 <span data-ttu-id="4ca98-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4ca98-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ca98-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4ca98-106">Attributes and elements</span></span>

<span data-ttu-id="4ca98-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4ca98-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ca98-108">属性</span><span class="sxs-lookup"><span data-stu-id="4ca98-108">Attributes</span></span>

<span data-ttu-id="4ca98-109">无。</span><span class="sxs-lookup"><span data-stu-id="4ca98-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ca98-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4ca98-110">Child elements</span></span>

<span data-ttu-id="4ca98-111">无。</span><span class="sxs-lookup"><span data-stu-id="4ca98-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4ca98-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4ca98-112">Parent elements</span></span>

|<span data-ttu-id="4ca98-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4ca98-113">**Element**</span></span>|<span data-ttu-id="4ca98-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ca98-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ca98-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="4ca98-115">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="4ca98-116">标识要在 GetFolder、 FindFolder 或 SyncFolderHierarchy 响应中包含的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="4ca98-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span>  <br/> |
|[<span data-ttu-id="4ca98-117">ItemShape</span><span class="sxs-lookup"><span data-stu-id="4ca98-117">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="4ca98-118">标识项目属性和 GetItem、 FindItem 或 SyncFolderItems 响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="4ca98-118">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4ca98-119">文本值</span><span class="sxs-lookup"><span data-stu-id="4ca98-119">Text value</span></span>

<span data-ttu-id="4ca98-120">文本值为**true** **BlockExternalImages**元素表示外部图像表单 HTML 正文中被阻止。</span><span class="sxs-lookup"><span data-stu-id="4ca98-120">A text value of **true** for **BlockExternalImages** element indicates that external images are blocked in HTML bodies.</span></span> <span data-ttu-id="4ca98-121">如果值为**false**指示允许外部图像。</span><span class="sxs-lookup"><span data-stu-id="4ca98-121">A value of **false** indicates that external images are allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4ca98-122">备注</span><span class="sxs-lookup"><span data-stu-id="4ca98-122">Remarks</span></span>

<span data-ttu-id="4ca98-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4ca98-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4ca98-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4ca98-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ca98-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="4ca98-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ca98-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="4ca98-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4ca98-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="4ca98-127">Schema Name</span></span>  <br/> |<span data-ttu-id="4ca98-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="4ca98-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="4ca98-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="4ca98-129">Validation File</span></span>  <br/> |<span data-ttu-id="4ca98-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="4ca98-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4ca98-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="4ca98-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4ca98-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4ca98-132">See also</span></span>



- [<span data-ttu-id="4ca98-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4ca98-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

