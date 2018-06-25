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
description: Status 元素提供状态信息的通讯组列表成员服务器上。
ms.openlocfilehash: ef062433c80f0cca413c33012e1164b17e226faf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827580"
---
# <a name="status-memberstatustype"></a><span data-ttu-id="4872d-103">状态 (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="4872d-103">Status (MemberStatusType)</span></span>

<span data-ttu-id="4872d-104">**Status**元素提供状态信息的通讯组列表成员服务器上。</span><span class="sxs-lookup"><span data-stu-id="4872d-104">The **Status** element provides information about the status of a distribution list member on the server.</span></span> 
  
```
<Status>Unrecognized or Normal or Demoted</Status>
```

 <span data-ttu-id="4872d-105">**MemberStatusType**</span><span class="sxs-lookup"><span data-stu-id="4872d-105">**MemberStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4872d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4872d-106">Attributes and elements</span></span>

<span data-ttu-id="4872d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4872d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4872d-108">属性</span><span class="sxs-lookup"><span data-stu-id="4872d-108">Attributes</span></span>

<span data-ttu-id="4872d-109">无。</span><span class="sxs-lookup"><span data-stu-id="4872d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4872d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4872d-110">Child elements</span></span>

<span data-ttu-id="4872d-111">无。</span><span class="sxs-lookup"><span data-stu-id="4872d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4872d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4872d-112">Parent elements</span></span>

|<span data-ttu-id="4872d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4872d-113">**Element**</span></span>|<span data-ttu-id="4872d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4872d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4872d-115">Member</span><span class="sxs-lookup"><span data-stu-id="4872d-115">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4872d-116">表示一个通讯组列表的成员。</span><span class="sxs-lookup"><span data-stu-id="4872d-116">Represents a member of a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4872d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="4872d-117">Text value</span></span>

<span data-ttu-id="4872d-118">下表列出了**Status**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="4872d-118">The following table lists the possible values for the **Status** element.</span></span> 
  
<span data-ttu-id="4872d-119">**状态元素的值**</span><span class="sxs-lookup"><span data-stu-id="4872d-119">**Status element values**</span></span>

|<span data-ttu-id="4872d-120">**值**</span><span class="sxs-lookup"><span data-stu-id="4872d-120">**Value**</span></span>|<span data-ttu-id="4872d-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="4872d-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4872d-122">无法识别</span><span class="sxs-lookup"><span data-stu-id="4872d-122">Unrecognized</span></span>  <br/> |<span data-ttu-id="4872d-123">成员信息是无效或无法识别。</span><span class="sxs-lookup"><span data-stu-id="4872d-123">Member information is invalid or unrecognized.</span></span>  <br/> |
|<span data-ttu-id="4872d-124">常规</span><span class="sxs-lookup"><span data-stu-id="4872d-124">Normal</span></span>  <br/> |<span data-ttu-id="4872d-125">与引用的对象同步通讯组列表中的成员身份信息。</span><span class="sxs-lookup"><span data-stu-id="4872d-125">Member information in a distribution list is in sync with the referenced object.</span></span>  <br/> |
|<span data-ttu-id="4872d-126">降级</span><span class="sxs-lookup"><span data-stu-id="4872d-126">Demoted</span></span>  <br/> |<span data-ttu-id="4872d-127">引用的对象不可用。</span><span class="sxs-lookup"><span data-stu-id="4872d-127">Referenced object is not available.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4872d-128">注解</span><span class="sxs-lookup"><span data-stu-id="4872d-128">Remarks</span></span>

<span data-ttu-id="4872d-129">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4872d-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4872d-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="4872d-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4872d-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="4872d-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4872d-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="4872d-132">Schema Name</span></span>  <br/> |<span data-ttu-id="4872d-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="4872d-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="4872d-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="4872d-134">Validation File</span></span>  <br/> |<span data-ttu-id="4872d-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4872d-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4872d-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="4872d-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="4872d-137">False</span><span class="sxs-lookup"><span data-stu-id="4872d-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4872d-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4872d-138">See also</span></span>



- [<span data-ttu-id="4872d-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4872d-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

