---
title: 以外
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5a84c19e-57cd-448e-af4f-c8005fd5f2a2
description: 生日元素指定一个生日数组，存储为字符串，并为关联的角色指定其源归属的标识符。
ms.openlocfilehash: aa85febd84c32ae87e0822ce47fd99f445b6fe9e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462757"
---
# <a name="birthdays"></a><span data-ttu-id="905c6-103">以外</span><span class="sxs-lookup"><span data-stu-id="905c6-103">Birthdays</span></span>

<span data-ttu-id="905c6-104">**生日**元素指定一个生日数组，存储为字符串，并为关联的角色指定其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="905c6-104">The **Birthdays** element specifies an array of birthdays, stored as strings, and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Birthdays>
   <StringAttributedValue/>
</Birthdays>
```

 <span data-ttu-id="905c6-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="905c6-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="905c6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="905c6-106">Attributes and elements</span></span>

<span data-ttu-id="905c6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="905c6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="905c6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="905c6-108">Attributes</span></span>

<span data-ttu-id="905c6-109">无。</span><span class="sxs-lookup"><span data-stu-id="905c6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="905c6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="905c6-110">Child elements</span></span>

|<span data-ttu-id="905c6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="905c6-111">**Element**</span></span>|<span data-ttu-id="905c6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="905c6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="905c6-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="905c6-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="905c6-114">指定与 persona 元素相关联的属性数组中的实例。</span><span class="sxs-lookup"><span data-stu-id="905c6-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="905c6-115">父元素</span><span class="sxs-lookup"><span data-stu-id="905c6-115">Parent elements</span></span>

|<span data-ttu-id="905c6-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="905c6-116">**Element**</span></span>|<span data-ttu-id="905c6-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="905c6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="905c6-118">角色</span><span class="sxs-lookup"><span data-stu-id="905c6-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="905c6-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="905c6-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="905c6-120">备注</span><span class="sxs-lookup"><span data-stu-id="905c6-120">Remarks</span></span>

<span data-ttu-id="905c6-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="905c6-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="905c6-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="905c6-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="905c6-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="905c6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="905c6-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="905c6-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="905c6-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="905c6-125">Schema Name</span></span>  <br/> |<span data-ttu-id="905c6-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="905c6-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="905c6-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="905c6-127">Validation File</span></span>  <br/> |<span data-ttu-id="905c6-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="905c6-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="905c6-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="905c6-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="905c6-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="905c6-130">See also</span></span>



- [<span data-ttu-id="905c6-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="905c6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

