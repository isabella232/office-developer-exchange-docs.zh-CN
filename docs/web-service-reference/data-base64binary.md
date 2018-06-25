---
title: 数据 (base64Binary)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: Data 元素包含单个导出的项或项上载到邮箱的数据。
ms.openlocfilehash: 9560273e31a64edb2254489961733dfe7360ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753728"
---
# <a name="data-base64binary"></a><span data-ttu-id="9500e-103">数据 (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="9500e-103">Data (base64Binary)</span></span>

<span data-ttu-id="9500e-104">**Data**元素包含单个导出的项或项上载到邮箱的数据。</span><span class="sxs-lookup"><span data-stu-id="9500e-104">The **Data** element contains the data of a single exported item or an item to upload into a mailbox.</span></span> 
  
```XML
<Data/>
```

<span data-ttu-id="9500e-105">**xs:base64Binary**</span><span class="sxs-lookup"><span data-stu-id="9500e-105">**xs:base64Binary**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9500e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9500e-106">Attributes and elements</span></span>

<span data-ttu-id="9500e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9500e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9500e-108">属性</span><span class="sxs-lookup"><span data-stu-id="9500e-108">Attributes</span></span>

<span data-ttu-id="9500e-109">无。</span><span class="sxs-lookup"><span data-stu-id="9500e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9500e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9500e-110">Child elements</span></span>

<span data-ttu-id="9500e-111">无。</span><span class="sxs-lookup"><span data-stu-id="9500e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9500e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9500e-112">Parent elements</span></span>

|<span data-ttu-id="9500e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9500e-113">**Element**</span></span>|<span data-ttu-id="9500e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9500e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9500e-115">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9500e-115">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md) <br/> |<span data-ttu-id="9500e-116">包含状态和请求导出的单个邮箱项目的结果。</span><span class="sxs-lookup"><span data-stu-id="9500e-116">Contains the status and results of a request to export a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="9500e-117">项目 (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="9500e-117">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="9500e-118">代表单个项目上载到邮箱。</span><span class="sxs-lookup"><span data-stu-id="9500e-118">Represents a single item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9500e-119">文本值</span><span class="sxs-lookup"><span data-stu-id="9500e-119">Text value</span></span>

<span data-ttu-id="9500e-120">**Data**元素包含的属性名称和导出的项目或将上载到邮箱的项的值。</span><span class="sxs-lookup"><span data-stu-id="9500e-120">The **Data** element contains the property names and values for an exported item or an item that will be uploaded into a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9500e-121">备注</span><span class="sxs-lookup"><span data-stu-id="9500e-121">Remarks</span></span>

<span data-ttu-id="9500e-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9500e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9500e-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="9500e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9500e-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="9500e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9500e-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="9500e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9500e-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="9500e-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="9500e-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="9500e-127">Validation File</span></span>  <br/> |<span data-ttu-id="9500e-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9500e-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9500e-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="9500e-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9500e-130">False</span><span class="sxs-lookup"><span data-stu-id="9500e-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9500e-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9500e-131">See also</span></span>

- [<span data-ttu-id="9500e-132">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="9500e-132">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="9500e-133">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="9500e-133">UploadItems operation</span></span>](uploaditems-operation.md)

