---
title: PostedTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostedTime
api_type:
- schema
ms.assetid: e8b3813c-fc7e-4674-a4c6-6818c13d2bcf
description: PostedTime 元素表示 PostItem 的发布时间。 此元素是只读的。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 5fc670bfee97a46700bc4442d489696a4489f88a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459193"
---
# <a name="postedtime"></a><span data-ttu-id="5938e-105">PostedTime</span><span class="sxs-lookup"><span data-stu-id="5938e-105">PostedTime</span></span>

<span data-ttu-id="5938e-106">**PostedTime**元素表示[PostItem](postitem.md)的发布时间。</span><span class="sxs-lookup"><span data-stu-id="5938e-106">The **PostedTime** element represents the time at which a [PostItem](postitem.md) was posted.</span></span> <span data-ttu-id="5938e-107">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="5938e-107">This element is read-only.</span></span> <span data-ttu-id="5938e-108">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5938e-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PostedTime/>
```

 <span data-ttu-id="5938e-109">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="5938e-109">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5938e-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5938e-110">Attributes and elements</span></span>

<span data-ttu-id="5938e-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5938e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5938e-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="5938e-112">Attributes</span></span>

<span data-ttu-id="5938e-113">无。</span><span class="sxs-lookup"><span data-stu-id="5938e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5938e-114">子元素</span><span class="sxs-lookup"><span data-stu-id="5938e-114">Child elements</span></span>

<span data-ttu-id="5938e-115">无。</span><span class="sxs-lookup"><span data-stu-id="5938e-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5938e-116">父元素</span><span class="sxs-lookup"><span data-stu-id="5938e-116">Parent elements</span></span>

|<span data-ttu-id="5938e-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="5938e-117">**Element**</span></span>|<span data-ttu-id="5938e-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="5938e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5938e-119">PostItem</span><span class="sxs-lookup"><span data-stu-id="5938e-119">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="5938e-120">表示 Exchange 存储中的 PostItem。</span><span class="sxs-lookup"><span data-stu-id="5938e-120">Represents a PostItem in the Exchange store.</span></span> <span data-ttu-id="5938e-121">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5938e-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5938e-122">文本值</span><span class="sxs-lookup"><span data-stu-id="5938e-122">Text value</span></span>

<span data-ttu-id="5938e-123">Text 值是表示**PostItem**何时发布的 dateTime。</span><span class="sxs-lookup"><span data-stu-id="5938e-123">The text value is a dateTime that represents when a **PostItem** was posted.</span></span> <span data-ttu-id="5938e-124">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="5938e-124">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5938e-125">说明</span><span class="sxs-lookup"><span data-stu-id="5938e-125">Remarks</span></span>

<span data-ttu-id="5938e-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5938e-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5938e-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="5938e-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5938e-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="5938e-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5938e-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="5938e-129">Schema Name</span></span>  <br/> |<span data-ttu-id="5938e-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="5938e-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="5938e-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="5938e-131">Validation File</span></span>  <br/> |<span data-ttu-id="5938e-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5938e-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5938e-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="5938e-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="5938e-134">False</span><span class="sxs-lookup"><span data-stu-id="5938e-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5938e-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5938e-135">See also</span></span>



- [<span data-ttu-id="5938e-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5938e-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

