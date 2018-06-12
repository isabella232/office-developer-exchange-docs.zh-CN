---
title: ErrorMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cec33a6-4b10-4259-8ac3-3f39a642b34c
description: ErrorMessage 元素均表示验证错误的原因。
ms.openlocfilehash: d1869041254ef7c661fb2acb7c9c2ccaf628b394
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754158"
---
# <a name="errormessage"></a><span data-ttu-id="f218b-103">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="f218b-103">ErrorMessage</span></span>

<span data-ttu-id="f218b-104">**ErrorMessage**元素均表示验证错误的原因。</span><span class="sxs-lookup"><span data-stu-id="f218b-104">The **ErrorMessage** element represents the reason for the validation error.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="f218b-105">**字符串**</span><span class="sxs-lookup"><span data-stu-id="f218b-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f218b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f218b-106">Attributes and elements</span></span>

<span data-ttu-id="f218b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f218b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f218b-108">属性</span><span class="sxs-lookup"><span data-stu-id="f218b-108">Attributes</span></span>

<span data-ttu-id="f218b-109">无。</span><span class="sxs-lookup"><span data-stu-id="f218b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f218b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f218b-110">Child elements</span></span>

<span data-ttu-id="f218b-111">无。</span><span class="sxs-lookup"><span data-stu-id="f218b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f218b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f218b-112">Parent elements</span></span>

|<span data-ttu-id="f218b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f218b-113">**Element**</span></span>|<span data-ttu-id="f218b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f218b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f218b-115">Error</span><span class="sxs-lookup"><span data-stu-id="f218b-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="f218b-116">代表对特定规则属性值、 谓词属性值或 action 属性值的单个验证错误。</span><span class="sxs-lookup"><span data-stu-id="f218b-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f218b-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f218b-117">Text value</span></span>

<span data-ttu-id="f218b-118">使用规则验证错误关联的错误消息。</span><span class="sxs-lookup"><span data-stu-id="f218b-118">The error message associated with the rule validation error.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f218b-119">备注</span><span class="sxs-lookup"><span data-stu-id="f218b-119">Remarks</span></span>

<span data-ttu-id="f218b-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f218b-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f218b-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="f218b-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f218b-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="f218b-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f218b-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="f218b-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f218b-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="f218b-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f218b-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="f218b-125">Validation File</span></span>  <br/> |<span data-ttu-id="f218b-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f218b-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f218b-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="f218b-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f218b-128">True</span><span class="sxs-lookup"><span data-stu-id="f218b-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f218b-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f218b-129">See also</span></span>



- [<span data-ttu-id="f218b-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f218b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

