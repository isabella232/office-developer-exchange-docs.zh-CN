---
title: IsVisible
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 403acdd5-3b79-46f4-9894-ba57e10085e4
description: IsVisible 元素指示保留策略对用户是否可见。
ms.openlocfilehash: 8cb8e99cef0f89d7ba6435690bd6d57b79a45bc8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458143"
---
# <a name="isvisible"></a><span data-ttu-id="20bb8-103">IsVisible</span><span class="sxs-lookup"><span data-stu-id="20bb8-103">IsVisible</span></span>

<span data-ttu-id="20bb8-104">**IsVisible**元素指示保留策略对用户是否可见。</span><span class="sxs-lookup"><span data-stu-id="20bb8-104">The **IsVisible** element indicates whether the retention policy is visible to users.</span></span> 
  
```XML
<IsVisible> true | false</IsVisible>
```

 <span data-ttu-id="20bb8-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="20bb8-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20bb8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="20bb8-106">Attributes and elements</span></span>

<span data-ttu-id="20bb8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="20bb8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20bb8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="20bb8-108">Attributes</span></span>

<span data-ttu-id="20bb8-109">无。</span><span class="sxs-lookup"><span data-stu-id="20bb8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20bb8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="20bb8-110">Child elements</span></span>

<span data-ttu-id="20bb8-111">无。</span><span class="sxs-lookup"><span data-stu-id="20bb8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="20bb8-112">父元素</span><span class="sxs-lookup"><span data-stu-id="20bb8-112">Parent elements</span></span>

[<span data-ttu-id="20bb8-113">Get-retentionpolicytag</span><span class="sxs-lookup"><span data-stu-id="20bb8-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="20bb8-114">文本值</span><span class="sxs-lookup"><span data-stu-id="20bb8-114">Text value</span></span>

<span data-ttu-id="20bb8-115">如果**IsVisible**元素的文本值为**true** ，则表示保留策略对用户可见。</span><span class="sxs-lookup"><span data-stu-id="20bb8-115">A text value of **true** for the **IsVisible** element indicates that the retention policy is visible to a user.</span></span> <span data-ttu-id="20bb8-116">**如果值为 false** ，则表示保留策略对用户不可见。</span><span class="sxs-lookup"><span data-stu-id="20bb8-116">A value of **false** indicates the retention policy is not visible to users.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="20bb8-117">备注</span><span class="sxs-lookup"><span data-stu-id="20bb8-117">Remarks</span></span>

<span data-ttu-id="20bb8-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="20bb8-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="20bb8-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="20bb8-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

