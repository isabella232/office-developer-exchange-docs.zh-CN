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
description: MarkAsRead 元素指示是否将邮件标记为已读。
ms.openlocfilehash: 691409a4eace8885d36f4b30b8eef1aca8c332a6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461763"
---
# <a name="markasread"></a><span data-ttu-id="9068a-103">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="9068a-103">MarkAsRead</span></span>

<span data-ttu-id="9068a-104">**MarkAsRead**元素指示是否将邮件标记为已读。</span><span class="sxs-lookup"><span data-stu-id="9068a-104">The **MarkAsRead** element indicates whether messages are to be marked as read.</span></span> 
  
```XML
<MarkAsRead>true | false</MarkAsRead>
```

 <span data-ttu-id="9068a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9068a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9068a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9068a-106">Attributes and elements</span></span>

<span data-ttu-id="9068a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9068a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9068a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9068a-108">Attributes</span></span>

<span data-ttu-id="9068a-109">无。</span><span class="sxs-lookup"><span data-stu-id="9068a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9068a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9068a-110">Child elements</span></span>

<span data-ttu-id="9068a-111">无。</span><span class="sxs-lookup"><span data-stu-id="9068a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9068a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9068a-112">Parent elements</span></span>

|<span data-ttu-id="9068a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9068a-113">**Element**</span></span>|<span data-ttu-id="9068a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9068a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9068a-115">操作</span><span class="sxs-lookup"><span data-stu-id="9068a-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="9068a-116">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="9068a-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9068a-117">文本值</span><span class="sxs-lookup"><span data-stu-id="9068a-117">Text value</span></span>

<span data-ttu-id="9068a-118">如果文本值为**true** ，则表示必须将邮件标记为已读。</span><span class="sxs-lookup"><span data-stu-id="9068a-118">A text value of **true** indicates that the message must be marked as read.</span></span> <span data-ttu-id="9068a-119">**如果值为 false，则**表示邮件不能标记为已读。</span><span class="sxs-lookup"><span data-stu-id="9068a-119">A value of **false** indicates that messages must not be marked as read.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9068a-120">说明</span><span class="sxs-lookup"><span data-stu-id="9068a-120">Remarks</span></span>

<span data-ttu-id="9068a-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9068a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9068a-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="9068a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9068a-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="9068a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9068a-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="9068a-124">Schema Name</span></span>  <br/> |<span data-ttu-id="9068a-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="9068a-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9068a-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="9068a-126">Validation File</span></span>  <br/> |<span data-ttu-id="9068a-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9068a-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9068a-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="9068a-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="9068a-129">True</span><span class="sxs-lookup"><span data-stu-id="9068a-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9068a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9068a-130">See also</span></span>



- [<span data-ttu-id="9068a-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9068a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

