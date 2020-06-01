---
title: ProposeNewTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6d5977ac-484e-4e53-92ba-58a868eb3395
description: ProposeNewTime 元素指定响应对象，该对象指示会议与会者可以建议新的会议时间。
ms.openlocfilehash: 76f590db760826aa2cd26938947a9b0e02a603f7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465539"
---
# <a name="proposenewtime"></a><span data-ttu-id="499cd-103">ProposeNewTime</span><span class="sxs-lookup"><span data-stu-id="499cd-103">ProposeNewTime</span></span>

<span data-ttu-id="499cd-104">**ProposeNewTime**元素指定响应对象，该对象指示会议与会者可以建议新的会议时间。</span><span class="sxs-lookup"><span data-stu-id="499cd-104">The **ProposeNewTime** element specifies a response object that indicates that the meeting attendee can propose a new meeting time.</span></span> 
  
```XML
<ProposeNewTime ObjectName=""></ProposeNewTime>
```

 <span data-ttu-id="499cd-105">**ProposeNewTimeType**</span><span class="sxs-lookup"><span data-stu-id="499cd-105">**ProposeNewTimeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="499cd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="499cd-106">Attributes and elements</span></span>

<span data-ttu-id="499cd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="499cd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="499cd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="499cd-108">Attributes</span></span>

****

|<span data-ttu-id="499cd-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="499cd-109">**Attribute**</span></span>|<span data-ttu-id="499cd-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="499cd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="499cd-111">ObjectName</span><span class="sxs-lookup"><span data-stu-id="499cd-111">ObjectName</span></span>  <br/> |<span data-ttu-id="499cd-112">Response 对象的名称。</span><span class="sxs-lookup"><span data-stu-id="499cd-112">The name of the response object.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="499cd-113">子元素</span><span class="sxs-lookup"><span data-stu-id="499cd-113">Child elements</span></span>

<span data-ttu-id="499cd-114">无。</span><span class="sxs-lookup"><span data-stu-id="499cd-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="499cd-115">父元素</span><span class="sxs-lookup"><span data-stu-id="499cd-115">Parent elements</span></span>

[<span data-ttu-id="499cd-116">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="499cd-116">ResponseObjects</span></span>](responseobjects.md)
  
## <a name="remarks"></a><span data-ttu-id="499cd-117">说明</span><span class="sxs-lookup"><span data-stu-id="499cd-117">Remarks</span></span>

<span data-ttu-id="499cd-118">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="499cd-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="499cd-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="499cd-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="499cd-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="499cd-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="499cd-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="499cd-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="499cd-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="499cd-122">Schema Name</span></span>  <br/> |<span data-ttu-id="499cd-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="499cd-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="499cd-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="499cd-124">Validation File</span></span>  <br/> |<span data-ttu-id="499cd-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="499cd-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="499cd-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="499cd-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="499cd-127">True</span><span class="sxs-lookup"><span data-stu-id="499cd-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="499cd-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="499cd-128">See also</span></span>



[<span data-ttu-id="499cd-129">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="499cd-129">ResponseObjects</span></span>](responseobjects.md)


- [<span data-ttu-id="499cd-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="499cd-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

