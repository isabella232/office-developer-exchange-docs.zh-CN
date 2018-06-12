---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: MinimumSize 元素均表示最小大小的条件或例外的顺序应用必须一条消息。
ms.openlocfilehash: 4f80bac3b9226019ec3d726cd2d6430e02cac423
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826480"
---
# <a name="minimumsize"></a><span data-ttu-id="310e7-103">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="310e7-103">MinimumSize</span></span>

<span data-ttu-id="310e7-104">**MinimumSize**元素均表示最小大小的条件或例外的顺序应用必须一条消息。</span><span class="sxs-lookup"><span data-stu-id="310e7-104">The **MinimumSize** element represents the minimum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<MinimumSize/>
```

 <span data-ttu-id="310e7-105">**int**</span><span class="sxs-lookup"><span data-stu-id="310e7-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="310e7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="310e7-106">Attributes and elements</span></span>

<span data-ttu-id="310e7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="310e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="310e7-108">属性</span><span class="sxs-lookup"><span data-stu-id="310e7-108">Attributes</span></span>

<span data-ttu-id="310e7-109">无。</span><span class="sxs-lookup"><span data-stu-id="310e7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="310e7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="310e7-110">Child elements</span></span>

<span data-ttu-id="310e7-111">无。</span><span class="sxs-lookup"><span data-stu-id="310e7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="310e7-112">父元素</span><span class="sxs-lookup"><span data-stu-id="310e7-112">Parent elements</span></span>

|<span data-ttu-id="310e7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="310e7-113">**Element**</span></span>|<span data-ttu-id="310e7-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="310e7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="310e7-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="310e7-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="310e7-116">指定的条件或例外的顺序应用必须传入消息的最小和最大大小。</span><span class="sxs-lookup"><span data-stu-id="310e7-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="310e7-117">文本值</span><span class="sxs-lookup"><span data-stu-id="310e7-117">Text value</span></span>

<span data-ttu-id="310e7-118">文本值是邮件的一个标识以字节为单位的最小整数。</span><span class="sxs-lookup"><span data-stu-id="310e7-118">The text value is an integer that identifies the minimum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="310e7-119">备注</span><span class="sxs-lookup"><span data-stu-id="310e7-119">Remarks</span></span>

<span data-ttu-id="310e7-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="310e7-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="310e7-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="310e7-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="310e7-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="310e7-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="310e7-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="310e7-123">Schema Name</span></span>  <br/> |<span data-ttu-id="310e7-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="310e7-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="310e7-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="310e7-125">Validation File</span></span>  <br/> |<span data-ttu-id="310e7-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="310e7-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="310e7-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="310e7-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="310e7-128">True</span><span class="sxs-lookup"><span data-stu-id="310e7-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="310e7-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="310e7-129">See also</span></span>



[<span data-ttu-id="310e7-130">大化</span><span class="sxs-lookup"><span data-stu-id="310e7-130">MaximumSize</span></span>](maximumsize.md)


- [<span data-ttu-id="310e7-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="310e7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

