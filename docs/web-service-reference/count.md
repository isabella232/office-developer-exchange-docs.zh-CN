---
title: Count
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Count
api_type:
- schema
ms.assetid: 68314b4a-1e17-4e21-9c2e-224d70ef7a32
description: Count 元素包含 UpdateItem 操作响应中的冲突数。
ms.openlocfilehash: a43896a1b8b6a9d96ab02afe64f9e553639e478e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466757"
---
# <a name="count"></a><span data-ttu-id="14cf9-103">Count</span><span class="sxs-lookup"><span data-stu-id="14cf9-103">Count</span></span>

<span data-ttu-id="14cf9-104">[Count](count.md)元素包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突数。</span><span class="sxs-lookup"><span data-stu-id="14cf9-104">The [Count](count.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
[<span data-ttu-id="14cf9-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="14cf9-105">UpdateItemResponse</span></span>](updateitemresponse.md)
  
[<span data-ttu-id="14cf9-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="14cf9-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="14cf9-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="14cf9-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
[<span data-ttu-id="14cf9-108">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="14cf9-108">ConflictResults</span></span>](conflictresults.md)
  
[<span data-ttu-id="14cf9-109">Count</span><span class="sxs-lookup"><span data-stu-id="14cf9-109">Count</span></span>](count.md)
  
```xml
<Count/>
```

 <span data-ttu-id="14cf9-110">**int**</span><span class="sxs-lookup"><span data-stu-id="14cf9-110">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14cf9-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="14cf9-111">Attributes and elements</span></span>

<span data-ttu-id="14cf9-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="14cf9-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14cf9-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="14cf9-113">Attributes</span></span>

<span data-ttu-id="14cf9-114">无。</span><span class="sxs-lookup"><span data-stu-id="14cf9-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14cf9-115">子元素</span><span class="sxs-lookup"><span data-stu-id="14cf9-115">Child elements</span></span>

<span data-ttu-id="14cf9-116">无。</span><span class="sxs-lookup"><span data-stu-id="14cf9-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="14cf9-117">父元素</span><span class="sxs-lookup"><span data-stu-id="14cf9-117">Parent elements</span></span>

|<span data-ttu-id="14cf9-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="14cf9-118">**Element**</span></span>|<span data-ttu-id="14cf9-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="14cf9-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14cf9-120">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="14cf9-120">ConflictResults</span></span>](conflictresults.md) <br/> |<span data-ttu-id="14cf9-121">包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突数。</span><span class="sxs-lookup"><span data-stu-id="14cf9-121">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="14cf9-122">文本值</span><span class="sxs-lookup"><span data-stu-id="14cf9-122">Text value</span></span>

<span data-ttu-id="14cf9-123">Text 值是一个整数，表示[UpdateItem 操作](updateitem-operation.md)响应中的冲突数。</span><span class="sxs-lookup"><span data-stu-id="14cf9-123">The text value is an integer that represents the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="14cf9-124">备注</span><span class="sxs-lookup"><span data-stu-id="14cf9-124">Remarks</span></span>

<span data-ttu-id="14cf9-125">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="14cf9-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14cf9-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="14cf9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14cf9-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="14cf9-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="14cf9-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="14cf9-128">Schema Name</span></span>  <br/> |<span data-ttu-id="14cf9-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="14cf9-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="14cf9-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="14cf9-130">Validation File</span></span>  <br/> |<span data-ttu-id="14cf9-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="14cf9-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="14cf9-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="14cf9-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="14cf9-133">False</span><span class="sxs-lookup"><span data-stu-id="14cf9-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14cf9-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="14cf9-134">See also</span></span>



[<span data-ttu-id="14cf9-135">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="14cf9-135">UpdateItem operation</span></span>](updateitem-operation.md)
  
 <span data-ttu-id="14cf9-136">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="14cf9-136">**ConflictResultsType**</span></span>

