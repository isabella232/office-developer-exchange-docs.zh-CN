---
title: ProgrammaticAccessAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a1fc7dff-a303-4809-b7f4-9672f86c183c
description: ProgrammaticAccessAllowed 元素指定是否对权限托管数据启用编程访问。
ms.openlocfilehash: 8a5cf4e57a97807e5940a0402768d7123b9912d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465637"
---
# <a name="programmaticaccessallowed"></a><span data-ttu-id="fbbaa-103">ProgrammaticAccessAllowed</span><span class="sxs-lookup"><span data-stu-id="fbbaa-103">ProgrammaticAccessAllowed</span></span>

<span data-ttu-id="fbbaa-104">**ProgrammaticAccessAllowed**元素指定是否对权限托管数据启用编程访问。</span><span class="sxs-lookup"><span data-stu-id="fbbaa-104">The **ProgrammaticAccessAllowed** element specifies whether programmatic access is enabled for rights managed data.</span></span> 
  
```XML
<ProgrammaticAccessAllowed> true | false </ProgrammaticAccessAllowed>
```

 <span data-ttu-id="fbbaa-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fbbaa-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbbaa-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fbbaa-106">Attributes and elements</span></span>

<span data-ttu-id="fbbaa-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fbbaa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbbaa-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fbbaa-108">Attributes</span></span>

<span data-ttu-id="fbbaa-109">无。</span><span class="sxs-lookup"><span data-stu-id="fbbaa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fbbaa-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fbbaa-110">Child elements</span></span>

<span data-ttu-id="fbbaa-111">无。</span><span class="sxs-lookup"><span data-stu-id="fbbaa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fbbaa-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fbbaa-112">Parent elements</span></span>

[<span data-ttu-id="fbbaa-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="fbbaa-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="fbbaa-114">文本值</span><span class="sxs-lookup"><span data-stu-id="fbbaa-114">Text value</span></span>

<span data-ttu-id="fbbaa-115">如果**ProgrammaticAccessAllowed**元素的文本值为**true** ，则表示以编程方式访问数据。</span><span class="sxs-lookup"><span data-stu-id="fbbaa-115">A text value of **true** for the **ProgrammaticAccessAllowed** element indicates that the data is programmatically accessible.</span></span> <span data-ttu-id="fbbaa-116">值**为 false**表示无法以编程方式访问数据。</span><span class="sxs-lookup"><span data-stu-id="fbbaa-116">A value of **false** indicates that the data is not programmatically accessible.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fbbaa-117">备注</span><span class="sxs-lookup"><span data-stu-id="fbbaa-117">Remarks</span></span>

<span data-ttu-id="fbbaa-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fbbaa-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fbbaa-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fbbaa-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbbaa-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="fbbaa-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbbaa-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="fbbaa-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fbbaa-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="fbbaa-122">Schema name</span></span>  <br/> |<span data-ttu-id="fbbaa-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="fbbaa-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="fbbaa-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="fbbaa-124">Validation file</span></span>  <br/> |<span data-ttu-id="fbbaa-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fbbaa-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fbbaa-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="fbbaa-126">Can be empty</span></span>  <br/> |<span data-ttu-id="fbbaa-127">false</span><span class="sxs-lookup"><span data-stu-id="fbbaa-127">false</span></span>  <br/> |
   

