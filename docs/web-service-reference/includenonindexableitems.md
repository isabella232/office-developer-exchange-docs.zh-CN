---
title: IncludeNonIndexableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: af7f202b-2889-447e-bdeb-aaad18ce6b46
description: IncludeNonIndexableItems 元素包含一个布尔值，指示是否包含无法编制索引的项目。
ms.openlocfilehash: ae91a3c6db82aea1d45940603d0ff2064d29f43f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825904"
---
# <a name="includenonindexableitems"></a><span data-ttu-id="381e6-103">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="381e6-103">IncludeNonIndexableItems</span></span>

<span data-ttu-id="381e6-104">**IncludeNonIndexableItems**元素包含一个**布尔**值，指示是否包含无法编制索引的项目。</span><span class="sxs-lookup"><span data-stu-id="381e6-104">The **IncludeNonIndexableItems** element contains a **Boolean** value to indicate whether to include items that cannot be indexed.</span></span> 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 <span data-ttu-id="381e6-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="381e6-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="381e6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="381e6-106">Attributes and elements</span></span>

<span data-ttu-id="381e6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="381e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="381e6-108">属性</span><span class="sxs-lookup"><span data-stu-id="381e6-108">Attributes</span></span>

<span data-ttu-id="381e6-109">无。</span><span class="sxs-lookup"><span data-stu-id="381e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="381e6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="381e6-110">Child elements</span></span>

<span data-ttu-id="381e6-111">无。</span><span class="sxs-lookup"><span data-stu-id="381e6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="381e6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="381e6-112">Parent elements</span></span>

[<span data-ttu-id="381e6-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="381e6-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="381e6-114">文本值</span><span class="sxs-lookup"><span data-stu-id="381e6-114">Text value</span></span>

<span data-ttu-id="381e6-115">文本值为**true**的**IncludeNonIndexableItems**元素指示无法编制索引的项目包含邮箱保留项。</span><span class="sxs-lookup"><span data-stu-id="381e6-115">A text value of **true** for the **IncludeNonIndexableItems** element indicates that items that cannot be indexed are included with mailbox holds.</span></span> <span data-ttu-id="381e6-116">如果值为**false**指示邮箱保留项中的用户不能包含不能编制索引的项目。</span><span class="sxs-lookup"><span data-stu-id="381e6-116">A value of **false** indicates that the items that cannot be indexed are not included in mailbox holds.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="381e6-117">备注</span><span class="sxs-lookup"><span data-stu-id="381e6-117">Remarks</span></span>

<span data-ttu-id="381e6-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="381e6-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="381e6-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="381e6-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="381e6-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="381e6-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="381e6-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="381e6-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="381e6-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="381e6-122">Schema name</span></span>  <br/> |<span data-ttu-id="381e6-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="381e6-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="381e6-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="381e6-124">Validation file</span></span>  <br/> |<span data-ttu-id="381e6-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="381e6-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="381e6-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="381e6-126">Can be empty</span></span>  <br/> |<span data-ttu-id="381e6-127">false</span><span class="sxs-lookup"><span data-stu-id="381e6-127">false</span></span>  <br/> |
   

