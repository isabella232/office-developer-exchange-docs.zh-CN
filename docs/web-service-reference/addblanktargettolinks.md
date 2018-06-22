---
title: AddBlankTargetToLinks
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: AddBlankTargetToLinks 元素指定的 HTML 链接的目标属性已设置为打开一个新窗口。
ms.openlocfilehash: 8a47e44d89bcc84bc0e8b61d45f18ff3182f7870
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753100"
---
# <a name="addblanktargettolinks"></a><span data-ttu-id="84150-103">AddBlankTargetToLinks</span><span class="sxs-lookup"><span data-stu-id="84150-103">AddBlankTargetToLinks</span></span>

<span data-ttu-id="84150-104">**AddBlankTargetToLinks**元素指定的 HTML 链接的目标属性已设置为打开一个新窗口。</span><span class="sxs-lookup"><span data-stu-id="84150-104">The **AddBlankTargetToLinks** element specifies that the target attribute in HTML links are set to open a new window.</span></span> 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

<span data-ttu-id="84150-105">**xs: boolean**</span><span class="sxs-lookup"><span data-stu-id="84150-105">**xs:Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="84150-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="84150-106">Attributes and elements</span></span>

<span data-ttu-id="84150-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="84150-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84150-108">属性</span><span class="sxs-lookup"><span data-stu-id="84150-108">Attributes</span></span>

<span data-ttu-id="84150-109">无。</span><span class="sxs-lookup"><span data-stu-id="84150-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84150-110">子元素</span><span class="sxs-lookup"><span data-stu-id="84150-110">Child elements</span></span>

<span data-ttu-id="84150-111">无。</span><span class="sxs-lookup"><span data-stu-id="84150-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="84150-112">父元素</span><span class="sxs-lookup"><span data-stu-id="84150-112">Parent elements</span></span>

|<span data-ttu-id="84150-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="84150-113">**Element**</span></span>|<span data-ttu-id="84150-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="84150-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84150-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="84150-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="84150-116">标识项目属性和**GetItem**、 **FindItem**、 **GetConversationItems**或**SyncFolderItems**响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="84150-116">Identifies the item properties and content to include in a **GetItem**, **FindItem**, **GetConversationItems** or **SyncFolderItems** response.</span></span><br/><br/>  <span data-ttu-id="84150-117">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="84150-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="84150-118">文本值</span><span class="sxs-lookup"><span data-stu-id="84150-118">Text value</span></span>

<span data-ttu-id="84150-119">文本值为**true**的**AddBlankTargetToLinks**元素表示，会设置所有 HTML 链接以打开一个新窗口。</span><span class="sxs-lookup"><span data-stu-id="84150-119">A text value of **true** for the **AddBlankTargetToLinks** element indicates that all HTML links will be set to open a new window.</span></span> <span data-ttu-id="84150-120">如果值为**false**指示 HTML 链接将在当前窗口中打开。</span><span class="sxs-lookup"><span data-stu-id="84150-120">A value of **false** indicates that HTML links will open in the current window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="84150-121">备注</span><span class="sxs-lookup"><span data-stu-id="84150-121">Remarks</span></span>

<span data-ttu-id="84150-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="84150-122">This element is optional.</span></span>
  
<span data-ttu-id="84150-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="84150-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="84150-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="84150-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84150-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="84150-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84150-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="84150-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84150-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="84150-127">Schema Name</span></span>  <br/> |<span data-ttu-id="84150-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="84150-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="84150-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="84150-129">Validation File</span></span>  <br/> |<span data-ttu-id="84150-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="84150-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="84150-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="84150-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="84150-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84150-132">See also</span></span>

- [<span data-ttu-id="84150-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="84150-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

