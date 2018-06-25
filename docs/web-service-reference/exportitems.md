---
title: ExportItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExportItems
api_type:
- schema
ms.assetid: bbbc56e4-8cc1-43ae-b70a-9a8d6bb0f399
description: ExportItems 元素表示的项目导出邮箱中的请求。
ms.openlocfilehash: 055012166bb125dfcf86070f2e23496bf0209b51
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754203"
---
# <a name="exportitems"></a><span data-ttu-id="7c063-103">ExportItems</span><span class="sxs-lookup"><span data-stu-id="7c063-103">ExportItems</span></span>

<span data-ttu-id="7c063-104">**ExportItems**元素表示的项目导出邮箱中的请求。</span><span class="sxs-lookup"><span data-stu-id="7c063-104">The **ExportItems** element represents a request to export items from a mailbox.</span></span> 
  
[<span data-ttu-id="7c063-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="7c063-105">ExportItems</span></span>](exportitems.md)
  
```XML
<ExportItems>
   <ItemIds/>
</ExportItems>
```

 <span data-ttu-id="7c063-106">**ExportItemsType**</span><span class="sxs-lookup"><span data-stu-id="7c063-106">**ExportItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7c063-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7c063-107">Attributes and elements</span></span>

<span data-ttu-id="7c063-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7c063-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c063-109">属性</span><span class="sxs-lookup"><span data-stu-id="7c063-109">Attributes</span></span>

<span data-ttu-id="7c063-110">无。</span><span class="sxs-lookup"><span data-stu-id="7c063-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c063-111">子元素</span><span class="sxs-lookup"><span data-stu-id="7c063-111">Child elements</span></span>

|<span data-ttu-id="7c063-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="7c063-112">**Element**</span></span>|<span data-ttu-id="7c063-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="7c063-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c063-114">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="7c063-114">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="7c063-115">包含确定要导出邮箱中的项的项标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="7c063-115">Contains an array of item identifiers that identify the items to export from a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7c063-116">父元素</span><span class="sxs-lookup"><span data-stu-id="7c063-116">Parent elements</span></span>

<span data-ttu-id="7c063-117">无。</span><span class="sxs-lookup"><span data-stu-id="7c063-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7c063-118">文本值</span><span class="sxs-lookup"><span data-stu-id="7c063-118">Text value</span></span>

<span data-ttu-id="7c063-119">无。</span><span class="sxs-lookup"><span data-stu-id="7c063-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c063-120">备注</span><span class="sxs-lookup"><span data-stu-id="7c063-120">Remarks</span></span>

<span data-ttu-id="7c063-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7c063-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c063-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="7c063-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c063-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="7c063-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7c063-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="7c063-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7c063-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="7c063-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="7c063-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="7c063-126">Validation File</span></span>  <br/> |<span data-ttu-id="7c063-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7c063-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7c063-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="7c063-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="7c063-129">False</span><span class="sxs-lookup"><span data-stu-id="7c063-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c063-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7c063-130">See also</span></span>



[<span data-ttu-id="7c063-131">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="7c063-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="7c063-132">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="7c063-132">UploadItems operation</span></span>](uploaditems-operation.md)

