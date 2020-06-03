---
title: EditAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e63c4f7e-77c0-4826-b4e2-43b795d03914
description: EditAllowed 元素指定是否可以编辑信息权限管理。
ms.openlocfilehash: 979fbaa9fcfbd1015468a8ae00628959bad0bf56
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463480"
---
# <a name="editallowed"></a><span data-ttu-id="a2ca3-103">EditAllowed</span><span class="sxs-lookup"><span data-stu-id="a2ca3-103">EditAllowed</span></span>

<span data-ttu-id="a2ca3-104">**EditAllowed**元素指定是否可以编辑信息权限管理。</span><span class="sxs-lookup"><span data-stu-id="a2ca3-104">The **EditAllowed** element specifies whether Information Rights Management can be edited.</span></span> 
  
```XML
<EditAllowed> true | false </EditAllowed>
```

 <span data-ttu-id="a2ca3-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a2ca3-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a2ca3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a2ca3-106">Attributes and elements</span></span>

<span data-ttu-id="a2ca3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a2ca3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2ca3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a2ca3-108">Attributes</span></span>

<span data-ttu-id="a2ca3-109">无。</span><span class="sxs-lookup"><span data-stu-id="a2ca3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a2ca3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a2ca3-110">Child elements</span></span>

<span data-ttu-id="a2ca3-111">无。</span><span class="sxs-lookup"><span data-stu-id="a2ca3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a2ca3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a2ca3-112">Parent elements</span></span>

|<span data-ttu-id="a2ca3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a2ca3-113">**Element**</span></span>|<span data-ttu-id="a2ca3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a2ca3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2ca3-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="a2ca3-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="a2ca3-116">指定有关权限管理许可证的信息。</span><span class="sxs-lookup"><span data-stu-id="a2ca3-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a2ca3-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a2ca3-117">Text value</span></span>

<span data-ttu-id="a2ca3-118">如果**EditAllowed**元素的文本值为**true，则**表示可以编辑信息权限管理（IRM）。</span><span class="sxs-lookup"><span data-stu-id="a2ca3-118">A text value of **true** for the **EditAllowed** element indicates that Information Rights Management (IRM) can be edited.</span></span> <span data-ttu-id="a2ca3-119">**如果值为 false，则**表示无法编辑 IRM。</span><span class="sxs-lookup"><span data-stu-id="a2ca3-119">A value of **false** indicates that IRM cannot be edited.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a2ca3-120">备注</span><span class="sxs-lookup"><span data-stu-id="a2ca3-120">Remarks</span></span>

<span data-ttu-id="a2ca3-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a2ca3-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a2ca3-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a2ca3-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2ca3-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="a2ca3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2ca3-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="a2ca3-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a2ca3-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="a2ca3-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a2ca3-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="a2ca3-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="a2ca3-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="a2ca3-127">Validation File</span></span>  <br/> |<span data-ttu-id="a2ca3-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="a2ca3-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a2ca3-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="a2ca3-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a2ca3-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a2ca3-130">See also</span></span>



- [<span data-ttu-id="a2ca3-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a2ca3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

