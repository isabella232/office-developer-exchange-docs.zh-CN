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
ms.openlocfilehash: eab559e938f0b949d79626ae5bf61b3d4a838924
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460622"
---
# <a name="includenonindexableitems"></a><span data-ttu-id="c7433-103">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="c7433-103">IncludeNonIndexableItems</span></span>

<span data-ttu-id="c7433-104">**IncludeNonIndexableItems**元素包含一个**布尔**值，指示是否包含无法编制索引的项目。</span><span class="sxs-lookup"><span data-stu-id="c7433-104">The **IncludeNonIndexableItems** element contains a **Boolean** value to indicate whether to include items that cannot be indexed.</span></span> 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 <span data-ttu-id="c7433-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c7433-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7433-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c7433-106">Attributes and elements</span></span>

<span data-ttu-id="c7433-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c7433-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7433-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c7433-108">Attributes</span></span>

<span data-ttu-id="c7433-109">无。</span><span class="sxs-lookup"><span data-stu-id="c7433-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7433-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c7433-110">Child elements</span></span>

<span data-ttu-id="c7433-111">无。</span><span class="sxs-lookup"><span data-stu-id="c7433-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7433-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c7433-112">Parent elements</span></span>

[<span data-ttu-id="c7433-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="c7433-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="c7433-114">文本值</span><span class="sxs-lookup"><span data-stu-id="c7433-114">Text value</span></span>

<span data-ttu-id="c7433-115">**IncludeNonIndexableItems**元素的文本值为**true**表示无法编制索引的项目包含在邮箱保留中。</span><span class="sxs-lookup"><span data-stu-id="c7433-115">A text value of **true** for the **IncludeNonIndexableItems** element indicates that items that cannot be indexed are included with mailbox holds.</span></span> <span data-ttu-id="c7433-116">**如果值为 false** ，则表示邮箱保留中不包含无法编制索引的项目。</span><span class="sxs-lookup"><span data-stu-id="c7433-116">A value of **false** indicates that the items that cannot be indexed are not included in mailbox holds.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c7433-117">备注</span><span class="sxs-lookup"><span data-stu-id="c7433-117">Remarks</span></span>

<span data-ttu-id="c7433-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c7433-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c7433-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c7433-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7433-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="c7433-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7433-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="c7433-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c7433-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="c7433-122">Schema name</span></span>  <br/> |<span data-ttu-id="c7433-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="c7433-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c7433-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="c7433-124">Validation file</span></span>  <br/> |<span data-ttu-id="c7433-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c7433-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c7433-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="c7433-126">Can be empty</span></span>  <br/> |<span data-ttu-id="c7433-127">false</span><span class="sxs-lookup"><span data-stu-id="c7433-127">false</span></span>  <br/> |
   

