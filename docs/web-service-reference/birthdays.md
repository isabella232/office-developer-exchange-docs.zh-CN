---
title: 生日
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5a84c19e-57cd-448e-af4f-c8005fd5f2a2
description: 生日元素指定生日，存储为字符串，并为该相关联的角色其源归属的标识符的数组。
ms.openlocfilehash: 2511a2acf0eb2eb24f06e98a1c660d289687bd02
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753332"
---
# <a name="birthdays"></a><span data-ttu-id="de52a-103">生日</span><span class="sxs-lookup"><span data-stu-id="de52a-103">Birthdays</span></span>

<span data-ttu-id="de52a-104">**生日**元素指定生日，存储为字符串，并为该相关联的角色其源归属的标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="de52a-104">The **Birthdays** element specifies an array of birthdays, stored as strings, and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Birthdays>
   <StringAttributedValue/>
</Birthdays>
```

 <span data-ttu-id="de52a-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="de52a-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de52a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="de52a-106">Attributes and elements</span></span>

<span data-ttu-id="de52a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="de52a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de52a-108">属性</span><span class="sxs-lookup"><span data-stu-id="de52a-108">Attributes</span></span>

<span data-ttu-id="de52a-109">无。</span><span class="sxs-lookup"><span data-stu-id="de52a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de52a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="de52a-110">Child elements</span></span>

|<span data-ttu-id="de52a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="de52a-111">**Element**</span></span>|<span data-ttu-id="de52a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="de52a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de52a-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="de52a-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="de52a-114">数组中的关联的个人元素的属性中指定的实例。</span><span class="sxs-lookup"><span data-stu-id="de52a-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de52a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="de52a-115">Parent elements</span></span>

|<span data-ttu-id="de52a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="de52a-116">**Element**</span></span>|<span data-ttu-id="de52a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="de52a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de52a-118">角色</span><span class="sxs-lookup"><span data-stu-id="de52a-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="de52a-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="de52a-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de52a-120">备注</span><span class="sxs-lookup"><span data-stu-id="de52a-120">Remarks</span></span>

<span data-ttu-id="de52a-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="de52a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="de52a-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="de52a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de52a-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="de52a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de52a-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="de52a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de52a-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="de52a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="de52a-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="de52a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="de52a-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="de52a-127">Validation File</span></span>  <br/> |<span data-ttu-id="de52a-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="de52a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="de52a-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="de52a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="de52a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="de52a-130">See also</span></span>



- [<span data-ttu-id="de52a-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="de52a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

