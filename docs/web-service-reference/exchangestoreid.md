---
title: ExchangeStoreId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5acceb42-a757-4c74-ab1c-b1abf7bf1e0a
description: ExchangeStoreId 元素指定的即时消息 (IM) 组标识符。
ms.openlocfilehash: 815e9c2f368558ea38efce3671dbdc33d4d97168
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754187"
---
# <a name="exchangestoreid"></a><span data-ttu-id="c5a08-103">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="c5a08-103">ExchangeStoreId</span></span>

<span data-ttu-id="c5a08-104">**ExchangeStoreId**元素指定的即时消息 (IM) 组标识符。</span><span class="sxs-lookup"><span data-stu-id="c5a08-104">The **ExchangeStoreId** element specifies the instant messaging (IM) group identifier.</span></span> 
  
```XML
<ExchangeStoreId Id="" ChangeKey=""/>
```

 <span data-ttu-id="c5a08-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="c5a08-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5a08-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c5a08-106">Attributes and elements</span></span>

<span data-ttu-id="c5a08-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c5a08-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5a08-108">属性</span><span class="sxs-lookup"><span data-stu-id="c5a08-108">Attributes</span></span>

|<span data-ttu-id="c5a08-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c5a08-109">**Attribute**</span></span>|<span data-ttu-id="c5a08-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c5a08-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c5a08-111">Id</span><span class="sxs-lookup"><span data-stu-id="c5a08-111">Id</span></span>  <br/> |<span data-ttu-id="c5a08-112">**Id**属性的文本值是组的标识符。</span><span class="sxs-lookup"><span data-stu-id="c5a08-112">The text value of the **Id** attribute is the identifier of the group.</span></span>  <br/> |
|<span data-ttu-id="c5a08-113">更改密钥</span><span class="sxs-lookup"><span data-stu-id="c5a08-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="c5a08-114">**更改密钥**属性的文本值是组的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="c5a08-114">The text value of the **ChangeKey** attribute is the change key of the group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c5a08-115">子元素</span><span class="sxs-lookup"><span data-stu-id="c5a08-115">Child elements</span></span>

<span data-ttu-id="c5a08-116">无。</span><span class="sxs-lookup"><span data-stu-id="c5a08-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5a08-117">父元素</span><span class="sxs-lookup"><span data-stu-id="c5a08-117">Parent elements</span></span>

|<span data-ttu-id="c5a08-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="c5a08-118">**Element**</span></span>|<span data-ttu-id="c5a08-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="c5a08-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5a08-120">ImGroup</span><span class="sxs-lookup"><span data-stu-id="c5a08-120">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="c5a08-121">代表一个即时消息的组。</span><span class="sxs-lookup"><span data-stu-id="c5a08-121">Represents an instant messaging group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5a08-122">备注</span><span class="sxs-lookup"><span data-stu-id="c5a08-122">Remarks</span></span>

<span data-ttu-id="c5a08-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c5a08-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c5a08-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c5a08-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5a08-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="c5a08-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5a08-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="c5a08-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5a08-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="c5a08-127">Schema Name</span></span>  <br/> |<span data-ttu-id="c5a08-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="c5a08-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="c5a08-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="c5a08-129">Validation File</span></span>  <br/> |<span data-ttu-id="c5a08-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5a08-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5a08-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="c5a08-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c5a08-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c5a08-132">See also</span></span>



- [<span data-ttu-id="c5a08-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c5a08-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

