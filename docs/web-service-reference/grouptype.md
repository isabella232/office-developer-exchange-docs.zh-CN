---
title: GroupType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c31552f-22b8-4bf0-8cac-046fd92ac0d4
description: GroupType 元素指定组类的即时消息 (IM) 组。
ms.openlocfilehash: 330a1567ce85877ba73c6205898ea66b59585e16
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825800"
---
# <a name="grouptype"></a><span data-ttu-id="fa5de-103">GroupType</span><span class="sxs-lookup"><span data-stu-id="fa5de-103">GroupType</span></span>

<span data-ttu-id="fa5de-104">**GroupType**元素指定组类的即时消息 (IM) 组。</span><span class="sxs-lookup"><span data-stu-id="fa5de-104">The **GroupType** element specifies the group class of an instant messaging (IM) group.</span></span> 
  
```XML
<GroupType></GroupType>
```

 <span data-ttu-id="fa5de-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="fa5de-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa5de-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa5de-106">Attributes and elements</span></span>

<span data-ttu-id="fa5de-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa5de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa5de-108">属性</span><span class="sxs-lookup"><span data-stu-id="fa5de-108">Attributes</span></span>

<span data-ttu-id="fa5de-109">无。</span><span class="sxs-lookup"><span data-stu-id="fa5de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa5de-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fa5de-110">Child elements</span></span>

<span data-ttu-id="fa5de-111">无。</span><span class="sxs-lookup"><span data-stu-id="fa5de-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa5de-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fa5de-112">Parent elements</span></span>

|<span data-ttu-id="fa5de-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa5de-113">**Element**</span></span>|<span data-ttu-id="fa5de-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa5de-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa5de-115">ImGroup</span><span class="sxs-lookup"><span data-stu-id="fa5de-115">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="fa5de-116">代表一个即时消息的组。</span><span class="sxs-lookup"><span data-stu-id="fa5de-116">Represents an instant messaging group.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa5de-117">文本值</span><span class="sxs-lookup"><span data-stu-id="fa5de-117">Text value</span></span>

<span data-ttu-id="fa5de-118">**GroupType**元素的文本值是一个字符串值，指定组的类型。</span><span class="sxs-lookup"><span data-stu-id="fa5de-118">The text value of the **GroupType** element is a string value that specifies type of the group.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa5de-119">备注</span><span class="sxs-lookup"><span data-stu-id="fa5de-119">Remarks</span></span>

<span data-ttu-id="fa5de-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fa5de-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa5de-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fa5de-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa5de-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa5de-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa5de-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa5de-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa5de-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa5de-124">Schema Name</span></span>  <br/> |<span data-ttu-id="fa5de-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="fa5de-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="fa5de-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa5de-126">Validation File</span></span>  <br/> |<span data-ttu-id="fa5de-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa5de-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa5de-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa5de-128">Can Be Empty</span></span>  <br/> |<span data-ttu-id="fa5de-129">False</span><span class="sxs-lookup"><span data-stu-id="fa5de-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa5de-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa5de-130">See also</span></span>



- [<span data-ttu-id="fa5de-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fa5de-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

