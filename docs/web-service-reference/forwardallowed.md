---
title: ForwardAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc32e0f4-61e9-4c9f-9a03-90a07eb51c53
description: ForwardAllowed 元素指定是否启用转发电子邮件。
ms.openlocfilehash: 4baa170a531cc9021102ff2255afc113f40e2348
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754412"
---
# <a name="forwardallowed"></a><span data-ttu-id="27d46-103">ForwardAllowed</span><span class="sxs-lookup"><span data-stu-id="27d46-103">ForwardAllowed</span></span>

<span data-ttu-id="27d46-104">**ForwardAllowed**元素指定是否启用转发电子邮件。</span><span class="sxs-lookup"><span data-stu-id="27d46-104">The **ForwardAllowed** element specifies whether forwarding emails is enabled.</span></span> 
  
```XML
<ForwardAllowed>true | false</ForwardAllowed>
```

 <span data-ttu-id="27d46-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="27d46-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27d46-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="27d46-106">Attributes and elements</span></span>

<span data-ttu-id="27d46-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="27d46-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27d46-108">属性</span><span class="sxs-lookup"><span data-stu-id="27d46-108">Attributes</span></span>

<span data-ttu-id="27d46-109">无。</span><span class="sxs-lookup"><span data-stu-id="27d46-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27d46-110">子元素</span><span class="sxs-lookup"><span data-stu-id="27d46-110">Child elements</span></span>

<span data-ttu-id="27d46-111">无。</span><span class="sxs-lookup"><span data-stu-id="27d46-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="27d46-112">父元素</span><span class="sxs-lookup"><span data-stu-id="27d46-112">Parent elements</span></span>

|<span data-ttu-id="27d46-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="27d46-113">**Element**</span></span>|<span data-ttu-id="27d46-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="27d46-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27d46-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="27d46-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="27d46-116">指定有关权限管理许可证的信息。</span><span class="sxs-lookup"><span data-stu-id="27d46-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="27d46-117">文本值</span><span class="sxs-lookup"><span data-stu-id="27d46-117">Text value</span></span>

<span data-ttu-id="27d46-118">文本值为**true**的**ForwardAllowed**元素指示指示允许转发电子邮件。</span><span class="sxs-lookup"><span data-stu-id="27d46-118">A text value of **true** for the **ForwardAllowed** element indicates that forwarding emails is allowed.</span></span> <span data-ttu-id="27d46-119">如果值为**false**指示，不允许进行转接。</span><span class="sxs-lookup"><span data-stu-id="27d46-119">A value of **false** indicates that forwarding is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="27d46-120">备注</span><span class="sxs-lookup"><span data-stu-id="27d46-120">Remarks</span></span>

<span data-ttu-id="27d46-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="27d46-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="27d46-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="27d46-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27d46-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="27d46-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27d46-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="27d46-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27d46-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="27d46-125">Schema Name</span></span>  <br/> |<span data-ttu-id="27d46-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="27d46-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="27d46-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="27d46-127">Validation File</span></span>  <br/> |<span data-ttu-id="27d46-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="27d46-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="27d46-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="27d46-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="27d46-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27d46-130">See also</span></span>



- [<span data-ttu-id="27d46-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="27d46-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

