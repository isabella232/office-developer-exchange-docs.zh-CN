---
title: HomeFaxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 459ddb1c-8cff-4125-b6fa-dc93c183dee8
description: HomeFaxes 元素指定一个数组住宅传真号码和为相关联的角色其源归属的标识符。
ms.openlocfilehash: dd2cd8bba2c4cc7d08e88787d648e96ea996a251
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825840"
---
# <a name="homefaxes"></a><span data-ttu-id="ffb5b-103">HomeFaxes</span><span class="sxs-lookup"><span data-stu-id="ffb5b-103">HomeFaxes</span></span>

<span data-ttu-id="ffb5b-104">**HomeFaxes**元素指定一个数组住宅传真号码和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="ffb5b-104">The **HomeFaxes** element specifies an array of home fax numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomeFaxes>
    <PhoneNumberAttributedValue/>
</HomeFaxes>
```

 <span data-ttu-id="ffb5b-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffb5b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ffb5b-106">Attributes and elements</span></span>

<span data-ttu-id="ffb5b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ffb5b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffb5b-108">属性</span><span class="sxs-lookup"><span data-stu-id="ffb5b-108">Attributes</span></span>

<span data-ttu-id="ffb5b-109">无。</span><span class="sxs-lookup"><span data-stu-id="ffb5b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ffb5b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ffb5b-110">Child elements</span></span>

|<span data-ttu-id="ffb5b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-111">**Element**</span></span>|<span data-ttu-id="ffb5b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffb5b-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="ffb5b-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="ffb5b-114">包含单个属性化的电话号码的角色。</span><span class="sxs-lookup"><span data-stu-id="ffb5b-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ffb5b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ffb5b-115">Parent elements</span></span>

|<span data-ttu-id="ffb5b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-116">**Element**</span></span>|<span data-ttu-id="ffb5b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ffb5b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffb5b-118">角色</span><span class="sxs-lookup"><span data-stu-id="ffb5b-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="ffb5b-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="ffb5b-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffb5b-120">备注</span><span class="sxs-lookup"><span data-stu-id="ffb5b-120">Remarks</span></span>

<span data-ttu-id="ffb5b-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ffb5b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ffb5b-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ffb5b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ffb5b-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="ffb5b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffb5b-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="ffb5b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ffb5b-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="ffb5b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ffb5b-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="ffb5b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="ffb5b-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="ffb5b-127">Validation File</span></span>  <br/> |<span data-ttu-id="ffb5b-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="ffb5b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ffb5b-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="ffb5b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ffb5b-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ffb5b-130">See also</span></span>



- [<span data-ttu-id="ffb5b-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ffb5b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

