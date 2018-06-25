---
title: UploadItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItems
api_type:
- schema
ms.assetid: fd2b9545-7213-4427-95ae-71a155b75971
description: UploadItems 元素表示项上载到邮箱的请求。
ms.openlocfilehash: d3cd69cdb744431daeede736c2e156c8ab92a79b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838436"
---
# <a name="uploaditems"></a><span data-ttu-id="b2ea0-103">UploadItems</span><span class="sxs-lookup"><span data-stu-id="b2ea0-103">UploadItems</span></span>

<span data-ttu-id="b2ea0-104">**UploadItems**元素表示项上载到邮箱的请求。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-104">The **UploadItems** element represents a request to upload items into a mailbox.</span></span> 
  
[<span data-ttu-id="b2ea0-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="b2ea0-105">UploadItems</span></span>](uploaditems.md)
  
```XML
<UploadItems>
   <Items/>
</UploadItems>
```

 <span data-ttu-id="b2ea0-106">**UploadItemsType**</span><span class="sxs-lookup"><span data-stu-id="b2ea0-106">**UploadItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b2ea0-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b2ea0-107">Attributes and elements</span></span>

<span data-ttu-id="b2ea0-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2ea0-109">属性</span><span class="sxs-lookup"><span data-stu-id="b2ea0-109">Attributes</span></span>

<span data-ttu-id="b2ea0-110">无。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b2ea0-111">子元素</span><span class="sxs-lookup"><span data-stu-id="b2ea0-111">Child elements</span></span>

|<span data-ttu-id="b2ea0-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="b2ea0-112">**Element**</span></span>|<span data-ttu-id="b2ea0-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2ea0-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2ea0-114">项目 (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="b2ea0-114">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="b2ea0-115">包含项目上载到邮箱的数组。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-115">Contains an array of items to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b2ea0-116">父元素</span><span class="sxs-lookup"><span data-stu-id="b2ea0-116">Parent elements</span></span>

<span data-ttu-id="b2ea0-117">无。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b2ea0-118">文本值</span><span class="sxs-lookup"><span data-stu-id="b2ea0-118">Text value</span></span>

<span data-ttu-id="b2ea0-119">无。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2ea0-120">备注</span><span class="sxs-lookup"><span data-stu-id="b2ea0-120">Remarks</span></span>

<span data-ttu-id="b2ea0-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b2ea0-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2ea0-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="b2ea0-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2ea0-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="b2ea0-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b2ea0-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="b2ea0-124">Schema Name</span></span>  <br/> |<span data-ttu-id="b2ea0-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="b2ea0-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="b2ea0-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="b2ea0-126">Validation File</span></span>  <br/> |<span data-ttu-id="b2ea0-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b2ea0-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b2ea0-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="b2ea0-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="b2ea0-129">False</span><span class="sxs-lookup"><span data-stu-id="b2ea0-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2ea0-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b2ea0-130">See also</span></span>



[<span data-ttu-id="b2ea0-131">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="b2ea0-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="b2ea0-132">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="b2ea0-132">UploadItems operation</span></span>](uploaditems-operation.md)

