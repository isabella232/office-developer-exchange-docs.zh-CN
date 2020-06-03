---
title: 状态 (MemberStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 4f8a860b-0a48-4a0d-9a7a-69a0304aa747
description: Status 元素提供有关服务器上的通讯组列表成员状态的信息。
ms.openlocfilehash: bfa0c349d6af51c1b2238c9749d2656541d31906
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465462"
---
# <a name="status-memberstatustype"></a><span data-ttu-id="c9c4f-103">状态 (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="c9c4f-103">Status (MemberStatusType)</span></span>

<span data-ttu-id="c9c4f-104">**Status**元素提供有关服务器上的通讯组列表成员状态的信息。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-104">The **Status** element provides information about the status of a distribution list member on the server.</span></span> 
  
```
<Status>Unrecognized or Normal or Demoted</Status>
```

 <span data-ttu-id="c9c4f-105">**MemberStatusType**</span><span class="sxs-lookup"><span data-stu-id="c9c4f-105">**MemberStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9c4f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c9c4f-106">Attributes and elements</span></span>

<span data-ttu-id="c9c4f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9c4f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c9c4f-108">Attributes</span></span>

<span data-ttu-id="c9c4f-109">无。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9c4f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c9c4f-110">Child elements</span></span>

<span data-ttu-id="c9c4f-111">无。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c9c4f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c9c4f-112">Parent elements</span></span>

|<span data-ttu-id="c9c4f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c9c4f-113">**Element**</span></span>|<span data-ttu-id="c9c4f-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="c9c4f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9c4f-115">Member</span><span class="sxs-lookup"><span data-stu-id="c9c4f-115">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c9c4f-116">表示一个通讯组列表的成员。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-116">Represents a member of a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c9c4f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c9c4f-117">Text value</span></span>

<span data-ttu-id="c9c4f-118">下表列出了**Status**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-118">The following table lists the possible values for the **Status** element.</span></span> 
  
<span data-ttu-id="c9c4f-119">**Status 元素值**</span><span class="sxs-lookup"><span data-stu-id="c9c4f-119">**Status element values**</span></span>

|<span data-ttu-id="c9c4f-120">**值**</span><span class="sxs-lookup"><span data-stu-id="c9c4f-120">**Value**</span></span>|<span data-ttu-id="c9c4f-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="c9c4f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9c4f-122">不</span><span class="sxs-lookup"><span data-stu-id="c9c4f-122">Unrecognized</span></span>  <br/> |<span data-ttu-id="c9c4f-123">成员信息无效或无法识别。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-123">Member information is invalid or unrecognized.</span></span>  <br/> |
|<span data-ttu-id="c9c4f-124">一般</span><span class="sxs-lookup"><span data-stu-id="c9c4f-124">Normal</span></span>  <br/> |<span data-ttu-id="c9c4f-125">通讯组列表中的成员信息与引用的对象同步。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-125">Member information in a distribution list is in sync with the referenced object.</span></span>  <br/> |
|<span data-ttu-id="c9c4f-126">降级</span><span class="sxs-lookup"><span data-stu-id="c9c4f-126">Demoted</span></span>  <br/> |<span data-ttu-id="c9c4f-127">引用的对象不可用。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-127">Referenced object is not available.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9c4f-128">备注</span><span class="sxs-lookup"><span data-stu-id="c9c4f-128">Remarks</span></span>

<span data-ttu-id="c9c4f-129">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c9c4f-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9c4f-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="c9c4f-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9c4f-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="c9c4f-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9c4f-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="c9c4f-132">Schema Name</span></span>  <br/> |<span data-ttu-id="c9c4f-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="c9c4f-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="c9c4f-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="c9c4f-134">Validation File</span></span>  <br/> |<span data-ttu-id="c9c4f-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c9c4f-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9c4f-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="c9c4f-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="c9c4f-137">False</span><span class="sxs-lookup"><span data-stu-id="c9c4f-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9c4f-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c9c4f-138">See also</span></span>



- [<span data-ttu-id="c9c4f-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c9c4f-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

