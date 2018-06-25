---
title: DisplayNamePrefix
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 60363698-7603-4051-a66e-007c02db17cb
description: DisplayNamePrefix 元素指定关联的个人的显示名称的前缀。
ms.openlocfilehash: 120a6402be386bc0c11f5859265098324ce4687f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753948"
---
# <a name="displaynameprefix"></a><span data-ttu-id="fe857-103">DisplayNamePrefix</span><span class="sxs-lookup"><span data-stu-id="fe857-103">DisplayNamePrefix</span></span>

<span data-ttu-id="fe857-104">**DisplayNamePrefix**元素指定关联的个人的显示名称的前缀。</span><span class="sxs-lookup"><span data-stu-id="fe857-104">The **DisplayNamePrefix** element specifies the prefix of the display name of the associated persona.</span></span> 
  
```xml
<DisplayNamePrefix></DisplayNamePrefix>
```

 <span data-ttu-id="fe857-105">**string**</span><span class="sxs-lookup"><span data-stu-id="fe857-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe857-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fe857-106">Attributes and elements</span></span>

<span data-ttu-id="fe857-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fe857-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe857-108">属性</span><span class="sxs-lookup"><span data-stu-id="fe857-108">Attributes</span></span>

<span data-ttu-id="fe857-109">无。</span><span class="sxs-lookup"><span data-stu-id="fe857-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe857-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fe857-110">Child elements</span></span>

<span data-ttu-id="fe857-111">无。</span><span class="sxs-lookup"><span data-stu-id="fe857-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe857-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fe857-112">Parent elements</span></span>

|<span data-ttu-id="fe857-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fe857-113">**Element**</span></span>|<span data-ttu-id="fe857-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe857-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe857-115">角色</span><span class="sxs-lookup"><span data-stu-id="fe857-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="fe857-116">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="fe857-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fe857-117">文本值</span><span class="sxs-lookup"><span data-stu-id="fe857-117">Text value</span></span>

<span data-ttu-id="fe857-118">**DisplayNamePrefix**元素的文本值是一个 string 值，指定的显示名称的前缀。</span><span class="sxs-lookup"><span data-stu-id="fe857-118">The text value of the **DisplayNamePrefix** element is a string value that specifies the prefix for the display name.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe857-119">备注</span><span class="sxs-lookup"><span data-stu-id="fe857-119">Remarks</span></span>

<span data-ttu-id="fe857-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fe857-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fe857-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fe857-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe857-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="fe857-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe857-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="fe857-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fe857-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="fe857-124">Schema Name</span></span>  <br/> |<span data-ttu-id="fe857-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="fe857-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="fe857-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="fe857-126">Validation File</span></span>  <br/> |<span data-ttu-id="fe857-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="fe857-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fe857-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="fe857-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fe857-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe857-129">See also</span></span>

- [<span data-ttu-id="fe857-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fe857-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

