---
title: GroupType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c31552f-22b8-4bf0-8cac-046fd92ac0d4
description: GroupType 元素指定即时消息（IM）组的组类。
ms.openlocfilehash: b8790a23507c51dfffceaddf3641ce820223c366
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462799"
---
# <a name="grouptype"></a><span data-ttu-id="c4e40-103">GroupType</span><span class="sxs-lookup"><span data-stu-id="c4e40-103">GroupType</span></span>

<span data-ttu-id="c4e40-104">**GroupType**元素指定即时消息（IM）组的组类。</span><span class="sxs-lookup"><span data-stu-id="c4e40-104">The **GroupType** element specifies the group class of an instant messaging (IM) group.</span></span> 
  
```XML
<GroupType></GroupType>
```

 <span data-ttu-id="c4e40-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="c4e40-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4e40-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c4e40-106">Attributes and elements</span></span>

<span data-ttu-id="c4e40-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c4e40-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4e40-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c4e40-108">Attributes</span></span>

<span data-ttu-id="c4e40-109">无。</span><span class="sxs-lookup"><span data-stu-id="c4e40-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c4e40-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c4e40-110">Child elements</span></span>

<span data-ttu-id="c4e40-111">无。</span><span class="sxs-lookup"><span data-stu-id="c4e40-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c4e40-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c4e40-112">Parent elements</span></span>

|<span data-ttu-id="c4e40-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c4e40-113">**Element**</span></span>|<span data-ttu-id="c4e40-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c4e40-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c4e40-115">ImGroup</span><span class="sxs-lookup"><span data-stu-id="c4e40-115">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="c4e40-116">表示即时消息组。</span><span class="sxs-lookup"><span data-stu-id="c4e40-116">Represents an instant messaging group.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c4e40-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c4e40-117">Text value</span></span>

<span data-ttu-id="c4e40-118">**GroupType**元素的文本值是一个 string 值，用于指定组的类型。</span><span class="sxs-lookup"><span data-stu-id="c4e40-118">The text value of the **GroupType** element is a string value that specifies type of the group.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c4e40-119">备注</span><span class="sxs-lookup"><span data-stu-id="c4e40-119">Remarks</span></span>

<span data-ttu-id="c4e40-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c4e40-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c4e40-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c4e40-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4e40-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="c4e40-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4e40-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="c4e40-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4e40-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="c4e40-124">Schema Name</span></span>  <br/> |<span data-ttu-id="c4e40-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="c4e40-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="c4e40-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="c4e40-126">Validation File</span></span>  <br/> |<span data-ttu-id="c4e40-127">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="c4e40-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4e40-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="c4e40-128">Can Be Empty</span></span>  <br/> |<span data-ttu-id="c4e40-129">False</span><span class="sxs-lookup"><span data-stu-id="c4e40-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4e40-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4e40-130">See also</span></span>



- [<span data-ttu-id="c4e40-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c4e40-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

