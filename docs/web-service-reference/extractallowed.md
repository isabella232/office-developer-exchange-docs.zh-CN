---
title: ExtractAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc213f0e-a655-44e9-9ac9-bc1673bae1fe
description: ExtractAllowed 元素指定是否启用实体提取。
ms.openlocfilehash: 48584e50be0ff66d156d9a3c3768729d63a9a3fd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754287"
---
# <a name="extractallowed"></a><span data-ttu-id="a3bdf-103">ExtractAllowed</span><span class="sxs-lookup"><span data-stu-id="a3bdf-103">ExtractAllowed</span></span>

<span data-ttu-id="a3bdf-104">**ExtractAllowed**元素指定是否启用实体提取。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-104">The **ExtractAllowed** element specifies whether entity extraction is enabled.</span></span> 
  
```XML
<ExtractAllowed>true | false</ExtractAllowed
```

 <span data-ttu-id="a3bdf-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a3bdf-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3bdf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a3bdf-106">Attributes and elements</span></span>

<span data-ttu-id="a3bdf-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3bdf-108">属性</span><span class="sxs-lookup"><span data-stu-id="a3bdf-108">Attributes</span></span>

<span data-ttu-id="a3bdf-109">无。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3bdf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a3bdf-110">Child elements</span></span>

<span data-ttu-id="a3bdf-111">无。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a3bdf-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a3bdf-112">Parent elements</span></span>

|<span data-ttu-id="a3bdf-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a3bdf-113">**Element**</span></span>|<span data-ttu-id="a3bdf-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a3bdf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3bdf-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="a3bdf-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="a3bdf-116">指定有关权限管理许可证的信息。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a3bdf-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a3bdf-117">Text value</span></span>

<span data-ttu-id="a3bdf-118">为**true**的**ExtractAllowed**元素的文本值指示已启用实体提取。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-118">A text value of **true** for the **ExtractAllowed** element indicates that entity extraction is enabled.</span></span> <span data-ttu-id="a3bdf-119">如果值为**false**指示实体提取未启用。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-119">A value of **false** indicates that entity extraction is not enabled.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a3bdf-120">备注</span><span class="sxs-lookup"><span data-stu-id="a3bdf-120">Remarks</span></span>

<span data-ttu-id="a3bdf-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a3bdf-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a3bdf-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3bdf-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="a3bdf-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3bdf-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="a3bdf-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a3bdf-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="a3bdf-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a3bdf-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="a3bdf-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="a3bdf-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="a3bdf-127">Validation File</span></span>  <br/> |<span data-ttu-id="a3bdf-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="a3bdf-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a3bdf-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="a3bdf-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a3bdf-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a3bdf-130">See also</span></span>



- [<span data-ttu-id="a3bdf-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a3bdf-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

