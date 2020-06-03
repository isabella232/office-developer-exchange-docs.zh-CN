---
title: ReferenceAttachment
ms.date: 7/7/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b9bde862-6b75-4a81-8033-00a47be4dc2f
description: ReferenceAttachment 元素指定 XXX。
ms.openlocfilehash: a5e4445b24395f1530e072f8aa9b5a9eed02f671
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468738"
---
# <a name="referenceattachment"></a><span data-ttu-id="8c5b9-103">ReferenceAttachment</span><span class="sxs-lookup"><span data-stu-id="8c5b9-103">ReferenceAttachment</span></span>

<span data-ttu-id="8c5b9-104">**ReferenceAttachment**元素指定 XXX。</span><span class="sxs-lookup"><span data-stu-id="8c5b9-104">The **ReferenceAttachment** element specifies XXX.</span></span> 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 <span data-ttu-id="8c5b9-105">**ReferenceAttachmen**</span><span class="sxs-lookup"><span data-stu-id="8c5b9-105">**ReferenceAttachmen**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8c5b9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8c5b9-106">Attributes and elements</span></span>

<span data-ttu-id="8c5b9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8c5b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c5b9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8c5b9-108">Attributes</span></span>

|<span data-ttu-id="8c5b9-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="8c5b9-109">**Attribute**</span></span>|<span data-ttu-id="8c5b9-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="8c5b9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8c5b9-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="8c5b9-111">**Id**</span></span> <br/> |<span data-ttu-id="8c5b9-112">**Id**属性的文本值是定期主项目的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="8c5b9-112">The text value of the **Id** attribute is a recurring master item's unique identifier.</span></span> <span data-ttu-id="8c5b9-113">这是一个**字符串**值。</span><span class="sxs-lookup"><span data-stu-id="8c5b9-113">This is a **string** value.</span></span>  <br/> |
|<span data-ttu-id="8c5b9-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="8c5b9-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="8c5b9-115">**ChangeKey**属性的文本值是定期主项目的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="8c5b9-115">The text value of the **ChangeKey** attribute is the recurring master item's change key.</span></span> <span data-ttu-id="8c5b9-116">这是一个**字符串**值。</span><span class="sxs-lookup"><span data-stu-id="8c5b9-116">This is a **string** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8c5b9-117">子元素</span><span class="sxs-lookup"><span data-stu-id="8c5b9-117">Child elements</span></span>

<span data-ttu-id="8c5b9-118">Range</span><span class="sxs-lookup"><span data-stu-id="8c5b9-118">Ranges</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8c5b9-119">父元素</span><span class="sxs-lookup"><span data-stu-id="8c5b9-119">Parent elements</span></span>

<span data-ttu-id="8c5b9-120">ItemIds |GlobalItemIds |DraftItemIds |ContactIds |Groupid</span><span class="sxs-lookup"><span data-stu-id="8c5b9-120">ItemIds | GlobalItemIds | DraftItemIds| ContactIds | GroupIds</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c5b9-121">备注</span><span class="sxs-lookup"><span data-stu-id="8c5b9-121">Remarks</span></span>

<span data-ttu-id="8c5b9-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8c5b9-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8c5b9-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8c5b9-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c5b9-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="8c5b9-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c5b9-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="8c5b9-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8c5b9-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="8c5b9-126">Schema name</span></span>  <br/> |<span data-ttu-id="8c5b9-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="8c5b9-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="8c5b9-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="8c5b9-128">Validation file</span></span>  <br/> |<span data-ttu-id="8c5b9-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8c5b9-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8c5b9-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="8c5b9-130">Can be empty</span></span>  <br/> ||
   

