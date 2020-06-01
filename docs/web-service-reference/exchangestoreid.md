---
title: ExchangeStoreId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5acceb42-a757-4c74-ab1c-b1abf7bf1e0a
description: ExchangeStoreId 元素指定即时消息（IM）组标识符。
ms.openlocfilehash: c1b1e1830987449eeb7ea186d00743ea9cc75a77
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456988"
---
# <a name="exchangestoreid"></a><span data-ttu-id="4976d-103">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="4976d-103">ExchangeStoreId</span></span>

<span data-ttu-id="4976d-104">**ExchangeStoreId**元素指定即时消息（IM）组标识符。</span><span class="sxs-lookup"><span data-stu-id="4976d-104">The **ExchangeStoreId** element specifies the instant messaging (IM) group identifier.</span></span> 
  
```XML
<ExchangeStoreId Id="" ChangeKey=""/>
```

 <span data-ttu-id="4976d-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="4976d-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4976d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4976d-106">Attributes and elements</span></span>

<span data-ttu-id="4976d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4976d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4976d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4976d-108">Attributes</span></span>

|<span data-ttu-id="4976d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="4976d-109">**Attribute**</span></span>|<span data-ttu-id="4976d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="4976d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4976d-111">Id</span><span class="sxs-lookup"><span data-stu-id="4976d-111">Id</span></span>  <br/> |<span data-ttu-id="4976d-112">**Id**属性的文本值是组的标识符。</span><span class="sxs-lookup"><span data-stu-id="4976d-112">The text value of the **Id** attribute is the identifier of the group.</span></span>  <br/> |
|<span data-ttu-id="4976d-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="4976d-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="4976d-114">**ChangeKey**属性的文本值是组的更改键。</span><span class="sxs-lookup"><span data-stu-id="4976d-114">The text value of the **ChangeKey** attribute is the change key of the group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4976d-115">子元素</span><span class="sxs-lookup"><span data-stu-id="4976d-115">Child elements</span></span>

<span data-ttu-id="4976d-116">无。</span><span class="sxs-lookup"><span data-stu-id="4976d-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4976d-117">父元素</span><span class="sxs-lookup"><span data-stu-id="4976d-117">Parent elements</span></span>

|<span data-ttu-id="4976d-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="4976d-118">**Element**</span></span>|<span data-ttu-id="4976d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="4976d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4976d-120">ImGroup</span><span class="sxs-lookup"><span data-stu-id="4976d-120">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="4976d-121">表示即时消息组。</span><span class="sxs-lookup"><span data-stu-id="4976d-121">Represents an instant messaging group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4976d-122">备注</span><span class="sxs-lookup"><span data-stu-id="4976d-122">Remarks</span></span>

<span data-ttu-id="4976d-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4976d-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4976d-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4976d-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4976d-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="4976d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4976d-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="4976d-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4976d-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="4976d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="4976d-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="4976d-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="4976d-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="4976d-129">Validation File</span></span>  <br/> |<span data-ttu-id="4976d-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="4976d-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4976d-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="4976d-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4976d-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4976d-132">See also</span></span>



- [<span data-ttu-id="4976d-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4976d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

