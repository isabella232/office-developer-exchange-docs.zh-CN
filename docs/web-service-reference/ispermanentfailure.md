---
title: IsPermanentFailure
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18dc3a97-cc0a-4092-934e-a6e86f52e668
description: IsPermanentFailure 元素指示先前对项目编制索引的尝试是否未成功。
ms.openlocfilehash: 48a13eebfa16c538c1b10d92f080d51f1b318d12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460391"
---
# <a name="ispermanentfailure"></a><span data-ttu-id="14655-103">IsPermanentFailure</span><span class="sxs-lookup"><span data-stu-id="14655-103">IsPermanentFailure</span></span>

<span data-ttu-id="14655-104">**IsPermanentFailure**元素指示先前对项目编制索引的尝试是否未成功。</span><span class="sxs-lookup"><span data-stu-id="14655-104">The **IsPermanentFailure** element indicates whether a previous attempt to index the item was unsuccessful.</span></span> 
  
```XML
<IsPermanentFailure>true | false</IsPermanentFailure>
```

 <span data-ttu-id="14655-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="14655-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14655-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="14655-106">Attributes and elements</span></span>

<span data-ttu-id="14655-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="14655-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14655-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="14655-108">Attributes</span></span>

<span data-ttu-id="14655-109">无。</span><span class="sxs-lookup"><span data-stu-id="14655-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14655-110">子元素</span><span class="sxs-lookup"><span data-stu-id="14655-110">Child elements</span></span>

<span data-ttu-id="14655-111">无。</span><span class="sxs-lookup"><span data-stu-id="14655-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="14655-112">父元素</span><span class="sxs-lookup"><span data-stu-id="14655-112">Parent elements</span></span>

[<span data-ttu-id="14655-113">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="14655-113">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
  
## <a name="text-value"></a><span data-ttu-id="14655-114">文本值</span><span class="sxs-lookup"><span data-stu-id="14655-114">Text value</span></span>

<span data-ttu-id="14655-115">如果**IsPermanentFailure**元素的文本值为**true，则**表示以前对邮箱项目的索引尝试未成功。</span><span class="sxs-lookup"><span data-stu-id="14655-115">A text value of **true** for the **IsPermanentFailure** element indicates that a previous attempt to index the mailbox item was unsuccessful.</span></span> <span data-ttu-id="14655-116">**如果值为 false** ，则表示之前对邮箱项目的索引尝试已成功。</span><span class="sxs-lookup"><span data-stu-id="14655-116">A value of **false** indicates that a previous attempt to index the mailbox item was successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="14655-117">备注</span><span class="sxs-lookup"><span data-stu-id="14655-117">Remarks</span></span>

<span data-ttu-id="14655-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="14655-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="14655-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="14655-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14655-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="14655-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14655-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="14655-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="14655-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="14655-122">Schema name</span></span>  <br/> |<span data-ttu-id="14655-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="14655-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="14655-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="14655-124">Validation file</span></span>  <br/> |<span data-ttu-id="14655-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="14655-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="14655-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="14655-126">Can be empty</span></span>  <br/> |<span data-ttu-id="14655-127">false</span><span class="sxs-lookup"><span data-stu-id="14655-127">false</span></span>  <br/> |
   

