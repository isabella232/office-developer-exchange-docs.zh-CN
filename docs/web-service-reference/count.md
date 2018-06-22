---
title: 计数
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
description: Count 元素包含 UpdateItem 操作响应中的冲突的数量。
ms.openlocfilehash: 15cea49eb250336cdc6b7d551d53951aff1372c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753614"
---
# <a name="count"></a><span data-ttu-id="88003-103">计数</span><span class="sxs-lookup"><span data-stu-id="88003-103">Count</span></span>

<span data-ttu-id="88003-104">[Count](count.md)元素包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突的数量。</span><span class="sxs-lookup"><span data-stu-id="88003-104">The [Count](count.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
[<span data-ttu-id="88003-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="88003-105">UpdateItemResponse</span></span>](updateitemresponse.md)
  
[<span data-ttu-id="88003-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="88003-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="88003-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="88003-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
[<span data-ttu-id="88003-108">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="88003-108">ConflictResults</span></span>](conflictresults.md)
  
[<span data-ttu-id="88003-109">Count</span><span class="sxs-lookup"><span data-stu-id="88003-109">Count</span></span>](count.md)
  
```xml
<Count/>
```

 <span data-ttu-id="88003-110">**int**</span><span class="sxs-lookup"><span data-stu-id="88003-110">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="88003-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="88003-111">Attributes and elements</span></span>

<span data-ttu-id="88003-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="88003-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88003-113">属性</span><span class="sxs-lookup"><span data-stu-id="88003-113">Attributes</span></span>

<span data-ttu-id="88003-114">无。</span><span class="sxs-lookup"><span data-stu-id="88003-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88003-115">子元素</span><span class="sxs-lookup"><span data-stu-id="88003-115">Child elements</span></span>

<span data-ttu-id="88003-116">无。</span><span class="sxs-lookup"><span data-stu-id="88003-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="88003-117">父元素</span><span class="sxs-lookup"><span data-stu-id="88003-117">Parent elements</span></span>

|<span data-ttu-id="88003-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="88003-118">**Element**</span></span>|<span data-ttu-id="88003-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="88003-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88003-120">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="88003-120">ConflictResults</span></span>](conflictresults.md) <br/> |<span data-ttu-id="88003-121">包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突的数量。</span><span class="sxs-lookup"><span data-stu-id="88003-121">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="88003-122">文本值</span><span class="sxs-lookup"><span data-stu-id="88003-122">Text value</span></span>

<span data-ttu-id="88003-123">文本值为整数类型的值，该值代表[UpdateItem 操作](updateitem-operation.md)响应中的冲突数量。</span><span class="sxs-lookup"><span data-stu-id="88003-123">The text value is an integer that represents the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="88003-124">备注</span><span class="sxs-lookup"><span data-stu-id="88003-124">Remarks</span></span>

<span data-ttu-id="88003-125">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="88003-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88003-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="88003-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88003-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="88003-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="88003-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="88003-128">Schema Name</span></span>  <br/> |<span data-ttu-id="88003-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="88003-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="88003-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="88003-130">Validation File</span></span>  <br/> |<span data-ttu-id="88003-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="88003-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="88003-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="88003-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="88003-133">False</span><span class="sxs-lookup"><span data-stu-id="88003-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88003-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="88003-134">See also</span></span>



[<span data-ttu-id="88003-135">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="88003-135">UpdateItem operation</span></span>](updateitem-operation.md)
  
 <span data-ttu-id="88003-136">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="88003-136">**ConflictResultsType**</span></span>

