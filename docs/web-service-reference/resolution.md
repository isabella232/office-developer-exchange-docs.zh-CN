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
description: 解析元素包含一个已解析的实体。
ms.openlocfilehash: 63c80f3c8d7dabf7e6dc1494df04c0be821b28bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468283"
---
# <a name="resolution"></a><span data-ttu-id="73d04-103">解决方案</span><span class="sxs-lookup"><span data-stu-id="73d04-103">Resolution</span></span>

<span data-ttu-id="73d04-104">**解析**元素包含一个已解析的实体。</span><span class="sxs-lookup"><span data-stu-id="73d04-104">The **Resolution** element contains a single resolved entity.</span></span> 
  
[<span data-ttu-id="73d04-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="73d04-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="73d04-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="73d04-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="73d04-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="73d04-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="73d04-108">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="73d04-108">ResolutionSet</span></span>](resolutionset.md)
  
[<span data-ttu-id="73d04-109">解决方案</span><span class="sxs-lookup"><span data-stu-id="73d04-109">Resolution</span></span>](resolution.md)
  
```xml
<Resolution>
   <Mailbox/>
   <Contact/>
</Resolution>
```

 <span data-ttu-id="73d04-110">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="73d04-110">**ResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73d04-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="73d04-111">Attributes and elements</span></span>

<span data-ttu-id="73d04-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="73d04-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73d04-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="73d04-113">Attributes</span></span>

<span data-ttu-id="73d04-114">无。</span><span class="sxs-lookup"><span data-stu-id="73d04-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73d04-115">子元素</span><span class="sxs-lookup"><span data-stu-id="73d04-115">Child elements</span></span>

|<span data-ttu-id="73d04-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="73d04-116">**Element**</span></span>|<span data-ttu-id="73d04-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="73d04-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73d04-118">Mailbox</span><span class="sxs-lookup"><span data-stu-id="73d04-118">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="73d04-119">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="73d04-119">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
|[<span data-ttu-id="73d04-120">Contact</span><span class="sxs-lookup"><span data-stu-id="73d04-120">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="73d04-121">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="73d04-121">Represents an Exchange contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="73d04-122">父元素</span><span class="sxs-lookup"><span data-stu-id="73d04-122">Parent elements</span></span>

|<span data-ttu-id="73d04-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="73d04-123">**Element**</span></span>|<span data-ttu-id="73d04-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="73d04-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73d04-125">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="73d04-125">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="73d04-126">包含一个不明确名称的分辨率数组。</span><span class="sxs-lookup"><span data-stu-id="73d04-126">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73d04-127">说明</span><span class="sxs-lookup"><span data-stu-id="73d04-127">Remarks</span></span>

<span data-ttu-id="73d04-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="73d04-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73d04-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="73d04-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73d04-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="73d04-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="73d04-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="73d04-131">Schema name</span></span>  <br/> |<span data-ttu-id="73d04-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="73d04-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="73d04-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="73d04-133">Validation file</span></span>  <br/> |<span data-ttu-id="73d04-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="73d04-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="73d04-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="73d04-135">Can be empty</span></span>  <br/> |<span data-ttu-id="73d04-136">False</span><span class="sxs-lookup"><span data-stu-id="73d04-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73d04-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="73d04-137">See also</span></span>



[<span data-ttu-id="73d04-138">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="73d04-138">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="73d04-139">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="73d04-139">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="73d04-140">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="73d04-140">ResolveNames operation</span></span>](resolvenames-operation.md)

