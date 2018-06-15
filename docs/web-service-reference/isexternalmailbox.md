---
title: IsExternalMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5cc83174-e684-42c8-b72a-f82d3de3bb2f
description: IsExternalMailbox元素指示该邮箱是否对组织外部。
ms.openlocfilehash: cf9f71e9b955cffd1bebefd5f23acba66ba1b894
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2018
ms.locfileid: "19826010"
---
# <a name="isexternalmailbox"></a><span data-ttu-id="f4af5-103">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="f4af5-103">IsExternalMailbox</span></span>

<span data-ttu-id="f4af5-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **IsExternalMailbox**元素指示该邮箱是否对组织外部。</span><span class="sxs-lookup"><span data-stu-id="f4af5-104">The **IsExternalMailbox** element indicates whether the mailbox is external to the organization.</span></span> 
  
```XML
<IsExternalMailbox>true | false</IsExternalMailbox>
```

 <span data-ttu-id="f4af5-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f4af5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4af5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f4af5-106">Attributes and elements</span></span>

<span data-ttu-id="f4af5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f4af5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4af5-108">属性</span><span class="sxs-lookup"><span data-stu-id="f4af5-108">Attributes</span></span>

<span data-ttu-id="f4af5-109">无。</span><span class="sxs-lookup"><span data-stu-id="f4af5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4af5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f4af5-110">Child elements</span></span>

<span data-ttu-id="f4af5-111">无。</span><span class="sxs-lookup"><span data-stu-id="f4af5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f4af5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f4af5-112">Parent elements</span></span>

[<span data-ttu-id="f4af5-113">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="f4af5-113">SearchableMailbox</span></span>](searchablemailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="f4af5-114">文本值</span><span class="sxs-lookup"><span data-stu-id="f4af5-114">Text value</span></span>

<span data-ttu-id="f4af5-p101">**true** **IsExternalMailbox**元素的文本值指示该邮箱位于外部组织。 **false**表示邮箱是组织中。</span><span class="sxs-lookup"><span data-stu-id="f4af5-p101">A text value of **true** for the **IsExternalMailbox** element indicates that the mailbox is in an external organization. A value of **false** indicates that the mailbox is in the organization.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f4af5-117">备注</span><span class="sxs-lookup"><span data-stu-id="f4af5-117">Remarks</span></span>

<span data-ttu-id="f4af5-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f4af5-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f4af5-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f4af5-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4af5-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="f4af5-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4af5-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="f4af5-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f4af5-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="f4af5-122">Schema name</span></span>  <br/> |<span data-ttu-id="f4af5-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="f4af5-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="f4af5-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="f4af5-124">Validation file</span></span>  <br/> |<span data-ttu-id="f4af5-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f4af5-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f4af5-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="f4af5-126">Can be empty</span></span>  <br/> |<span data-ttu-id="f4af5-127">False</span><span class="sxs-lookup"><span data-stu-id="f4af5-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4af5-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f4af5-128">See also</span></span>



- [<span data-ttu-id="f4af5-129">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f4af5-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

