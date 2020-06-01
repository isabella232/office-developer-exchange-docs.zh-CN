---
title: AdditionalInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 50bebbab-2fef-4a27-a5a9-32d7200820b6
description: AdditionalInfo 元素指定有关邮箱的保留状态的其他信息。
ms.openlocfilehash: 1911ff3ac0baf7a8854c0609e08959a54cc27b6d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455819"
---
# <a name="additionalinfo"></a><span data-ttu-id="bc160-103">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="bc160-103">AdditionalInfo</span></span>

<span data-ttu-id="bc160-104">**AdditionalInfo**元素指定有关邮箱的保留状态的其他信息。</span><span class="sxs-lookup"><span data-stu-id="bc160-104">The **AdditionalInfo** element specifies additional information about the hold status of a mailbox.</span></span> 
  
```XML
<AdditionalInfo></AdditionalInfo>
```

 <span data-ttu-id="bc160-105">**xs： string**</span><span class="sxs-lookup"><span data-stu-id="bc160-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bc160-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bc160-106">Attributes and elements</span></span>

<span data-ttu-id="bc160-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bc160-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc160-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bc160-108">Attributes</span></span>

<span data-ttu-id="bc160-109">无。</span><span class="sxs-lookup"><span data-stu-id="bc160-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc160-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bc160-110">Child elements</span></span>

<span data-ttu-id="bc160-111">无。</span><span class="sxs-lookup"><span data-stu-id="bc160-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bc160-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bc160-112">Parent elements</span></span>

|<span data-ttu-id="bc160-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc160-113">**Element**</span></span>|<span data-ttu-id="bc160-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc160-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc160-115">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="bc160-115">MailboxHoldStatus</span></span>](mailboxholdstatus.md) <br/> |<span data-ttu-id="bc160-116">指定邮箱的保留状态。</span><span class="sxs-lookup"><span data-stu-id="bc160-116">Specifies the hold status of the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bc160-117">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="bc160-117">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md) <br/> |<span data-ttu-id="bc160-118">指定无法编制索引的项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="bc160-118">Specifies detail for an item that cannot be indexed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bc160-119">文本值</span><span class="sxs-lookup"><span data-stu-id="bc160-119">Text value</span></span>

<span data-ttu-id="bc160-120">AdditionalInfo 元素的文本值是有关邮箱保留状态的其他信息。</span><span class="sxs-lookup"><span data-stu-id="bc160-120">The text value of the AdditionalInfo element is additional information about the hold status of a mailbox.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc160-121">说明</span><span class="sxs-lookup"><span data-stu-id="bc160-121">Remarks</span></span>

<span data-ttu-id="bc160-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="bc160-122">This element is optional.</span></span>
  
<span data-ttu-id="bc160-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bc160-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="bc160-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bc160-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc160-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="bc160-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc160-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="bc160-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bc160-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="bc160-127">Schema Name</span></span>  <br/> |<span data-ttu-id="bc160-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="bc160-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="bc160-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="bc160-129">Validation File</span></span>  <br/> |<span data-ttu-id="bc160-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="bc160-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="bc160-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="bc160-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="bc160-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bc160-132">See also</span></span>

- [<span data-ttu-id="bc160-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bc160-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

