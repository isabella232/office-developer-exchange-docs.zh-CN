---
title: EmailAddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20049467-c01a-4c7d-8ada-ca1801cc95ed
description: EmailAddressEntity 元素指定的单个电子邮件地址实体。
ms.openlocfilehash: c149ee69c1ed08c33d0341c8dfdac3bcda040afb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754058"
---
# <a name="emailaddressentity"></a><span data-ttu-id="59bc2-103">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="59bc2-103">EmailAddressEntity</span></span>

<span data-ttu-id="59bc2-104">**EmailAddressEntity**元素指定的单个电子邮件地址实体。</span><span class="sxs-lookup"><span data-stu-id="59bc2-104">The **EmailAddressEntity** element specifies a single email address entity.</span></span> 
  
```XML
<EmailAddressEntity>
    <EmailAddress></EmailAddress>
</EmailAddressEntity>
```

 <span data-ttu-id="59bc2-105">**EmailAddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="59bc2-105">**EmailAddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59bc2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="59bc2-106">Attributes and elements</span></span>

<span data-ttu-id="59bc2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="59bc2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59bc2-108">属性</span><span class="sxs-lookup"><span data-stu-id="59bc2-108">Attributes</span></span>

<span data-ttu-id="59bc2-109">无。</span><span class="sxs-lookup"><span data-stu-id="59bc2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59bc2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="59bc2-110">Child elements</span></span>

|<span data-ttu-id="59bc2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="59bc2-111">**Element**</span></span>|<span data-ttu-id="59bc2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="59bc2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59bc2-113">EmailAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="59bc2-113">EmailAddress (string)</span></span>](emailaddress-string.md) <br/> |<span data-ttu-id="59bc2-114">指定单个电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="59bc2-114">Specifies a single email address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="59bc2-115">父元素</span><span class="sxs-lookup"><span data-stu-id="59bc2-115">Parent elements</span></span>

|<span data-ttu-id="59bc2-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="59bc2-116">**Element**</span></span>|<span data-ttu-id="59bc2-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="59bc2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59bc2-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="59bc2-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="59bc2-119">指定电子邮件地址实体的数组。</span><span class="sxs-lookup"><span data-stu-id="59bc2-119">Specifies an array of email address entities.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59bc2-120">备注</span><span class="sxs-lookup"><span data-stu-id="59bc2-120">Remarks</span></span>

<span data-ttu-id="59bc2-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="59bc2-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="59bc2-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="59bc2-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59bc2-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="59bc2-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59bc2-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="59bc2-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="59bc2-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="59bc2-125">Schema Name</span></span>  <br/> |<span data-ttu-id="59bc2-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="59bc2-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="59bc2-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="59bc2-127">Validation File</span></span>  <br/> |<span data-ttu-id="59bc2-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="59bc2-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="59bc2-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="59bc2-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="59bc2-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="59bc2-130">See also</span></span>



- [<span data-ttu-id="59bc2-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="59bc2-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

