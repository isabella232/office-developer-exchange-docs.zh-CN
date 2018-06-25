---
title: ProgrammaticAccessAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a1fc7dff-a303-4809-b7f4-9672f86c183c
description: ProgrammaticAccessAllowed 元素指定是否为权限管理的数据启用的编程访问权限。
ms.openlocfilehash: 50bcce745bd94bf9c2e5ced93825722307e0a096
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826889"
---
# <a name="programmaticaccessallowed"></a><span data-ttu-id="1f4f3-103">ProgrammaticAccessAllowed</span><span class="sxs-lookup"><span data-stu-id="1f4f3-103">ProgrammaticAccessAllowed</span></span>

<span data-ttu-id="1f4f3-104">**ProgrammaticAccessAllowed**元素指定是否为权限管理的数据启用的编程访问权限。</span><span class="sxs-lookup"><span data-stu-id="1f4f3-104">The **ProgrammaticAccessAllowed** element specifies whether programmatic access is enabled for rights managed data.</span></span> 
  
```XML
<ProgrammaticAccessAllowed> true | false </ProgrammaticAccessAllowed>
```

 <span data-ttu-id="1f4f3-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1f4f3-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f4f3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1f4f3-106">Attributes and elements</span></span>

<span data-ttu-id="1f4f3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1f4f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f4f3-108">属性</span><span class="sxs-lookup"><span data-stu-id="1f4f3-108">Attributes</span></span>

<span data-ttu-id="1f4f3-109">无。</span><span class="sxs-lookup"><span data-stu-id="1f4f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f4f3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1f4f3-110">Child elements</span></span>

<span data-ttu-id="1f4f3-111">无。</span><span class="sxs-lookup"><span data-stu-id="1f4f3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f4f3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1f4f3-112">Parent elements</span></span>

[<span data-ttu-id="1f4f3-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="1f4f3-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="1f4f3-114">文本值</span><span class="sxs-lookup"><span data-stu-id="1f4f3-114">Text value</span></span>

<span data-ttu-id="1f4f3-115">为**true**的**ProgrammaticAccessAllowed**元素的文本值指示以编程方式访问数据。</span><span class="sxs-lookup"><span data-stu-id="1f4f3-115">A text value of **true** for the **ProgrammaticAccessAllowed** element indicates that the data is programmatically accessible.</span></span> <span data-ttu-id="1f4f3-116">如果值为**false**指示的数据不是以编程方式访问。</span><span class="sxs-lookup"><span data-stu-id="1f4f3-116">A value of **false** indicates that the data is not programmatically accessible.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1f4f3-117">备注</span><span class="sxs-lookup"><span data-stu-id="1f4f3-117">Remarks</span></span>

<span data-ttu-id="1f4f3-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1f4f3-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1f4f3-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1f4f3-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f4f3-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="1f4f3-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f4f3-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="1f4f3-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1f4f3-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="1f4f3-122">Schema name</span></span>  <br/> |<span data-ttu-id="1f4f3-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="1f4f3-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="1f4f3-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="1f4f3-124">Validation file</span></span>  <br/> |<span data-ttu-id="1f4f3-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1f4f3-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1f4f3-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="1f4f3-126">Can be empty</span></span>  <br/> |<span data-ttu-id="1f4f3-127">false</span><span class="sxs-lookup"><span data-stu-id="1f4f3-127">false</span></span>  <br/> |
   

