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
description: UploadItems 元素表示将项目上传到邮箱的请求。
ms.openlocfilehash: 8fdb7253926e030085374b650e792349e598ee4a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468822"
---
# <a name="uploaditems"></a><span data-ttu-id="8333e-103">UploadItems</span><span class="sxs-lookup"><span data-stu-id="8333e-103">UploadItems</span></span>

<span data-ttu-id="8333e-104">**UploadItems**元素表示将项目上传到邮箱的请求。</span><span class="sxs-lookup"><span data-stu-id="8333e-104">The **UploadItems** element represents a request to upload items into a mailbox.</span></span> 
  
[<span data-ttu-id="8333e-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="8333e-105">UploadItems</span></span>](uploaditems.md)
  
```XML
<UploadItems>
   <Items/>
</UploadItems>
```

 <span data-ttu-id="8333e-106">**UploadItemsType**</span><span class="sxs-lookup"><span data-stu-id="8333e-106">**UploadItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8333e-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8333e-107">Attributes and elements</span></span>

<span data-ttu-id="8333e-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8333e-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8333e-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="8333e-109">Attributes</span></span>

<span data-ttu-id="8333e-110">无。</span><span class="sxs-lookup"><span data-stu-id="8333e-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8333e-111">子元素</span><span class="sxs-lookup"><span data-stu-id="8333e-111">Child elements</span></span>

|<span data-ttu-id="8333e-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="8333e-112">**Element**</span></span>|<span data-ttu-id="8333e-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="8333e-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8333e-114">项目（NonEmptyArrayOfUploadItemsType）</span><span class="sxs-lookup"><span data-stu-id="8333e-114">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="8333e-115">包含要上载到邮箱中的项的数组。</span><span class="sxs-lookup"><span data-stu-id="8333e-115">Contains an array of items to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8333e-116">父元素</span><span class="sxs-lookup"><span data-stu-id="8333e-116">Parent elements</span></span>

<span data-ttu-id="8333e-117">无。</span><span class="sxs-lookup"><span data-stu-id="8333e-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="8333e-118">文本值</span><span class="sxs-lookup"><span data-stu-id="8333e-118">Text value</span></span>

<span data-ttu-id="8333e-119">无。</span><span class="sxs-lookup"><span data-stu-id="8333e-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8333e-120">说明</span><span class="sxs-lookup"><span data-stu-id="8333e-120">Remarks</span></span>

<span data-ttu-id="8333e-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8333e-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8333e-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="8333e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8333e-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="8333e-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8333e-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="8333e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="8333e-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="8333e-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="8333e-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="8333e-126">Validation File</span></span>  <br/> |<span data-ttu-id="8333e-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8333e-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8333e-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="8333e-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="8333e-129">False</span><span class="sxs-lookup"><span data-stu-id="8333e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8333e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8333e-130">See also</span></span>



[<span data-ttu-id="8333e-131">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="8333e-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="8333e-132">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="8333e-132">UploadItems operation</span></span>](uploaditems-operation.md)

