---
title: IsMembershipGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: IsMembershipGroup 元素指定一个布尔值，该值指示是否实体为通讯组或邮箱。
ms.openlocfilehash: 03ab0dc75d2c798b7f2afeef85aa45f0349be70a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826050"
---
# <a name="ismembershipgroup"></a><span data-ttu-id="4910f-103">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="4910f-103">IsMembershipGroup</span></span>

<span data-ttu-id="4910f-104">**IsMembershipGroup**元素指定一个布尔值，该值指示是否实体为通讯组或邮箱。</span><span class="sxs-lookup"><span data-stu-id="4910f-104">The **IsMembershipGroup** element specifies a Boolean value that indicates whether the entity is a distribution group or a mailbox.</span></span> 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
```

 <span data-ttu-id="4910f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4910f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4910f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4910f-106">Attributes and elements</span></span>

<span data-ttu-id="4910f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4910f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4910f-108">属性</span><span class="sxs-lookup"><span data-stu-id="4910f-108">Attributes</span></span>

<span data-ttu-id="4910f-109">无。</span><span class="sxs-lookup"><span data-stu-id="4910f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4910f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4910f-110">Child elements</span></span>

<span data-ttu-id="4910f-111">无。</span><span class="sxs-lookup"><span data-stu-id="4910f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4910f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4910f-112">Parent elements</span></span>

|<span data-ttu-id="4910f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4910f-113">**Element**</span></span>|<span data-ttu-id="4910f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4910f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4910f-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="4910f-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="4910f-116">指定从**GetSearchableMailboxes**请求返回的邮箱。</span><span class="sxs-lookup"><span data-stu-id="4910f-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4910f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="4910f-117">Text value</span></span>

<span data-ttu-id="4910f-118">文本值为**true**的**IsMembershipGroup**元素表示的实体是通讯组或邮箱。</span><span class="sxs-lookup"><span data-stu-id="4910f-118">A text value of **true** for the **IsMembershipGroup** element indicates that the entity is a distribution group or a mailbox.</span></span> <span data-ttu-id="4910f-119">值为 false 指示该实体不通讯组或邮箱。</span><span class="sxs-lookup"><span data-stu-id="4910f-119">A value of false indicates that the entity is not a distribution group or a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4910f-120">备注</span><span class="sxs-lookup"><span data-stu-id="4910f-120">Remarks</span></span>

<span data-ttu-id="4910f-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4910f-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4910f-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4910f-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4910f-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="4910f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4910f-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="4910f-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4910f-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="4910f-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4910f-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="4910f-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="4910f-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="4910f-127">Validation File</span></span>  <br/> |<span data-ttu-id="4910f-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="4910f-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4910f-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="4910f-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4910f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4910f-130">See also</span></span>



- [<span data-ttu-id="4910f-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4910f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

