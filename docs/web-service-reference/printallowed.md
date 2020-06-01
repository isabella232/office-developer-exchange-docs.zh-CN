---
title: PrintAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7232505a-bab0-4d78-87bc-6cc4b568937a
description: PrintAllowed 元素指定是否启用打印。
ms.openlocfilehash: ac38491d563916160b4d00165b743c51cb29fe00
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468745"
---
# <a name="printallowed"></a><span data-ttu-id="c0690-103">PrintAllowed</span><span class="sxs-lookup"><span data-stu-id="c0690-103">PrintAllowed</span></span>

<span data-ttu-id="c0690-104">**PrintAllowed**元素指定是否启用打印。</span><span class="sxs-lookup"><span data-stu-id="c0690-104">The **PrintAllowed** element specifies whether printing is enabled.</span></span> 
  
```XML
<PrintAllowed> true | false </PrintAllowed>
```

 <span data-ttu-id="c0690-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c0690-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0690-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c0690-106">Attributes and elements</span></span>

<span data-ttu-id="c0690-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c0690-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0690-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c0690-108">Attributes</span></span>

<span data-ttu-id="c0690-109">无。</span><span class="sxs-lookup"><span data-stu-id="c0690-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0690-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c0690-110">Child elements</span></span>

<span data-ttu-id="c0690-111">无。</span><span class="sxs-lookup"><span data-stu-id="c0690-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c0690-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c0690-112">Parent elements</span></span>

[<span data-ttu-id="c0690-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="c0690-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="c0690-114">文本值</span><span class="sxs-lookup"><span data-stu-id="c0690-114">Text value</span></span>

<span data-ttu-id="c0690-115">如果**PrintAllowed**元素的文本值为**true** ，则表示权限管理项的打印内容是允许的。</span><span class="sxs-lookup"><span data-stu-id="c0690-115">A text value of **true** for the **PrintAllowed** element indicates that printing the contents is allowed for a rights managed item.</span></span> <span data-ttu-id="c0690-116">**如果值为 false** ，则表示不允许打印。</span><span class="sxs-lookup"><span data-stu-id="c0690-116">A value of **false** indicates that printing is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c0690-117">备注</span><span class="sxs-lookup"><span data-stu-id="c0690-117">Remarks</span></span>

<span data-ttu-id="c0690-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c0690-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c0690-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c0690-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0690-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="c0690-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0690-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="c0690-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c0690-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="c0690-122">Schema name</span></span>  <br/> |<span data-ttu-id="c0690-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="c0690-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="c0690-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="c0690-124">Validation file</span></span>  <br/> |<span data-ttu-id="c0690-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c0690-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c0690-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="c0690-126">Can be empty</span></span>  <br/> ||
   

