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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754058"
---
# <a name="emailaddressentity"></a><span data-ttu-id="f51d0-103">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="f51d0-103">EmailAddressEntity</span></span>

<span data-ttu-id="f51d0-104">**EmailAddressEntity**元素指定的单个电子邮件地址实体。</span><span class="sxs-lookup"><span data-stu-id="f51d0-104">The **EmailAddressEntity** element specifies a single email address entity.</span></span> 
  
```XML
<EmailAddressEntity>
    <EmailAddress></EmailAddress>
</EmailAddressEntity>
```

 <span data-ttu-id="f51d0-105">**EmailAddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="f51d0-105">**EmailAddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f51d0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f51d0-106">Attributes and elements</span></span>

<span data-ttu-id="f51d0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f51d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f51d0-108">属性</span><span class="sxs-lookup"><span data-stu-id="f51d0-108">Attributes</span></span>

<span data-ttu-id="f51d0-109">无。</span><span class="sxs-lookup"><span data-stu-id="f51d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f51d0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f51d0-110">Child elements</span></span>

|<span data-ttu-id="f51d0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f51d0-111">**Element**</span></span>|<span data-ttu-id="f51d0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f51d0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f51d0-113">EmailAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="f51d0-113">EmailAddress (string)</span></span>](emailaddress-string.md) <br/> |<span data-ttu-id="f51d0-114">指定单个电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f51d0-114">Specifies a single email address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f51d0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f51d0-115">Parent elements</span></span>

|<span data-ttu-id="f51d0-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f51d0-116">**Element**</span></span>|<span data-ttu-id="f51d0-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f51d0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f51d0-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="f51d0-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="f51d0-119">指定电子邮件地址实体的数组。</span><span class="sxs-lookup"><span data-stu-id="f51d0-119">Specifies an array of email address entities.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f51d0-120">备注</span><span class="sxs-lookup"><span data-stu-id="f51d0-120">Remarks</span></span>

<span data-ttu-id="f51d0-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f51d0-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f51d0-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f51d0-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f51d0-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f51d0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f51d0-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f51d0-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f51d0-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f51d0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f51d0-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="f51d0-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f51d0-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f51d0-127">Validation File</span></span>  <br/> |<span data-ttu-id="f51d0-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="f51d0-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f51d0-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f51d0-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f51d0-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f51d0-130">See also</span></span>



- [<span data-ttu-id="f51d0-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f51d0-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

