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
ms.openlocfilehash: 3c722809bf68239c7d776108cb60d98afbed6e93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461931"
---
# <a name="forwardallowed"></a><span data-ttu-id="f2b1b-103">ForwardAllowed</span><span class="sxs-lookup"><span data-stu-id="f2b1b-103">ForwardAllowed</span></span>

<span data-ttu-id="f2b1b-104">**ForwardAllowed**元素指定是否启用转发电子邮件。</span><span class="sxs-lookup"><span data-stu-id="f2b1b-104">The **ForwardAllowed** element specifies whether forwarding emails is enabled.</span></span> 
  
```XML
<ForwardAllowed>true | false</ForwardAllowed>
```

 <span data-ttu-id="f2b1b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f2b1b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2b1b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f2b1b-106">Attributes and elements</span></span>

<span data-ttu-id="f2b1b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f2b1b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2b1b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f2b1b-108">Attributes</span></span>

<span data-ttu-id="f2b1b-109">无。</span><span class="sxs-lookup"><span data-stu-id="f2b1b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2b1b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f2b1b-110">Child elements</span></span>

<span data-ttu-id="f2b1b-111">无。</span><span class="sxs-lookup"><span data-stu-id="f2b1b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f2b1b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f2b1b-112">Parent elements</span></span>

|<span data-ttu-id="f2b1b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2b1b-113">**Element**</span></span>|<span data-ttu-id="f2b1b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2b1b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2b1b-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="f2b1b-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="f2b1b-116">指定有关权限管理许可证的信息。</span><span class="sxs-lookup"><span data-stu-id="f2b1b-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f2b1b-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f2b1b-117">Text value</span></span>

<span data-ttu-id="f2b1b-118">如果**ForwardAllowed**元素的文本值为**true** ，则表示允许转发电子邮件。</span><span class="sxs-lookup"><span data-stu-id="f2b1b-118">A text value of **true** for the **ForwardAllowed** element indicates that forwarding emails is allowed.</span></span> <span data-ttu-id="f2b1b-119">**如果值为 false** ，则表示不允许进行转发。</span><span class="sxs-lookup"><span data-stu-id="f2b1b-119">A value of **false** indicates that forwarding is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f2b1b-120">备注</span><span class="sxs-lookup"><span data-stu-id="f2b1b-120">Remarks</span></span>

<span data-ttu-id="f2b1b-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f2b1b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f2b1b-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f2b1b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2b1b-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f2b1b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2b1b-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f2b1b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f2b1b-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f2b1b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f2b1b-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="f2b1b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f2b1b-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f2b1b-127">Validation File</span></span>  <br/> |<span data-ttu-id="f2b1b-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="f2b1b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2b1b-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f2b1b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f2b1b-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2b1b-130">See also</span></span>



- [<span data-ttu-id="f2b1b-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f2b1b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

