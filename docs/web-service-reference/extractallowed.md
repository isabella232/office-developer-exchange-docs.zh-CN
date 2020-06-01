---
title: ExtractAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc213f0e-a655-44e9-9ac9-bc1673bae1fe
description: ExtractAllowed 元素指定实体提取是否已启用。
ms.openlocfilehash: f9fcae72d6241e51f549fbf650f5b2aebe019e46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461980"
---
# <a name="extractallowed"></a><span data-ttu-id="a71c2-103">ExtractAllowed</span><span class="sxs-lookup"><span data-stu-id="a71c2-103">ExtractAllowed</span></span>

<span data-ttu-id="a71c2-104">**ExtractAllowed**元素指定实体提取是否已启用。</span><span class="sxs-lookup"><span data-stu-id="a71c2-104">The **ExtractAllowed** element specifies whether entity extraction is enabled.</span></span> 
  
```XML
<ExtractAllowed>true | false</ExtractAllowed
```

 <span data-ttu-id="a71c2-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a71c2-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a71c2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a71c2-106">Attributes and elements</span></span>

<span data-ttu-id="a71c2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a71c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a71c2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a71c2-108">Attributes</span></span>

<span data-ttu-id="a71c2-109">无。</span><span class="sxs-lookup"><span data-stu-id="a71c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a71c2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a71c2-110">Child elements</span></span>

<span data-ttu-id="a71c2-111">无。</span><span class="sxs-lookup"><span data-stu-id="a71c2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a71c2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a71c2-112">Parent elements</span></span>

|<span data-ttu-id="a71c2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a71c2-113">**Element**</span></span>|<span data-ttu-id="a71c2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a71c2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a71c2-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="a71c2-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="a71c2-116">指定有关权限管理许可证的信息。</span><span class="sxs-lookup"><span data-stu-id="a71c2-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a71c2-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a71c2-117">Text value</span></span>

<span data-ttu-id="a71c2-118">如果**ExtractAllowed**元素的文本值为**true** ，则表示实体提取已启用。</span><span class="sxs-lookup"><span data-stu-id="a71c2-118">A text value of **true** for the **ExtractAllowed** element indicates that entity extraction is enabled.</span></span> <span data-ttu-id="a71c2-119">**如果值为 false** ，则表示未启用实体提取。</span><span class="sxs-lookup"><span data-stu-id="a71c2-119">A value of **false** indicates that entity extraction is not enabled.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a71c2-120">备注</span><span class="sxs-lookup"><span data-stu-id="a71c2-120">Remarks</span></span>

<span data-ttu-id="a71c2-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a71c2-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a71c2-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a71c2-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a71c2-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="a71c2-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a71c2-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="a71c2-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a71c2-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="a71c2-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a71c2-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="a71c2-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="a71c2-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="a71c2-127">Validation File</span></span>  <br/> |<span data-ttu-id="a71c2-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="a71c2-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a71c2-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="a71c2-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a71c2-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a71c2-130">See also</span></span>



- [<span data-ttu-id="a71c2-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a71c2-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

