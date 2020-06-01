---
title: MakeItemImmutable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de1d2a60-aeeb-4625-8b11-23c42e1e7bae
description: MakeItemImmutable 元素指定一个布尔值，该值指示是否应将项目设为只读。
ms.openlocfilehash: 05c6e3343b8ba892048174ad98c9d31fe8da685b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465861"
---
# <a name="makeitemimmutable"></a><span data-ttu-id="cd687-103">MakeItemImmutable</span><span class="sxs-lookup"><span data-stu-id="cd687-103">MakeItemImmutable</span></span>

<span data-ttu-id="cd687-104">**MakeItemImmutable**元素指定一个布尔值，该值指示是否应将项目设为只读。</span><span class="sxs-lookup"><span data-stu-id="cd687-104">The **MakeItemImmutable** element specifies a Boolean value that indicates whether an item should be made read-only.</span></span> 
  
```XML
<MakeItemImmutable>true | false</MakeItemImmutable>
```

 <span data-ttu-id="cd687-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cd687-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd687-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cd687-106">Attributes and elements</span></span>

<span data-ttu-id="cd687-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd687-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd687-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cd687-108">Attributes</span></span>

<span data-ttu-id="cd687-109">无。</span><span class="sxs-lookup"><span data-stu-id="cd687-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd687-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cd687-110">Child elements</span></span>

<span data-ttu-id="cd687-111">无。</span><span class="sxs-lookup"><span data-stu-id="cd687-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd687-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cd687-112">Parent elements</span></span>

[<span data-ttu-id="cd687-113">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="cd687-113">UpdateItemInRecoverableItems</span></span>](updateiteminrecoverableitems.md)
  
## <a name="text-value"></a><span data-ttu-id="cd687-114">文本值</span><span class="sxs-lookup"><span data-stu-id="cd687-114">Text value</span></span>

<span data-ttu-id="cd687-115">如果**MakeItemImmutable**元素的文本值为**true** ，则表示应将该项设为只读。</span><span class="sxs-lookup"><span data-stu-id="cd687-115">A text value of **true** for the **MakeItemImmutable** element indicates that the item should be made read-only.</span></span> <span data-ttu-id="cd687-116">**如果值为 false** ，则表示项目允许读写访问。</span><span class="sxs-lookup"><span data-stu-id="cd687-116">A value of **false** indicates that the item allows read-write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cd687-117">备注</span><span class="sxs-lookup"><span data-stu-id="cd687-117">Remarks</span></span>

<span data-ttu-id="cd687-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cd687-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cd687-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cd687-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd687-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="cd687-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd687-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="cd687-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd687-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="cd687-122">Schema name</span></span>  <br/> |<span data-ttu-id="cd687-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="cd687-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cd687-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="cd687-124">Validation file</span></span>  <br/> |<span data-ttu-id="cd687-125">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="cd687-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd687-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="cd687-126">Can be empty</span></span>  <br/> ||
   

