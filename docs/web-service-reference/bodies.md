---
title: 团体
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a71a75f0-0b77-4cb9-8f9d-319de72fc1fd
description: 主体元素指定 BodyContentAttributedValue 元素的数组。
ms.openlocfilehash: d7087cf213d3c659a55458e021f4b8f0400efb1d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461511"
---
# <a name="bodies"></a><span data-ttu-id="39e9f-103">团体</span><span class="sxs-lookup"><span data-stu-id="39e9f-103">Bodies</span></span>

<span data-ttu-id="39e9f-104">**主体**元素指定**BodyContentAttributedValue**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="39e9f-104">The **Bodies** element specifies an array of **BodyContentAttributedValue** elements.</span></span> 
  
```XML
<Bodies>
    <BodyContentAttributedValue></BodyContentAttributedValue>
<Bodies>
```

 <span data-ttu-id="39e9f-105">**ArrayOfBodyContentAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="39e9f-105">**ArrayOfBodyContentAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39e9f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="39e9f-106">Attributes and elements</span></span>

<span data-ttu-id="39e9f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="39e9f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39e9f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="39e9f-108">Attributes</span></span>

<span data-ttu-id="39e9f-109">无。</span><span class="sxs-lookup"><span data-stu-id="39e9f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39e9f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="39e9f-110">Child elements</span></span>

|<span data-ttu-id="39e9f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="39e9f-111">**Element**</span></span>|<span data-ttu-id="39e9f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="39e9f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39e9f-113">BodyContentAttributedValue</span><span class="sxs-lookup"><span data-stu-id="39e9f-113">BodyContentAttributedValue</span></span>](bodycontentattributedvalue.md) <br/> |<span data-ttu-id="39e9f-114">指定项目的正文内容。</span><span class="sxs-lookup"><span data-stu-id="39e9f-114">Specifies the body content of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39e9f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="39e9f-115">Parent elements</span></span>

|<span data-ttu-id="39e9f-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="39e9f-116">**Element**</span></span>|<span data-ttu-id="39e9f-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="39e9f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39e9f-118">角色</span><span class="sxs-lookup"><span data-stu-id="39e9f-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="39e9f-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="39e9f-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39e9f-120">备注</span><span class="sxs-lookup"><span data-stu-id="39e9f-120">Remarks</span></span>

<span data-ttu-id="39e9f-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="39e9f-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="39e9f-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="39e9f-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39e9f-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="39e9f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39e9f-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="39e9f-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="39e9f-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="39e9f-125">Schema Name</span></span>  <br/> |<span data-ttu-id="39e9f-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="39e9f-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="39e9f-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="39e9f-127">Validation File</span></span>  <br/> |<span data-ttu-id="39e9f-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="39e9f-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="39e9f-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="39e9f-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="39e9f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="39e9f-130">See also</span></span>



- [<span data-ttu-id="39e9f-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="39e9f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

