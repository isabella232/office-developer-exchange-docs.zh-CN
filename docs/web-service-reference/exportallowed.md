---
title: ExportAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dcff5ccc-31dc-4941-9f71-d6519133aebb
description: ExportAllowed 元素指定是否启用导出。
ms.openlocfilehash: f5a9aa3040c45d535ef338010bb37bcedb797ffc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460629"
---
# <a name="exportallowed"></a><span data-ttu-id="1e24e-103">ExportAllowed</span><span class="sxs-lookup"><span data-stu-id="1e24e-103">ExportAllowed</span></span>

<span data-ttu-id="1e24e-104">**ExportAllowed**元素指定是否启用导出。</span><span class="sxs-lookup"><span data-stu-id="1e24e-104">The **ExportAllowed** element specifies whether exporting is enabled.</span></span> 
  
```XML
<ExportAllowed>true | false</ExportAllowed>
```

 <span data-ttu-id="1e24e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1e24e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1e24e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1e24e-106">Attributes and elements</span></span>

<span data-ttu-id="1e24e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1e24e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e24e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1e24e-108">Attributes</span></span>

<span data-ttu-id="1e24e-109">无。</span><span class="sxs-lookup"><span data-stu-id="1e24e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e24e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1e24e-110">Child elements</span></span>

<span data-ttu-id="1e24e-111">无。</span><span class="sxs-lookup"><span data-stu-id="1e24e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1e24e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1e24e-112">Parent elements</span></span>

|<span data-ttu-id="1e24e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e24e-113">**Element**</span></span>|<span data-ttu-id="1e24e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e24e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e24e-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="1e24e-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="1e24e-116">指定有关权限管理许可证的信息。</span><span class="sxs-lookup"><span data-stu-id="1e24e-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1e24e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="1e24e-117">Text value</span></span>

<span data-ttu-id="1e24e-118">如果**ExportAllowed**元素的文本值为**true** ，则表示允许导出。</span><span class="sxs-lookup"><span data-stu-id="1e24e-118">A text value of **true** for the **ExportAllowed** element indicates that exporting is allowed.</span></span> <span data-ttu-id="1e24e-119">**如果值为 false** ，则表示不允许导出。</span><span class="sxs-lookup"><span data-stu-id="1e24e-119">A value of **false** indicates that exporting is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1e24e-120">说明</span><span class="sxs-lookup"><span data-stu-id="1e24e-120">Remarks</span></span>

<span data-ttu-id="1e24e-121">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="1e24e-121">This element is optional.</span></span>
  
<span data-ttu-id="1e24e-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1e24e-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1e24e-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1e24e-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e24e-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="1e24e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e24e-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="1e24e-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1e24e-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="1e24e-126">Schema Name</span></span>  <br/> |<span data-ttu-id="1e24e-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="1e24e-127">Type schema</span></span>  <br/> |
|<span data-ttu-id="1e24e-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="1e24e-128">Validation File</span></span>  <br/> |<span data-ttu-id="1e24e-129">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="1e24e-129">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1e24e-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="1e24e-130">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1e24e-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1e24e-131">See also</span></span>



- [<span data-ttu-id="1e24e-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1e24e-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

