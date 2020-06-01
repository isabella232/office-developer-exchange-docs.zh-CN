---
title: IsMembershipGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: IsMembershipGroup 元素指定一个布尔值，该值指示实体是否为通讯组或邮箱。
ms.openlocfilehash: ed79961c6d13ab226c0b489103ef3d2c4a08668d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459284"
---
# <a name="ismembershipgroup"></a><span data-ttu-id="3c982-103">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="3c982-103">IsMembershipGroup</span></span>

<span data-ttu-id="3c982-104">**IsMembershipGroup**元素指定一个布尔值，该值指示实体是否为通讯组或邮箱。</span><span class="sxs-lookup"><span data-stu-id="3c982-104">The **IsMembershipGroup** element specifies a Boolean value that indicates whether the entity is a distribution group or a mailbox.</span></span> 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
```

 <span data-ttu-id="3c982-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3c982-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c982-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3c982-106">Attributes and elements</span></span>

<span data-ttu-id="3c982-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3c982-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c982-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3c982-108">Attributes</span></span>

<span data-ttu-id="3c982-109">无。</span><span class="sxs-lookup"><span data-stu-id="3c982-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c982-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3c982-110">Child elements</span></span>

<span data-ttu-id="3c982-111">无。</span><span class="sxs-lookup"><span data-stu-id="3c982-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3c982-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3c982-112">Parent elements</span></span>

|<span data-ttu-id="3c982-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3c982-113">**Element**</span></span>|<span data-ttu-id="3c982-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3c982-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c982-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="3c982-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="3c982-116">指定从**GetSearchableMailboxes**请求返回的邮箱。</span><span class="sxs-lookup"><span data-stu-id="3c982-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3c982-117">文本值</span><span class="sxs-lookup"><span data-stu-id="3c982-117">Text value</span></span>

<span data-ttu-id="3c982-118">如果**IsMembershipGroup**元素的文本值为**true** ，则表示该实体是通讯组或邮箱。</span><span class="sxs-lookup"><span data-stu-id="3c982-118">A text value of **true** for the **IsMembershipGroup** element indicates that the entity is a distribution group or a mailbox.</span></span> <span data-ttu-id="3c982-119">如果值为 false，则表示该实体不是通讯组或邮箱。</span><span class="sxs-lookup"><span data-stu-id="3c982-119">A value of false indicates that the entity is not a distribution group or a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3c982-120">备注</span><span class="sxs-lookup"><span data-stu-id="3c982-120">Remarks</span></span>

<span data-ttu-id="3c982-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3c982-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3c982-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3c982-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c982-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="3c982-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c982-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="3c982-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3c982-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="3c982-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3c982-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="3c982-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="3c982-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="3c982-127">Validation File</span></span>  <br/> |<span data-ttu-id="3c982-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="3c982-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3c982-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="3c982-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3c982-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3c982-130">See also</span></span>



- [<span data-ttu-id="3c982-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3c982-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

