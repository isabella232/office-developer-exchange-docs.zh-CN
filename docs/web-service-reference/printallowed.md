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
ms.openlocfilehash: 85c18f3a6bd8f1705d0e21b99bae15484348f777
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826880"
---
# <a name="printallowed"></a><span data-ttu-id="e04f1-103">PrintAllowed</span><span class="sxs-lookup"><span data-stu-id="e04f1-103">PrintAllowed</span></span>

<span data-ttu-id="e04f1-104">**PrintAllowed**元素指定是否启用打印。</span><span class="sxs-lookup"><span data-stu-id="e04f1-104">The **PrintAllowed** element specifies whether printing is enabled.</span></span> 
  
```XML
<PrintAllowed> true | false </PrintAllowed>
```

 <span data-ttu-id="e04f1-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e04f1-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e04f1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e04f1-106">Attributes and elements</span></span>

<span data-ttu-id="e04f1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e04f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e04f1-108">属性</span><span class="sxs-lookup"><span data-stu-id="e04f1-108">Attributes</span></span>

<span data-ttu-id="e04f1-109">无。</span><span class="sxs-lookup"><span data-stu-id="e04f1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e04f1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e04f1-110">Child elements</span></span>

<span data-ttu-id="e04f1-111">无。</span><span class="sxs-lookup"><span data-stu-id="e04f1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e04f1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e04f1-112">Parent elements</span></span>

[<span data-ttu-id="e04f1-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="e04f1-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="e04f1-114">文本值</span><span class="sxs-lookup"><span data-stu-id="e04f1-114">Text value</span></span>

<span data-ttu-id="e04f1-115">文本值为**true**的**PrintAllowed**元素表示为权限管理项允许打印内容。</span><span class="sxs-lookup"><span data-stu-id="e04f1-115">A text value of **true** for the **PrintAllowed** element indicates that printing the contents is allowed for a rights managed item.</span></span> <span data-ttu-id="e04f1-116">如果值为**false**指示，不允许进行打印。</span><span class="sxs-lookup"><span data-stu-id="e04f1-116">A value of **false** indicates that printing is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e04f1-117">备注</span><span class="sxs-lookup"><span data-stu-id="e04f1-117">Remarks</span></span>

<span data-ttu-id="e04f1-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e04f1-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e04f1-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e04f1-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e04f1-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="e04f1-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e04f1-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="e04f1-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e04f1-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="e04f1-122">Schema name</span></span>  <br/> |<span data-ttu-id="e04f1-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="e04f1-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="e04f1-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="e04f1-124">Validation file</span></span>  <br/> |<span data-ttu-id="e04f1-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e04f1-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e04f1-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="e04f1-126">Can be empty</span></span>  <br/> ||
   

