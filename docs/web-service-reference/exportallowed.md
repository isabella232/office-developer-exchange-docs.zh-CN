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
ms.openlocfilehash: 5c07941e0a79394bbdaa1a1f62b20adedfe7a9bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754204"
---
# <a name="exportallowed"></a><span data-ttu-id="3430f-103">ExportAllowed</span><span class="sxs-lookup"><span data-stu-id="3430f-103">ExportAllowed</span></span>

<span data-ttu-id="3430f-104">**ExportAllowed**元素指定是否启用导出。</span><span class="sxs-lookup"><span data-stu-id="3430f-104">The **ExportAllowed** element specifies whether exporting is enabled.</span></span> 
  
```XML
<ExportAllowed>true | false</ExportAllowed>
```

 <span data-ttu-id="3430f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3430f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3430f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3430f-106">Attributes and elements</span></span>

<span data-ttu-id="3430f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3430f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3430f-108">属性</span><span class="sxs-lookup"><span data-stu-id="3430f-108">Attributes</span></span>

<span data-ttu-id="3430f-109">无。</span><span class="sxs-lookup"><span data-stu-id="3430f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3430f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3430f-110">Child elements</span></span>

<span data-ttu-id="3430f-111">无。</span><span class="sxs-lookup"><span data-stu-id="3430f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3430f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3430f-112">Parent elements</span></span>

|<span data-ttu-id="3430f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3430f-113">**Element**</span></span>|<span data-ttu-id="3430f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3430f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3430f-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="3430f-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="3430f-116">指定有关权限管理许可证的信息。</span><span class="sxs-lookup"><span data-stu-id="3430f-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3430f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="3430f-117">Text value</span></span>

<span data-ttu-id="3430f-118">文本值为**true**的**ExportAllowed**元素表示允许为导出。</span><span class="sxs-lookup"><span data-stu-id="3430f-118">A text value of **true** for the **ExportAllowed** element indicates that exporting is allowed.</span></span> <span data-ttu-id="3430f-119">如果值为**false**指示不允许导出。</span><span class="sxs-lookup"><span data-stu-id="3430f-119">A value of **false** indicates that exporting is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3430f-120">备注</span><span class="sxs-lookup"><span data-stu-id="3430f-120">Remarks</span></span>

<span data-ttu-id="3430f-121">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="3430f-121">This element is optional.</span></span>
  
<span data-ttu-id="3430f-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3430f-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3430f-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3430f-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3430f-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="3430f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3430f-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="3430f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3430f-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="3430f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="3430f-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="3430f-127">Type schema</span></span>  <br/> |
|<span data-ttu-id="3430f-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="3430f-128">Validation File</span></span>  <br/> |<span data-ttu-id="3430f-129">types.xsd</span><span class="sxs-lookup"><span data-stu-id="3430f-129">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3430f-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="3430f-130">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3430f-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3430f-131">See also</span></span>



- [<span data-ttu-id="3430f-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3430f-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

