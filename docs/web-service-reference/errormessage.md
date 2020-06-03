---
title: ErrorMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cec33a6-4b10-4259-8ac3-3f39a642b34c
description: ErrorMessage 元素表示验证错误的原因。
ms.openlocfilehash: a35dc6af12e71c8437c13024a254000e8f477a15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526191"
---
# <a name="errormessage"></a><span data-ttu-id="59f35-103">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="59f35-103">ErrorMessage</span></span>

<span data-ttu-id="59f35-104">**ErrorMessage**元素表示验证错误的原因。</span><span class="sxs-lookup"><span data-stu-id="59f35-104">The **ErrorMessage** element represents the reason for the validation error.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="59f35-105">**String**</span><span class="sxs-lookup"><span data-stu-id="59f35-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59f35-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="59f35-106">Attributes and elements</span></span>

<span data-ttu-id="59f35-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="59f35-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59f35-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="59f35-108">Attributes</span></span>

<span data-ttu-id="59f35-109">无。</span><span class="sxs-lookup"><span data-stu-id="59f35-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59f35-110">子元素</span><span class="sxs-lookup"><span data-stu-id="59f35-110">Child elements</span></span>

<span data-ttu-id="59f35-111">无。</span><span class="sxs-lookup"><span data-stu-id="59f35-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="59f35-112">父元素</span><span class="sxs-lookup"><span data-stu-id="59f35-112">Parent elements</span></span>

|<span data-ttu-id="59f35-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="59f35-113">**Element**</span></span>|<span data-ttu-id="59f35-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="59f35-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59f35-115">Error</span><span class="sxs-lookup"><span data-stu-id="59f35-115">Error</span></span>](error.md) <br/> |<span data-ttu-id="59f35-116">表示特定规则属性值、谓词属性值或 action 属性值上的单个验证错误。</span><span class="sxs-lookup"><span data-stu-id="59f35-116">Represents a single validation error on a particular rule property value, predicate property value, or action property value.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="59f35-117">文本值</span><span class="sxs-lookup"><span data-stu-id="59f35-117">Text value</span></span>

<span data-ttu-id="59f35-118">与规则验证错误关联的错误消息。</span><span class="sxs-lookup"><span data-stu-id="59f35-118">The error message associated with the rule validation error.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59f35-119">说明</span><span class="sxs-lookup"><span data-stu-id="59f35-119">Remarks</span></span>

<span data-ttu-id="59f35-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="59f35-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59f35-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="59f35-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59f35-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="59f35-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="59f35-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="59f35-123">Schema Name</span></span>  <br/> |<span data-ttu-id="59f35-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="59f35-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="59f35-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="59f35-125">Validation File</span></span>  <br/> |<span data-ttu-id="59f35-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="59f35-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="59f35-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="59f35-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="59f35-128">True</span><span class="sxs-lookup"><span data-stu-id="59f35-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59f35-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="59f35-129">See also</span></span>



- [<span data-ttu-id="59f35-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="59f35-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

