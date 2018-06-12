---
title: MarkAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MarkAsRead
api_type:
- schema
ms.assetid: 404842e1-fbdb-480d-a1d8-ba1ab2c9fb1e
description: MarkAsRead 元素表示邮件是否被标记为只读。
ms.openlocfilehash: b453ad73912e99b6fd3aed84b03a7d2fc2b6a294
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826355"
---
# <a name="markasread"></a><span data-ttu-id="5235f-103">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="5235f-103">MarkAsRead</span></span>

<span data-ttu-id="5235f-104">**MarkAsRead**元素表示邮件是否被标记为只读。</span><span class="sxs-lookup"><span data-stu-id="5235f-104">The **MarkAsRead** element indicates whether messages are to be marked as read.</span></span> 
  
```XML
<MarkAsRead>true | false</MarkAsRead>
```

 <span data-ttu-id="5235f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5235f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5235f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5235f-106">Attributes and elements</span></span>

<span data-ttu-id="5235f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5235f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5235f-108">属性</span><span class="sxs-lookup"><span data-stu-id="5235f-108">Attributes</span></span>

<span data-ttu-id="5235f-109">无。</span><span class="sxs-lookup"><span data-stu-id="5235f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5235f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5235f-110">Child elements</span></span>

<span data-ttu-id="5235f-111">无。</span><span class="sxs-lookup"><span data-stu-id="5235f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5235f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5235f-112">Parent elements</span></span>

|<span data-ttu-id="5235f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5235f-113">**Element**</span></span>|<span data-ttu-id="5235f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5235f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5235f-115">操作</span><span class="sxs-lookup"><span data-stu-id="5235f-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="5235f-116">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="5235f-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5235f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="5235f-117">Text value</span></span>

<span data-ttu-id="5235f-118">文本值为**true**指示邮件，必须标记为已读。</span><span class="sxs-lookup"><span data-stu-id="5235f-118">A text value of **true** indicates that the message must be marked as read.</span></span> <span data-ttu-id="5235f-119">如果值为**false**指示邮件，不得标记为已读。</span><span class="sxs-lookup"><span data-stu-id="5235f-119">A value of **false** indicates that messages must not be marked as read.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5235f-120">备注</span><span class="sxs-lookup"><span data-stu-id="5235f-120">Remarks</span></span>

<span data-ttu-id="5235f-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5235f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5235f-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="5235f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5235f-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="5235f-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5235f-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="5235f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="5235f-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="5235f-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5235f-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="5235f-126">Validation File</span></span>  <br/> |<span data-ttu-id="5235f-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5235f-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5235f-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="5235f-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="5235f-129">True</span><span class="sxs-lookup"><span data-stu-id="5235f-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5235f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5235f-130">See also</span></span>



- [<span data-ttu-id="5235f-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5235f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

