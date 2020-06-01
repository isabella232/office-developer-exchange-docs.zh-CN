---
title: EmailAddresses （ArrayOfEmailAddressEntitiesType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2fc4a8e8-5377-4059-8fb4-3fdabfd30fe3
description: EmailAddresses 元素指定电子邮件地址实体的数组。
ms.openlocfilehash: bd478b369f3b359edc6007db9231af50c36877e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463424"
---
# <a name="emailaddresses-arrayofemailaddressentitiestype"></a><span data-ttu-id="9389a-103">EmailAddresses （ArrayOfEmailAddressEntitiesType）</span><span class="sxs-lookup"><span data-stu-id="9389a-103">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>

<span data-ttu-id="9389a-104">**EmailAddresses**元素指定电子邮件地址实体的数组。</span><span class="sxs-lookup"><span data-stu-id="9389a-104">The **EmailAddresses** element specifies an array of email address entities.</span></span> 
  
```XML
<EmailAddresses>
    <EmailAddressEntity></EmailAddressEntity>
</EmailAddresses>
```

 <span data-ttu-id="9389a-105">**ArrayOfEmailAddressEntitiesType**</span><span class="sxs-lookup"><span data-stu-id="9389a-105">**ArrayOfEmailAddressEntitiesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9389a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9389a-106">Attributes and elements</span></span>

<span data-ttu-id="9389a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9389a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9389a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9389a-108">Attributes</span></span>

<span data-ttu-id="9389a-109">无。</span><span class="sxs-lookup"><span data-stu-id="9389a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9389a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9389a-110">Child elements</span></span>

|<span data-ttu-id="9389a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9389a-111">**Element**</span></span>|<span data-ttu-id="9389a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9389a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9389a-113">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="9389a-113">EmailAddressEntity</span></span>](emailaddressentity.md) <br/> |<span data-ttu-id="9389a-114">指定一个电子邮件地址实体。</span><span class="sxs-lookup"><span data-stu-id="9389a-114">Specifies a single email address entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9389a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9389a-115">Parent elements</span></span>

|<span data-ttu-id="9389a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9389a-116">**Element**</span></span>|<span data-ttu-id="9389a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9389a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9389a-118">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="9389a-118">EntityExtractionResult</span></span>](entityextractionresult.md) <br/> |<span data-ttu-id="9389a-119">指定项的**EntityExtractionResult**属性。</span><span class="sxs-lookup"><span data-stu-id="9389a-119">Specifies the **EntityExtractionResult** property of an item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9389a-120">备注</span><span class="sxs-lookup"><span data-stu-id="9389a-120">Remarks</span></span>

<span data-ttu-id="9389a-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9389a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9389a-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9389a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9389a-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="9389a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9389a-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="9389a-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9389a-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="9389a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9389a-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="9389a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="9389a-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="9389a-127">Validation File</span></span>  <br/> |<span data-ttu-id="9389a-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="9389a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9389a-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="9389a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9389a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9389a-130">See also</span></span>



- [<span data-ttu-id="9389a-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9389a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

