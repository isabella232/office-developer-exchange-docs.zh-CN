---
title: EmailAddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20049467-c01a-4c7d-8ada-ca1801cc95ed
description: EmailAddressEntity 元素指定单个电子邮件地址实体。
ms.openlocfilehash: b76b08f93e60c8492906f3cc94e60f5725c8a9dc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526219"
---
# <a name="emailaddressentity"></a><span data-ttu-id="25434-103">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="25434-103">EmailAddressEntity</span></span>

<span data-ttu-id="25434-104">**EmailAddressEntity**元素指定单个电子邮件地址实体。</span><span class="sxs-lookup"><span data-stu-id="25434-104">The **EmailAddressEntity** element specifies a single email address entity.</span></span> 
  
```XML
<EmailAddressEntity>
    <EmailAddress></EmailAddress>
</EmailAddressEntity>
```

 <span data-ttu-id="25434-105">**EmailAddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="25434-105">**EmailAddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25434-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="25434-106">Attributes and elements</span></span>

<span data-ttu-id="25434-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="25434-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25434-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="25434-108">Attributes</span></span>

<span data-ttu-id="25434-109">无。</span><span class="sxs-lookup"><span data-stu-id="25434-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25434-110">子元素</span><span class="sxs-lookup"><span data-stu-id="25434-110">Child elements</span></span>

|<span data-ttu-id="25434-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="25434-111">**Element**</span></span>|<span data-ttu-id="25434-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="25434-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25434-113">EmailAddress （字符串）</span><span class="sxs-lookup"><span data-stu-id="25434-113">EmailAddress (string)</span></span>](emailaddress-string.md) <br/> |<span data-ttu-id="25434-114">指定一个电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="25434-114">Specifies a single email address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="25434-115">父元素</span><span class="sxs-lookup"><span data-stu-id="25434-115">Parent elements</span></span>

|<span data-ttu-id="25434-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="25434-116">**Element**</span></span>|<span data-ttu-id="25434-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="25434-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25434-118">EmailAddresses （ArrayOfEmailAddressEntitiesType）</span><span class="sxs-lookup"><span data-stu-id="25434-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="25434-119">指定电子邮件地址实体的数组。</span><span class="sxs-lookup"><span data-stu-id="25434-119">Specifies an array of email address entities.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25434-120">备注</span><span class="sxs-lookup"><span data-stu-id="25434-120">Remarks</span></span>

<span data-ttu-id="25434-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="25434-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="25434-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="25434-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25434-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="25434-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25434-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="25434-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25434-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="25434-125">Schema Name</span></span>  <br/> |<span data-ttu-id="25434-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="25434-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="25434-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="25434-127">Validation File</span></span>  <br/> |<span data-ttu-id="25434-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="25434-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="25434-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="25434-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="25434-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="25434-130">See also</span></span>



- [<span data-ttu-id="25434-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="25434-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

