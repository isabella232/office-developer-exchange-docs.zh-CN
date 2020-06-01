---
title: Office.mailboxenums.bodytype （BodyTypeType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d730e3af-3102-4242-a2f1-c2873af188f9
description: Office.mailboxenums.bodytype 元素指定项的正文的类型。
ms.openlocfilehash: e9e09ea01477558f3a12abbee3d028b9268ac7eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461504"
---
# <a name="bodytype-bodytypetype"></a><span data-ttu-id="31dc0-103">Office.mailboxenums.bodytype （BodyTypeType）</span><span class="sxs-lookup"><span data-stu-id="31dc0-103">BodyType (BodyTypeType)</span></span>

<span data-ttu-id="31dc0-104">**Office.mailboxenums.bodytype**元素指定项的正文的类型。</span><span class="sxs-lookup"><span data-stu-id="31dc0-104">The **BodyType** element specifies the type of the body of the item.</span></span> 
  
```XML
<BodyType> HTML | Text</BodyType>
```

 <span data-ttu-id="31dc0-105">**BodyTypeType**</span><span class="sxs-lookup"><span data-stu-id="31dc0-105">**BodyTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31dc0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="31dc0-106">Attributes and elements</span></span>

<span data-ttu-id="31dc0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="31dc0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31dc0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="31dc0-108">Attributes</span></span>

<span data-ttu-id="31dc0-109">无。</span><span class="sxs-lookup"><span data-stu-id="31dc0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31dc0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="31dc0-110">Child elements</span></span>

<span data-ttu-id="31dc0-111">无。</span><span class="sxs-lookup"><span data-stu-id="31dc0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31dc0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="31dc0-112">Parent elements</span></span>

|<span data-ttu-id="31dc0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="31dc0-113">**Element**</span></span>|<span data-ttu-id="31dc0-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="31dc0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31dc0-115">Body</span><span class="sxs-lookup"><span data-stu-id="31dc0-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="31dc0-116">指定项的正文。</span><span class="sxs-lookup"><span data-stu-id="31dc0-116">Specifies the body of an item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31dc0-117">文本值</span><span class="sxs-lookup"><span data-stu-id="31dc0-117">Text value</span></span>

<span data-ttu-id="31dc0-118">**Office.mailboxenums.bodytype 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="31dc0-118">**BodyType element text values**</span></span>

|<span data-ttu-id="31dc0-119">**值**</span><span class="sxs-lookup"><span data-stu-id="31dc0-119">**Value**</span></span>|<span data-ttu-id="31dc0-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="31dc0-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31dc0-121">HTML</span><span class="sxs-lookup"><span data-stu-id="31dc0-121">HTML</span></span>  <br/> |<span data-ttu-id="31dc0-122">指示正文为 HTML。</span><span class="sxs-lookup"><span data-stu-id="31dc0-122">Indicates that the body is HTML.</span></span>  <br/> |
|<span data-ttu-id="31dc0-123">文本</span><span class="sxs-lookup"><span data-stu-id="31dc0-123">Text</span></span>  <br/> |<span data-ttu-id="31dc0-124">指示正文为文本。</span><span class="sxs-lookup"><span data-stu-id="31dc0-124">Indicates that the body is text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31dc0-125">备注</span><span class="sxs-lookup"><span data-stu-id="31dc0-125">Remarks</span></span>

<span data-ttu-id="31dc0-126">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="31dc0-126">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="31dc0-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="31dc0-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31dc0-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="31dc0-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31dc0-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="31dc0-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31dc0-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="31dc0-130">Schema Name</span></span>  <br/> |<span data-ttu-id="31dc0-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="31dc0-131">Type schema</span></span>  <br/> |
|<span data-ttu-id="31dc0-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="31dc0-132">Validation File</span></span>  <br/> |<span data-ttu-id="31dc0-133">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="31dc0-133">types.xsd</span></span>  <br/> |
|<span data-ttu-id="31dc0-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="31dc0-134">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="31dc0-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="31dc0-135">See also</span></span>



- [<span data-ttu-id="31dc0-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="31dc0-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

