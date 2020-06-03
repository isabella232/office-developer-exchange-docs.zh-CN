---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: MinimumSize 元素表示要应用的条件或例外的邮件必须满足的最小大小。
ms.openlocfilehash: b43a8b5916747c4e3e4ca9b66cf8b9d73f5f8942
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464201"
---
# <a name="minimumsize"></a><span data-ttu-id="b738c-103">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="b738c-103">MinimumSize</span></span>

<span data-ttu-id="b738c-104">**MinimumSize**元素表示要应用的条件或例外的邮件必须满足的最小大小。</span><span class="sxs-lookup"><span data-stu-id="b738c-104">The **MinimumSize** element represents the minimum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<MinimumSize/>
```

 <span data-ttu-id="b738c-105">**int**</span><span class="sxs-lookup"><span data-stu-id="b738c-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b738c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b738c-106">Attributes and elements</span></span>

<span data-ttu-id="b738c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b738c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b738c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b738c-108">Attributes</span></span>

<span data-ttu-id="b738c-109">无。</span><span class="sxs-lookup"><span data-stu-id="b738c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b738c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b738c-110">Child elements</span></span>

<span data-ttu-id="b738c-111">无。</span><span class="sxs-lookup"><span data-stu-id="b738c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b738c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b738c-112">Parent elements</span></span>

|<span data-ttu-id="b738c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b738c-113">**Element**</span></span>|<span data-ttu-id="b738c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b738c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b738c-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="b738c-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="b738c-116">指定传入邮件必须满足的最小和最大大小，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="b738c-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b738c-117">文本值</span><span class="sxs-lookup"><span data-stu-id="b738c-117">Text value</span></span>

<span data-ttu-id="b738c-118">Text 值是一个整数，用于标识邮件的最小大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="b738c-118">The text value is an integer that identifies the minimum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b738c-119">说明</span><span class="sxs-lookup"><span data-stu-id="b738c-119">Remarks</span></span>

<span data-ttu-id="b738c-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b738c-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b738c-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="b738c-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b738c-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="b738c-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b738c-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="b738c-123">Schema Name</span></span>  <br/> |<span data-ttu-id="b738c-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="b738c-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b738c-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="b738c-125">Validation File</span></span>  <br/> |<span data-ttu-id="b738c-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b738c-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b738c-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="b738c-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="b738c-128">True</span><span class="sxs-lookup"><span data-stu-id="b738c-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b738c-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b738c-129">See also</span></span>



[<span data-ttu-id="b738c-130">MaximumSize</span><span class="sxs-lookup"><span data-stu-id="b738c-130">MaximumSize</span></span>](maximumsize.md)


- [<span data-ttu-id="b738c-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b738c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

