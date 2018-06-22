---
title: AssistantPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd9ac1-7db3-44ea-9117-18488dddde15
description: AssistantPhoneNumbers 元素指定一个数组助理电话号码和为相关联的角色其源归属的标识符。
ms.openlocfilehash: 747835102af28d94d60b763fdbc5b2ea0947d47e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753273"
---
# <a name="assistantphonenumbers"></a><span data-ttu-id="9d26b-103">AssistantPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="9d26b-103">AssistantPhoneNumbers</span></span>

<span data-ttu-id="9d26b-104">**AssistantPhoneNumbers**元素指定一个数组助理电话号码和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="9d26b-104">The **AssistantPhoneNumbers** element specifies an array of assistant phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantPhoneNumbers>
    <PhoneNumberAttributedValue></PhoneNumberAttributedValue>
</AssistantPhoneNumbers>
```

 <span data-ttu-id="9d26b-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="9d26b-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d26b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9d26b-106">Attributes and elements</span></span>

<span data-ttu-id="9d26b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9d26b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d26b-108">属性</span><span class="sxs-lookup"><span data-stu-id="9d26b-108">Attributes</span></span>

<span data-ttu-id="9d26b-109">无。</span><span class="sxs-lookup"><span data-stu-id="9d26b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d26b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9d26b-110">Child elements</span></span>

|<span data-ttu-id="9d26b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9d26b-111">**Element**</span></span>|<span data-ttu-id="9d26b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9d26b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d26b-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="9d26b-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="9d26b-114">指定一个电话号码和其关联的归属的数组的实例。</span><span class="sxs-lookup"><span data-stu-id="9d26b-114">Specifies an instance of an array of phone numbers and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d26b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9d26b-115">Parent elements</span></span>

|<span data-ttu-id="9d26b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9d26b-116">**Element**</span></span>|<span data-ttu-id="9d26b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9d26b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d26b-118">角色</span><span class="sxs-lookup"><span data-stu-id="9d26b-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="9d26b-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="9d26b-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d26b-120">备注</span><span class="sxs-lookup"><span data-stu-id="9d26b-120">Remarks</span></span>

<span data-ttu-id="9d26b-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9d26b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9d26b-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9d26b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d26b-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="9d26b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d26b-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="9d26b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9d26b-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="9d26b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9d26b-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="9d26b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="9d26b-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="9d26b-127">Validation File</span></span>  <br/> |<span data-ttu-id="9d26b-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="9d26b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9d26b-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="9d26b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9d26b-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9d26b-130">See also</span></span>

- [<span data-ttu-id="9d26b-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9d26b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

