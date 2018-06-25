---
title: EmailAddresses (ArrayOfEmailAddressEntitiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2fc4a8e8-5377-4059-8fb4-3fdabfd30fe3
description: EmailAddresses 元素指定电子邮件地址实体的数组。
ms.openlocfilehash: 8d96d49ef2420f269197e47577efb956daa64e53
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754057"
---
# <a name="emailaddresses-arrayofemailaddressentitiestype"></a><span data-ttu-id="52317-103">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="52317-103">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>

<span data-ttu-id="52317-104">**EmailAddresses**元素指定电子邮件地址实体的数组。</span><span class="sxs-lookup"><span data-stu-id="52317-104">The **EmailAddresses** element specifies an array of email address entities.</span></span> 
  
```XML
<EmailAddresses>
    <EmailAddressEntity></EmailAddressEntity>
</EmailAddresses>
```

 <span data-ttu-id="52317-105">**ArrayOfEmailAddressEntitiesType**</span><span class="sxs-lookup"><span data-stu-id="52317-105">**ArrayOfEmailAddressEntitiesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52317-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52317-106">Attributes and elements</span></span>

<span data-ttu-id="52317-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52317-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52317-108">属性</span><span class="sxs-lookup"><span data-stu-id="52317-108">Attributes</span></span>

<span data-ttu-id="52317-109">无。</span><span class="sxs-lookup"><span data-stu-id="52317-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52317-110">子元素</span><span class="sxs-lookup"><span data-stu-id="52317-110">Child elements</span></span>

|<span data-ttu-id="52317-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="52317-111">**Element**</span></span>|<span data-ttu-id="52317-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="52317-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52317-113">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="52317-113">EmailAddressEntity</span></span>](emailaddressentity.md) <br/> |<span data-ttu-id="52317-114">指定单个电子邮件地址实体。</span><span class="sxs-lookup"><span data-stu-id="52317-114">Specifies a single email address entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52317-115">父元素</span><span class="sxs-lookup"><span data-stu-id="52317-115">Parent elements</span></span>

|<span data-ttu-id="52317-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="52317-116">**Element**</span></span>|<span data-ttu-id="52317-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="52317-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52317-118">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="52317-118">EntityExtractionResult</span></span>](entityextractionresult.md) <br/> |<span data-ttu-id="52317-119">指定项目的**EntityExtractionResult**属性。</span><span class="sxs-lookup"><span data-stu-id="52317-119">Specifies the **EntityExtractionResult** property of an item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52317-120">备注</span><span class="sxs-lookup"><span data-stu-id="52317-120">Remarks</span></span>

<span data-ttu-id="52317-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="52317-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="52317-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52317-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52317-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="52317-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52317-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="52317-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52317-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="52317-125">Schema Name</span></span>  <br/> |<span data-ttu-id="52317-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="52317-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="52317-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="52317-127">Validation File</span></span>  <br/> |<span data-ttu-id="52317-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="52317-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="52317-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="52317-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="52317-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52317-130">See also</span></span>



- [<span data-ttu-id="52317-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="52317-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

