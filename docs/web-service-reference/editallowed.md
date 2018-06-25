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
ms.openlocfilehash: 48c7d751c018bf5702b05b41eeaa7ad350189e3a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754018"
---
# <a name="editallowed"></a><span data-ttu-id="670c3-103">EditAllowed</span><span class="sxs-lookup"><span data-stu-id="670c3-103">EditAllowed</span></span>

<span data-ttu-id="670c3-104">**EditAllowed**元素指定是否可以编辑信息权限管理。</span><span class="sxs-lookup"><span data-stu-id="670c3-104">The **EditAllowed** element specifies whether Information Rights Management can be edited.</span></span> 
  
```XML
<EditAllowed> true | false </EditAllowed>
```

 <span data-ttu-id="670c3-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="670c3-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="670c3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="670c3-106">Attributes and elements</span></span>

<span data-ttu-id="670c3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="670c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="670c3-108">属性</span><span class="sxs-lookup"><span data-stu-id="670c3-108">Attributes</span></span>

<span data-ttu-id="670c3-109">无。</span><span class="sxs-lookup"><span data-stu-id="670c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="670c3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="670c3-110">Child elements</span></span>

<span data-ttu-id="670c3-111">无。</span><span class="sxs-lookup"><span data-stu-id="670c3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="670c3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="670c3-112">Parent elements</span></span>

|<span data-ttu-id="670c3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="670c3-113">**Element**</span></span>|<span data-ttu-id="670c3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="670c3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="670c3-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="670c3-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="670c3-116">指定有关权限管理许可证的信息。</span><span class="sxs-lookup"><span data-stu-id="670c3-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="670c3-117">文本值</span><span class="sxs-lookup"><span data-stu-id="670c3-117">Text value</span></span>

<span data-ttu-id="670c3-118">文本值为**true**的**EditAllowed**元素表示可编辑的信息权限管理 (IRM)。</span><span class="sxs-lookup"><span data-stu-id="670c3-118">A text value of **true** for the **EditAllowed** element indicates that Information Rights Management (IRM) can be edited.</span></span> <span data-ttu-id="670c3-119">如果值为**false**指示不能编辑 IRM。</span><span class="sxs-lookup"><span data-stu-id="670c3-119">A value of **false** indicates that IRM cannot be edited.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="670c3-120">备注</span><span class="sxs-lookup"><span data-stu-id="670c3-120">Remarks</span></span>

<span data-ttu-id="670c3-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="670c3-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="670c3-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="670c3-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="670c3-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="670c3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="670c3-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="670c3-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="670c3-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="670c3-125">Schema Name</span></span>  <br/> |<span data-ttu-id="670c3-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="670c3-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="670c3-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="670c3-127">Validation File</span></span>  <br/> |<span data-ttu-id="670c3-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="670c3-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="670c3-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="670c3-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="670c3-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="670c3-130">See also</span></span>



- [<span data-ttu-id="670c3-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="670c3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

