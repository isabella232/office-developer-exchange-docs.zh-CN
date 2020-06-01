---
title: AssistantPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd9ac1-7db3-44ea-9117-18488dddde15
description: AssistantPhoneNumbers 元素指定助理电话号码的数组以及关联角色的源归属的标识符。
ms.openlocfilehash: a72c8d646750b5d7cf9ebca13a51f4df84bf7bdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464481"
---
# <a name="assistantphonenumbers"></a><span data-ttu-id="983ed-103">AssistantPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="983ed-103">AssistantPhoneNumbers</span></span>

<span data-ttu-id="983ed-104">**AssistantPhoneNumbers**元素指定助理电话号码的数组以及关联角色的源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="983ed-104">The **AssistantPhoneNumbers** element specifies an array of assistant phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<AssistantPhoneNumbers>
    <PhoneNumberAttributedValue></PhoneNumberAttributedValue>
</AssistantPhoneNumbers>
```

 <span data-ttu-id="983ed-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="983ed-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="983ed-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="983ed-106">Attributes and elements</span></span>

<span data-ttu-id="983ed-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="983ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="983ed-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="983ed-108">Attributes</span></span>

<span data-ttu-id="983ed-109">无。</span><span class="sxs-lookup"><span data-stu-id="983ed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="983ed-110">子元素</span><span class="sxs-lookup"><span data-stu-id="983ed-110">Child elements</span></span>

|<span data-ttu-id="983ed-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="983ed-111">**Element**</span></span>|<span data-ttu-id="983ed-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="983ed-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="983ed-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="983ed-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="983ed-114">指定电话号码数组的实例及其关联的归属。</span><span class="sxs-lookup"><span data-stu-id="983ed-114">Specifies an instance of an array of phone numbers and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="983ed-115">父元素</span><span class="sxs-lookup"><span data-stu-id="983ed-115">Parent elements</span></span>

|<span data-ttu-id="983ed-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="983ed-116">**Element**</span></span>|<span data-ttu-id="983ed-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="983ed-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="983ed-118">角色</span><span class="sxs-lookup"><span data-stu-id="983ed-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="983ed-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="983ed-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="983ed-120">备注</span><span class="sxs-lookup"><span data-stu-id="983ed-120">Remarks</span></span>

<span data-ttu-id="983ed-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="983ed-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="983ed-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="983ed-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="983ed-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="983ed-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="983ed-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="983ed-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="983ed-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="983ed-125">Schema Name</span></span>  <br/> |<span data-ttu-id="983ed-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="983ed-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="983ed-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="983ed-127">Validation File</span></span>  <br/> |<span data-ttu-id="983ed-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="983ed-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="983ed-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="983ed-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="983ed-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="983ed-130">See also</span></span>

- [<span data-ttu-id="983ed-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="983ed-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

