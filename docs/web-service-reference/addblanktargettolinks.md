---
title: AddBlankTargetToLinks
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: AddBlankTargetToLinks 元素指定将 HTML 链接中的目标属性设置为打开一个新窗口。
ms.openlocfilehash: 1d4d36c1f4b98ebee96baea683c40527d2a9ec27
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465041"
---
# <a name="addblanktargettolinks"></a><span data-ttu-id="7deb8-103">AddBlankTargetToLinks</span><span class="sxs-lookup"><span data-stu-id="7deb8-103">AddBlankTargetToLinks</span></span>

<span data-ttu-id="7deb8-104">**AddBlankTargetToLinks**元素指定将 HTML 链接中的目标属性设置为打开一个新窗口。</span><span class="sxs-lookup"><span data-stu-id="7deb8-104">The **AddBlankTargetToLinks** element specifies that the target attribute in HTML links are set to open a new window.</span></span> 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

<span data-ttu-id="7deb8-105">**xs： Boolean**</span><span class="sxs-lookup"><span data-stu-id="7deb8-105">**xs:Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7deb8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7deb8-106">Attributes and elements</span></span>

<span data-ttu-id="7deb8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7deb8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7deb8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7deb8-108">Attributes</span></span>

<span data-ttu-id="7deb8-109">无。</span><span class="sxs-lookup"><span data-stu-id="7deb8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7deb8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7deb8-110">Child elements</span></span>

<span data-ttu-id="7deb8-111">无。</span><span class="sxs-lookup"><span data-stu-id="7deb8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7deb8-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7deb8-112">Parent elements</span></span>

|<span data-ttu-id="7deb8-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7deb8-113">**Element**</span></span>|<span data-ttu-id="7deb8-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7deb8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7deb8-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="7deb8-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="7deb8-116">标识要包括在**GetItem**、 **FindItem**、 **GetConversationItems**或**SyncFolderItems**响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="7deb8-116">Identifies the item properties and content to include in a **GetItem**, **FindItem**, **GetConversationItems** or **SyncFolderItems** response.</span></span><br/><br/>  <span data-ttu-id="7deb8-117">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="7deb8-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7deb8-118">文本值</span><span class="sxs-lookup"><span data-stu-id="7deb8-118">Text value</span></span>

<span data-ttu-id="7deb8-119">如果**AddBlankTargetToLinks**元素的文本值为**true** ，则指示所有 HTML 链接都将设置为打开一个新窗口。</span><span class="sxs-lookup"><span data-stu-id="7deb8-119">A text value of **true** for the **AddBlankTargetToLinks** element indicates that all HTML links will be set to open a new window.</span></span> <span data-ttu-id="7deb8-120">如果值为**false** ，则表示将在当前窗口中打开 HTML 链接。</span><span class="sxs-lookup"><span data-stu-id="7deb8-120">A value of **false** indicates that HTML links will open in the current window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7deb8-121">说明</span><span class="sxs-lookup"><span data-stu-id="7deb8-121">Remarks</span></span>

<span data-ttu-id="7deb8-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="7deb8-122">This element is optional.</span></span>
  
<span data-ttu-id="7deb8-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7deb8-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7deb8-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7deb8-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7deb8-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="7deb8-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7deb8-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="7deb8-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7deb8-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="7deb8-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7deb8-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="7deb8-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="7deb8-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="7deb8-129">Validation File</span></span>  <br/> |<span data-ttu-id="7deb8-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="7deb8-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7deb8-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="7deb8-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7deb8-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7deb8-132">See also</span></span>

- [<span data-ttu-id="7deb8-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7deb8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

