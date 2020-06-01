---
title: DisplayNameLastFirst
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d392e138-a514-4bce-81b1-1f484e353d1c
description: DisplayNameLastFirst 元素以格式、姓氏、名字指定关联角色的显示名称。
ms.openlocfilehash: d569a87ce77a4f1840ed4f865e671399726ede78
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463158"
---
# <a name="displaynamelastfirst"></a><span data-ttu-id="89c49-103">DisplayNameLastFirst</span><span class="sxs-lookup"><span data-stu-id="89c49-103">DisplayNameLastFirst</span></span>

<span data-ttu-id="89c49-104">**DisplayNameLastFirst**元素指定格式为 "Last name"，"First name" 的关联角色的显示名称。</span><span class="sxs-lookup"><span data-stu-id="89c49-104">The **DisplayNameLastFirst** element specifies the display name of the associated persona in the format, "Last Name", "First Name".</span></span> 
  
```XML
<DisplayNameLastFirst></DisplayNameLastFirst>
```

 <span data-ttu-id="89c49-105">**string**</span><span class="sxs-lookup"><span data-stu-id="89c49-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89c49-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="89c49-106">Attributes and elements</span></span>

<span data-ttu-id="89c49-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="89c49-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89c49-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="89c49-108">Attributes</span></span>

<span data-ttu-id="89c49-109">无。</span><span class="sxs-lookup"><span data-stu-id="89c49-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89c49-110">子元素</span><span class="sxs-lookup"><span data-stu-id="89c49-110">Child elements</span></span>

<span data-ttu-id="89c49-111">无。</span><span class="sxs-lookup"><span data-stu-id="89c49-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89c49-112">父元素</span><span class="sxs-lookup"><span data-stu-id="89c49-112">Parent elements</span></span>

|<span data-ttu-id="89c49-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="89c49-113">**Element**</span></span>|<span data-ttu-id="89c49-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="89c49-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89c49-115">角色</span><span class="sxs-lookup"><span data-stu-id="89c49-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="89c49-116">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="89c49-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89c49-117">文本值</span><span class="sxs-lookup"><span data-stu-id="89c49-117">Text value</span></span>

<span data-ttu-id="89c49-118">**DisplayNameLastFirst**元素的文本值是一个 string 值，它指定显示名称，姓先是。</span><span class="sxs-lookup"><span data-stu-id="89c49-118">The text value of the **DisplayNameLastFirst** element is a string value that specifies the display name, with the surname first.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="89c49-119">备注</span><span class="sxs-lookup"><span data-stu-id="89c49-119">Remarks</span></span>

<span data-ttu-id="89c49-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="89c49-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="89c49-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="89c49-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89c49-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="89c49-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89c49-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="89c49-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="89c49-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="89c49-124">Schema Name</span></span>  <br/> |<span data-ttu-id="89c49-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="89c49-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="89c49-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="89c49-126">Validation File</span></span>  <br/> |<span data-ttu-id="89c49-127">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="89c49-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="89c49-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="89c49-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="89c49-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89c49-129">See also</span></span>

- [<span data-ttu-id="89c49-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="89c49-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

