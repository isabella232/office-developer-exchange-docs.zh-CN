---
title: ExportItemsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItemsResponse
api_type:
- schema
ms.assetid: ef44354b-fbdb-4f7c-b6bd-b27f56a1d018
description: ExportItemsResponse 元素均表示单个 ExportItems 请求的响应。
ms.openlocfilehash: 08033532d9cc381be8c544d790e9fe43840efb7b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754207"
---
# <a name="exportitemsresponse"></a><span data-ttu-id="a206e-103">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="a206e-103">ExportItemsResponse</span></span>

<span data-ttu-id="a206e-104">**ExportItemsResponse**元素均表示单个**ExportItems**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="a206e-104">The **ExportItemsResponse** element represents response to a single **ExportItems** request.</span></span> 
  
[<span data-ttu-id="a206e-105">ExportItemsResponse</span><span class="sxs-lookup"><span data-stu-id="a206e-105">ExportItemsResponse</span></span>](exportitemsresponse.md)
  
```XML
<ExportItemsResponse>
   <ResponseMessages/>
</ExportItemsResponse>
```

 <span data-ttu-id="a206e-106">**ExportItemsResponseType**</span><span class="sxs-lookup"><span data-stu-id="a206e-106">**ExportItemsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a206e-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a206e-107">Attributes and elements</span></span>

<span data-ttu-id="a206e-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a206e-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a206e-109">属性</span><span class="sxs-lookup"><span data-stu-id="a206e-109">Attributes</span></span>

<span data-ttu-id="a206e-110">无。</span><span class="sxs-lookup"><span data-stu-id="a206e-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a206e-111">子元素</span><span class="sxs-lookup"><span data-stu-id="a206e-111">Child elements</span></span>

|<span data-ttu-id="a206e-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="a206e-112">**Element**</span></span>|<span data-ttu-id="a206e-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="a206e-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a206e-114">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a206e-114">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="a206e-115">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="a206e-115">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a206e-116">父元素</span><span class="sxs-lookup"><span data-stu-id="a206e-116">Parent elements</span></span>

<span data-ttu-id="a206e-117">无。</span><span class="sxs-lookup"><span data-stu-id="a206e-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a206e-118">文本值</span><span class="sxs-lookup"><span data-stu-id="a206e-118">Text value</span></span>

<span data-ttu-id="a206e-119">无。</span><span class="sxs-lookup"><span data-stu-id="a206e-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a206e-120">备注</span><span class="sxs-lookup"><span data-stu-id="a206e-120">Remarks</span></span>

<span data-ttu-id="a206e-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a206e-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a206e-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="a206e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a206e-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="a206e-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a206e-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="a206e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="a206e-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="a206e-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="a206e-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="a206e-126">Validation File</span></span>  <br/> |<span data-ttu-id="a206e-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a206e-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a206e-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="a206e-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="a206e-129">False</span><span class="sxs-lookup"><span data-stu-id="a206e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a206e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a206e-130">See also</span></span>



[<span data-ttu-id="a206e-131">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="a206e-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="a206e-132">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="a206e-132">UploadItems operation</span></span>](uploaditems-operation.md)

