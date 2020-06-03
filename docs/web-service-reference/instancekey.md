---
title: InstanceKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb4dbe9b-aea0-4527-b7d6-e928066caf38
description: InstanceKey 元素指定项或对话的实例键。
ms.openlocfilehash: a6b55b9021fe63be7f678f0a1bcb24e88aeba005
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459971"
---
# <a name="instancekey"></a><span data-ttu-id="91545-103">InstanceKey</span><span class="sxs-lookup"><span data-stu-id="91545-103">InstanceKey</span></span>

<span data-ttu-id="91545-104">**InstanceKey**元素指定项或对话的实例键。</span><span class="sxs-lookup"><span data-stu-id="91545-104">The **InstanceKey** element specifies an instance key for an item or conversation.</span></span> 
  
```XML
<InstanceKey></InstanceKey>
```

 <span data-ttu-id="91545-105">**base64Binary**</span><span class="sxs-lookup"><span data-stu-id="91545-105">**base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91545-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="91545-106">Attributes and elements</span></span>

<span data-ttu-id="91545-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="91545-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91545-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="91545-108">Attributes</span></span>

<span data-ttu-id="91545-109">无。</span><span class="sxs-lookup"><span data-stu-id="91545-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91545-110">子元素</span><span class="sxs-lookup"><span data-stu-id="91545-110">Child elements</span></span>

<span data-ttu-id="91545-111">无。</span><span class="sxs-lookup"><span data-stu-id="91545-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="91545-112">父元素</span><span class="sxs-lookup"><span data-stu-id="91545-112">Parent elements</span></span>

|<span data-ttu-id="91545-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="91545-113">**Element**</span></span>|<span data-ttu-id="91545-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="91545-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91545-115">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="91545-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="91545-116">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="91545-116">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="91545-117">项</span><span class="sxs-lookup"><span data-stu-id="91545-117">Item</span></span>](item.md) <br/> |<span data-ttu-id="91545-118">表示 Exchange 存储中的一般项目。</span><span class="sxs-lookup"><span data-stu-id="91545-118">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="91545-119">文本值</span><span class="sxs-lookup"><span data-stu-id="91545-119">Text value</span></span>

<span data-ttu-id="91545-120">**InstanceKey**元素的文本值是项目或对话的实例键。</span><span class="sxs-lookup"><span data-stu-id="91545-120">The text value of the **InstanceKey** element is the instance key for an item or conversation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="91545-121">备注</span><span class="sxs-lookup"><span data-stu-id="91545-121">Remarks</span></span>

<span data-ttu-id="91545-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="91545-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="91545-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="91545-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91545-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="91545-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91545-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="91545-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="91545-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="91545-126">Schema Name</span></span>  <br/> |<span data-ttu-id="91545-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="91545-127">Type schema</span></span>  <br/> |
|<span data-ttu-id="91545-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="91545-128">Validation File</span></span>  <br/> |<span data-ttu-id="91545-129">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="91545-129">types.xsd</span></span>  <br/> |
|<span data-ttu-id="91545-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="91545-130">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="91545-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="91545-131">See also</span></span>



- [<span data-ttu-id="91545-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="91545-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

