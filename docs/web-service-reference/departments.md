---
title: 部
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0a6b0a4-f0dd-4945-af69-628da93f5452
description: 部门元素为关联角色指定部门名称和其源归属的标识符的数组。
ms.openlocfilehash: 17590793e00a914cb53b479994bcc89e37bb0e31
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467933"
---
# <a name="departments"></a><span data-ttu-id="02872-103">部</span><span class="sxs-lookup"><span data-stu-id="02872-103">Departments</span></span>

<span data-ttu-id="02872-104">**部门**元素为关联角色指定部门名称和其源归属的标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="02872-104">The **Departments** element specifies an array of department names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Departments>
    <StringAttributedValue></StringAttributedValue>
</Departments>
```

 <span data-ttu-id="02872-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="02872-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02872-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="02872-106">Attributes and elements</span></span>

<span data-ttu-id="02872-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="02872-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02872-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="02872-108">Attributes</span></span>

<span data-ttu-id="02872-109">无。</span><span class="sxs-lookup"><span data-stu-id="02872-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02872-110">子元素</span><span class="sxs-lookup"><span data-stu-id="02872-110">Child elements</span></span>

|<span data-ttu-id="02872-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="02872-111">**Element**</span></span>|<span data-ttu-id="02872-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="02872-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02872-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="02872-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="02872-114">指定与 persona 元素相关联的属性数组中的实例。</span><span class="sxs-lookup"><span data-stu-id="02872-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="02872-115">父元素</span><span class="sxs-lookup"><span data-stu-id="02872-115">Parent elements</span></span>

|<span data-ttu-id="02872-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="02872-116">**Element**</span></span>|<span data-ttu-id="02872-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="02872-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02872-118">角色</span><span class="sxs-lookup"><span data-stu-id="02872-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="02872-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="02872-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02872-120">备注</span><span class="sxs-lookup"><span data-stu-id="02872-120">Remarks</span></span>

<span data-ttu-id="02872-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="02872-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="02872-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="02872-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02872-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="02872-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02872-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="02872-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="02872-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="02872-125">Schema Name</span></span>  <br/> |<span data-ttu-id="02872-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="02872-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="02872-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="02872-127">Validation File</span></span>  <br/> |<span data-ttu-id="02872-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="02872-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="02872-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="02872-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="02872-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="02872-130">See also</span></span>

- [<span data-ttu-id="02872-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="02872-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

