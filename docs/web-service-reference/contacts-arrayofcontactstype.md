---
title: 联系人（ArrayOfContactsType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a2c1e833-5f8c-438d-bad7-bb5dcc29ca9e
description: "\"联系人\" 元素指定联系人数组。"
ms.openlocfilehash: eeb202f41fcf5ec7aad12a8a2b8e6dd539b3dba4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529439"
---
# <a name="contacts-arrayofcontactstype"></a><span data-ttu-id="b662c-103">联系人（ArrayOfContactsType）</span><span class="sxs-lookup"><span data-stu-id="b662c-103">Contacts (ArrayOfContactsType)</span></span>

<span data-ttu-id="b662c-104">"**联系人**" 元素指定联系人数组。</span><span class="sxs-lookup"><span data-stu-id="b662c-104">The **Contacts** element specifies an array of contacts.</span></span> 
  
```XML
<Contacts>
    <Contact></Contact>
</Contacts>
```

 <span data-ttu-id="b662c-105">**ArrayOfContactsType**</span><span class="sxs-lookup"><span data-stu-id="b662c-105">**ArrayOfContactsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b662c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b662c-106">Attributes and elements</span></span>

<span data-ttu-id="b662c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b662c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b662c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b662c-108">Attributes</span></span>

<span data-ttu-id="b662c-109">无。</span><span class="sxs-lookup"><span data-stu-id="b662c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b662c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b662c-110">Child elements</span></span>

|<span data-ttu-id="b662c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b662c-111">**Element**</span></span>|<span data-ttu-id="b662c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b662c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b662c-113">Contact （ContactType）</span><span class="sxs-lookup"><span data-stu-id="b662c-113">Contact (ContactType)</span></span>](contact-contacttype.md) <br/> |<span data-ttu-id="b662c-114">指定统一联系人存储库中的联系人。</span><span class="sxs-lookup"><span data-stu-id="b662c-114">Specifies a contact in the Unified Contact Store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b662c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b662c-115">Parent elements</span></span>

|<span data-ttu-id="b662c-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b662c-116">**Element**</span></span>|<span data-ttu-id="b662c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b662c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b662c-118">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="b662c-118">EntityExtractionResult</span></span>](entityextractionresult.md) <br/> |<span data-ttu-id="b662c-119">指定项的**EntityExtractionResult**属性。</span><span class="sxs-lookup"><span data-stu-id="b662c-119">Specifies the **EntityExtractionResult** property of an item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b662c-120">备注</span><span class="sxs-lookup"><span data-stu-id="b662c-120">Remarks</span></span>

<span data-ttu-id="b662c-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b662c-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b662c-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b662c-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b662c-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="b662c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b662c-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="b662c-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b662c-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="b662c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b662c-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="b662c-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="b662c-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="b662c-127">Validation File</span></span>  <br/> |<span data-ttu-id="b662c-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="b662c-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b662c-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="b662c-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b662c-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b662c-130">See also</span></span>



- [<span data-ttu-id="b662c-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b662c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

