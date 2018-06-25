---
title: 解决方案
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Resolution
api_type:
- schema
ms.assetid: 573bed4b-d7b1-4baf-b16f-0795cdebf1a7
description: 解决方案元素包含一个解析的实体。
ms.openlocfilehash: d65f6401e54a4397cad1bfcc85384f644fbae405
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827156"
---
# <a name="resolution"></a><span data-ttu-id="a89fe-103">解决方案</span><span class="sxs-lookup"><span data-stu-id="a89fe-103">Resolution</span></span>

<span data-ttu-id="a89fe-104">**解决方案**元素包含一个解析的实体。</span><span class="sxs-lookup"><span data-stu-id="a89fe-104">The **Resolution** element contains a single resolved entity.</span></span> 
  
[<span data-ttu-id="a89fe-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="a89fe-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="a89fe-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a89fe-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="a89fe-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a89fe-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="a89fe-108">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="a89fe-108">ResolutionSet</span></span>](resolutionset.md)
  
[<span data-ttu-id="a89fe-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="a89fe-109">Resolution</span></span>](resolution.md)
  
```xml
<Resolution>
   <Mailbox/>
   <Contact/>
</Resolution>
```

 <span data-ttu-id="a89fe-110">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="a89fe-110">**ResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a89fe-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a89fe-111">Attributes and elements</span></span>

<span data-ttu-id="a89fe-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a89fe-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a89fe-113">属性</span><span class="sxs-lookup"><span data-stu-id="a89fe-113">Attributes</span></span>

<span data-ttu-id="a89fe-114">无。</span><span class="sxs-lookup"><span data-stu-id="a89fe-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a89fe-115">子元素</span><span class="sxs-lookup"><span data-stu-id="a89fe-115">Child elements</span></span>

|<span data-ttu-id="a89fe-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a89fe-116">**Element**</span></span>|<span data-ttu-id="a89fe-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a89fe-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a89fe-118">Mailbox</span><span class="sxs-lookup"><span data-stu-id="a89fe-118">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="a89fe-119">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="a89fe-119">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
|[<span data-ttu-id="a89fe-120">联系人</span><span class="sxs-lookup"><span data-stu-id="a89fe-120">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="a89fe-121">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="a89fe-121">Represents an Exchange contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a89fe-122">父元素</span><span class="sxs-lookup"><span data-stu-id="a89fe-122">Parent elements</span></span>

|<span data-ttu-id="a89fe-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="a89fe-123">**Element**</span></span>|<span data-ttu-id="a89fe-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="a89fe-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a89fe-125">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="a89fe-125">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="a89fe-126">包含的不明确名称解析的数组。</span><span class="sxs-lookup"><span data-stu-id="a89fe-126">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a89fe-127">备注</span><span class="sxs-lookup"><span data-stu-id="a89fe-127">Remarks</span></span>

<span data-ttu-id="a89fe-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a89fe-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a89fe-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="a89fe-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a89fe-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="a89fe-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a89fe-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="a89fe-131">Schema name</span></span>  <br/> |<span data-ttu-id="a89fe-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="a89fe-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="a89fe-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="a89fe-133">Validation file</span></span>  <br/> |<span data-ttu-id="a89fe-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a89fe-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a89fe-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="a89fe-135">Can be empty</span></span>  <br/> |<span data-ttu-id="a89fe-136">False</span><span class="sxs-lookup"><span data-stu-id="a89fe-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a89fe-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a89fe-137">See also</span></span>



[<span data-ttu-id="a89fe-138">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="a89fe-138">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="a89fe-139">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="a89fe-139">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="a89fe-140">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="a89fe-140">ResolveNames operation</span></span>](resolvenames-operation.md)

