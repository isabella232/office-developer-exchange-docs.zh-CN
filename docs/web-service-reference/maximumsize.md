---
title: 大化
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fb7c3ab3-ef97-44c7-83e0-93cfe8c48e84
description: 大化元素均表示的条件或例外的顺序应用必须一条消息的最大大小。
ms.openlocfilehash: 37e3d377b105534fe34b54e262bd47bc450706da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826387"
---
# <a name="maximumsize"></a><span data-ttu-id="407fc-103">大化</span><span class="sxs-lookup"><span data-stu-id="407fc-103">MaximumSize</span></span>

<span data-ttu-id="407fc-104">**大化**元素均表示的条件或例外的顺序应用必须一条消息的最大大小。</span><span class="sxs-lookup"><span data-stu-id="407fc-104">The **MaximumSize** element represents the maximum size that a message must be in order for the condition or exception to apply.</span></span> 
  
```XML
<Maximum/>
```

 <span data-ttu-id="407fc-105">**int**</span><span class="sxs-lookup"><span data-stu-id="407fc-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="407fc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="407fc-106">Attributes and elements</span></span>

<span data-ttu-id="407fc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="407fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="407fc-108">属性</span><span class="sxs-lookup"><span data-stu-id="407fc-108">Attributes</span></span>

<span data-ttu-id="407fc-109">无。</span><span class="sxs-lookup"><span data-stu-id="407fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="407fc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="407fc-110">Child elements</span></span>

<span data-ttu-id="407fc-111">无。</span><span class="sxs-lookup"><span data-stu-id="407fc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="407fc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="407fc-112">Parent elements</span></span>

|<span data-ttu-id="407fc-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="407fc-113">**Element**</span></span>|<span data-ttu-id="407fc-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="407fc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="407fc-115">WithinSizeRange</span><span class="sxs-lookup"><span data-stu-id="407fc-115">WithinSizeRange</span></span>](withinsizerange.md) <br/> |<span data-ttu-id="407fc-116">指定的条件或例外的顺序应用必须传入消息的最小和最大大小。</span><span class="sxs-lookup"><span data-stu-id="407fc-116">Specifies the minimum and maximum sizes that incoming messages must be in order for the condition or exception to apply.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="407fc-117">文本值</span><span class="sxs-lookup"><span data-stu-id="407fc-117">Text value</span></span>

<span data-ttu-id="407fc-118">文本值是一个整数，标识邮件以字节为单位的最大大小。</span><span class="sxs-lookup"><span data-stu-id="407fc-118">The text value is an integer that identifies the maximum size of the message in bytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="407fc-119">备注</span><span class="sxs-lookup"><span data-stu-id="407fc-119">Remarks</span></span>

<span data-ttu-id="407fc-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="407fc-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="407fc-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="407fc-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="407fc-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="407fc-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="407fc-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="407fc-123">Schema Name</span></span>  <br/> |<span data-ttu-id="407fc-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="407fc-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="407fc-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="407fc-125">Validation File</span></span>  <br/> |<span data-ttu-id="407fc-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="407fc-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="407fc-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="407fc-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="407fc-128">True</span><span class="sxs-lookup"><span data-stu-id="407fc-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="407fc-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="407fc-129">See also</span></span>



[<span data-ttu-id="407fc-130">MinimumSize</span><span class="sxs-lookup"><span data-stu-id="407fc-130">MinimumSize</span></span>](minimumsize.md)


- [<span data-ttu-id="407fc-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="407fc-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

