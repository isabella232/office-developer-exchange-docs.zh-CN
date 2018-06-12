---
title: Guid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 49dcf69f-bf8d-4be6-a24c-03bbd13f4fe5
description: Guid 元素指定邮箱的全局唯一标识符。
ms.openlocfilehash: 35307a706523fc5c2916767c7508dec07deb8d09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825799"
---
# <a name="guid"></a><span data-ttu-id="acad5-103">Guid</span><span class="sxs-lookup"><span data-stu-id="acad5-103">Guid</span></span>

<span data-ttu-id="acad5-104">**Guid**元素指定邮箱的全局唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="acad5-104">The **Guid** element specifies the globally unique identifier of the mailbox.</span></span> 
  
```XML
<Guid></Guid>
```

 <span data-ttu-id="acad5-105">**GuidType**</span><span class="sxs-lookup"><span data-stu-id="acad5-105">**GuidType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="acad5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="acad5-106">Attributes and elements</span></span>

<span data-ttu-id="acad5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="acad5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acad5-108">属性</span><span class="sxs-lookup"><span data-stu-id="acad5-108">Attributes</span></span>

<span data-ttu-id="acad5-109">无。</span><span class="sxs-lookup"><span data-stu-id="acad5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acad5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="acad5-110">Child elements</span></span>

<span data-ttu-id="acad5-111">无。</span><span class="sxs-lookup"><span data-stu-id="acad5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="acad5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="acad5-112">Parent elements</span></span>

|<span data-ttu-id="acad5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="acad5-113">**Element**</span></span>|<span data-ttu-id="acad5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="acad5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acad5-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="acad5-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="acad5-116">指定从**GetSearchableMailboxes**请求返回的邮箱。</span><span class="sxs-lookup"><span data-stu-id="acad5-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="acad5-117">文本值</span><span class="sxs-lookup"><span data-stu-id="acad5-117">Text value</span></span>

<span data-ttu-id="acad5-118">**Guid**元素的文本值是 GUID 值，该值唯一地标识邮箱。</span><span class="sxs-lookup"><span data-stu-id="acad5-118">The text value of the **Guid** element is a GUID value that uniquely identifies a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="acad5-119">备注</span><span class="sxs-lookup"><span data-stu-id="acad5-119">Remarks</span></span>

<span data-ttu-id="acad5-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="acad5-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="acad5-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="acad5-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acad5-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="acad5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acad5-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="acad5-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="acad5-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="acad5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="acad5-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="acad5-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="acad5-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="acad5-126">Validation File</span></span>  <br/> |<span data-ttu-id="acad5-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="acad5-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="acad5-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="acad5-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="acad5-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="acad5-129">See also</span></span>



- [<span data-ttu-id="acad5-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="acad5-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
