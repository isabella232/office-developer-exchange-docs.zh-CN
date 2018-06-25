---
title: ConflictResults
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictResults
api_type:
- schema
ms.assetid: 08cdd547-4de7-4c7a-b60f-e618dc217d20
description: ConflictResults 元素包含 UpdateItem 操作响应中的冲突的数量。
ms.openlocfilehash: faa6dc6c5fbbe874438a89c810a12fa675e8a1c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753483"
---
# <a name="conflictresults"></a><span data-ttu-id="61ced-103">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="61ced-103">ConflictResults</span></span>

<span data-ttu-id="61ced-104">[ConflictResults](conflictresults.md)元素包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突的数量。</span><span class="sxs-lookup"><span data-stu-id="61ced-104">The [ConflictResults](conflictresults.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
[<span data-ttu-id="61ced-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="61ced-105">UpdateItemResponse</span></span>](updateitemresponse.md)
  
[<span data-ttu-id="61ced-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="61ced-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="61ced-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="61ced-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
[<span data-ttu-id="61ced-108">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="61ced-108">ConflictResults</span></span>](conflictresults.md)
  
```xml
<ConflictResults>
   <Count/>
</ConflictResults>
```

 <span data-ttu-id="61ced-109">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="61ced-109">**ConflictResultsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61ced-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="61ced-110">Attributes and elements</span></span>

<span data-ttu-id="61ced-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="61ced-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61ced-112">属性</span><span class="sxs-lookup"><span data-stu-id="61ced-112">Attributes</span></span>

<span data-ttu-id="61ced-113">无。</span><span class="sxs-lookup"><span data-stu-id="61ced-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61ced-114">子元素</span><span class="sxs-lookup"><span data-stu-id="61ced-114">Child elements</span></span>

|<span data-ttu-id="61ced-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="61ced-115">**Element**</span></span>|<span data-ttu-id="61ced-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="61ced-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61ced-117">Count</span><span class="sxs-lookup"><span data-stu-id="61ced-117">Count</span></span>](count.md) <br/> |<span data-ttu-id="61ced-118">包含[UpdateItem 操作](updateitem-operation.md)响应中的冲突的数量。</span><span class="sxs-lookup"><span data-stu-id="61ced-118">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61ced-119">父元素</span><span class="sxs-lookup"><span data-stu-id="61ced-119">Parent elements</span></span>

|<span data-ttu-id="61ced-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="61ced-120">**Element**</span></span>|<span data-ttu-id="61ced-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="61ced-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61ced-122">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="61ced-122">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md) <br/> |<span data-ttu-id="61ced-123">包含状态和的单个结果[UpdateItem 操作](updateitem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="61ced-123">Contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61ced-124">注解</span><span class="sxs-lookup"><span data-stu-id="61ced-124">Remarks</span></span>

<span data-ttu-id="61ced-125">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="61ced-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61ced-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="61ced-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61ced-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="61ced-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="61ced-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="61ced-128">Schema Name</span></span>  <br/> |<span data-ttu-id="61ced-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="61ced-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="61ced-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="61ced-130">Validation File</span></span>  <br/> |<span data-ttu-id="61ced-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="61ced-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="61ced-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="61ced-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="61ced-133">False</span><span class="sxs-lookup"><span data-stu-id="61ced-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61ced-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="61ced-134">See also</span></span>



[<span data-ttu-id="61ced-135">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="61ced-135">UpdateItem operation</span></span>](updateitem-operation.md)
  
 <span data-ttu-id="61ced-136">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="61ced-136">**ConflictResultsType**</span></span>

