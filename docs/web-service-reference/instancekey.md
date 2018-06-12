---
title: InstanceKey
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb4dbe9b-aea0-4527-b7d6-e928066caf38
description: InstanceKey 元素指定项目或会话实例的密钥。
ms.openlocfilehash: a0e4f9390d5dc368388b5a20e38796c6c0157a40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825943"
---
# <a name="instancekey"></a><span data-ttu-id="c8fc1-103">InstanceKey</span><span class="sxs-lookup"><span data-stu-id="c8fc1-103">InstanceKey</span></span>

<span data-ttu-id="c8fc1-104">**InstanceKey**元素指定项目或会话实例的密钥。</span><span class="sxs-lookup"><span data-stu-id="c8fc1-104">The **InstanceKey** element specifies an instance key for an item or conversation.</span></span> 
  
```XML
<InstanceKey></InstanceKey>
```

 <span data-ttu-id="c8fc1-105">**base64Binary**</span><span class="sxs-lookup"><span data-stu-id="c8fc1-105">**base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8fc1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c8fc1-106">Attributes and elements</span></span>

<span data-ttu-id="c8fc1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c8fc1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8fc1-108">属性</span><span class="sxs-lookup"><span data-stu-id="c8fc1-108">Attributes</span></span>

<span data-ttu-id="c8fc1-109">无。</span><span class="sxs-lookup"><span data-stu-id="c8fc1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8fc1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c8fc1-110">Child elements</span></span>

<span data-ttu-id="c8fc1-111">无。</span><span class="sxs-lookup"><span data-stu-id="c8fc1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c8fc1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c8fc1-112">Parent elements</span></span>

|<span data-ttu-id="c8fc1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c8fc1-113">**Element**</span></span>|<span data-ttu-id="c8fc1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c8fc1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8fc1-115">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c8fc1-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="c8fc1-116">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="c8fc1-116">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="c8fc1-117">Item</span><span class="sxs-lookup"><span data-stu-id="c8fc1-117">Item</span></span>](item.md) <br/> |<span data-ttu-id="c8fc1-118">表示 Exchange 存储中的泛型项。</span><span class="sxs-lookup"><span data-stu-id="c8fc1-118">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8fc1-119">文本值</span><span class="sxs-lookup"><span data-stu-id="c8fc1-119">Text value</span></span>

<span data-ttu-id="c8fc1-120">**InstanceKey**元素的文本值是项目或对话的实例密钥。</span><span class="sxs-lookup"><span data-stu-id="c8fc1-120">The text value of the **InstanceKey** element is the instance key for an item or conversation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c8fc1-121">备注</span><span class="sxs-lookup"><span data-stu-id="c8fc1-121">Remarks</span></span>

<span data-ttu-id="c8fc1-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c8fc1-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c8fc1-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c8fc1-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8fc1-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c8fc1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8fc1-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c8fc1-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8fc1-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c8fc1-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c8fc1-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="c8fc1-127">Type schema</span></span>  <br/> |
|<span data-ttu-id="c8fc1-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c8fc1-128">Validation File</span></span>  <br/> |<span data-ttu-id="c8fc1-129">types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8fc1-129">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8fc1-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c8fc1-130">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c8fc1-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c8fc1-131">See also</span></span>



- [<span data-ttu-id="c8fc1-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c8fc1-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

