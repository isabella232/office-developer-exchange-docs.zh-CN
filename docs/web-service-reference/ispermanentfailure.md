---
title: IsPermanentFailure
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18dc3a97-cc0a-4092-934e-a6e86f52e668
description: IsPermanentFailure 元素表示索引项的上一次尝试是否成功。
ms.openlocfilehash: 39592c15394a57e1c6aa1183ed0ccedeb085e6ea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826085"
---
# <a name="ispermanentfailure"></a><span data-ttu-id="41029-103">IsPermanentFailure</span><span class="sxs-lookup"><span data-stu-id="41029-103">IsPermanentFailure</span></span>

<span data-ttu-id="41029-104">**IsPermanentFailure**元素表示索引项的上一次尝试是否成功。</span><span class="sxs-lookup"><span data-stu-id="41029-104">The **IsPermanentFailure** element indicates whether a previous attempt to index the item was unsuccessful.</span></span> 
  
```XML
<IsPermanentFailure>true | false</IsPermanentFailure>
```

 <span data-ttu-id="41029-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="41029-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41029-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41029-106">Attributes and elements</span></span>

<span data-ttu-id="41029-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41029-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41029-108">属性</span><span class="sxs-lookup"><span data-stu-id="41029-108">Attributes</span></span>

<span data-ttu-id="41029-109">无。</span><span class="sxs-lookup"><span data-stu-id="41029-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41029-110">子元素</span><span class="sxs-lookup"><span data-stu-id="41029-110">Child elements</span></span>

<span data-ttu-id="41029-111">无。</span><span class="sxs-lookup"><span data-stu-id="41029-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="41029-112">父元素</span><span class="sxs-lookup"><span data-stu-id="41029-112">Parent elements</span></span>

[<span data-ttu-id="41029-113">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="41029-113">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
  
## <a name="text-value"></a><span data-ttu-id="41029-114">文本值</span><span class="sxs-lookup"><span data-stu-id="41029-114">Text value</span></span>

<span data-ttu-id="41029-115">文本值为**true**的**IsPermanentFailure**元素表示索引邮箱项目上一次尝试成功。</span><span class="sxs-lookup"><span data-stu-id="41029-115">A text value of **true** for the **IsPermanentFailure** element indicates that a previous attempt to index the mailbox item was unsuccessful.</span></span> <span data-ttu-id="41029-116">如果值为**false**指示索引邮箱项目上一次尝试成功。</span><span class="sxs-lookup"><span data-stu-id="41029-116">A value of **false** indicates that a previous attempt to index the mailbox item was successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="41029-117">备注</span><span class="sxs-lookup"><span data-stu-id="41029-117">Remarks</span></span>

<span data-ttu-id="41029-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="41029-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="41029-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="41029-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41029-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="41029-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41029-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="41029-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="41029-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="41029-122">Schema name</span></span>  <br/> |<span data-ttu-id="41029-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="41029-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="41029-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="41029-124">Validation file</span></span>  <br/> |<span data-ttu-id="41029-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="41029-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="41029-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="41029-126">Can be empty</span></span>  <br/> |<span data-ttu-id="41029-127">false</span><span class="sxs-lookup"><span data-stu-id="41029-127">false</span></span>  <br/> |
   

