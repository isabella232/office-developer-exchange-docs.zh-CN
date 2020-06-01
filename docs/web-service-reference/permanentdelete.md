---
title: PermanentDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermanentDelete
api_type:
- schema
ms.assetid: 1a0e0f46-1472-4eb7-bb54-f193a2603587
description: PermanentDelete 元素指示是否要永久删除邮件，而不将邮件保存到 "已删除邮件" 文件夹。
ms.openlocfilehash: da7680eefca9ad359948af38eac49d18e9055988
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467765"
---
# <a name="permanentdelete"></a><span data-ttu-id="cd413-103">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="cd413-103">PermanentDelete</span></span>

<span data-ttu-id="cd413-104">**PermanentDelete**元素指示是否要永久删除邮件，而不将邮件保存到 "已删除邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="cd413-104">The **PermanentDelete** element indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span> 
  
```XML
<PermanentDelete>true | false</PermanentDelete>
```

 <span data-ttu-id="cd413-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cd413-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd413-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cd413-106">Attributes and elements</span></span>

<span data-ttu-id="cd413-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd413-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd413-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cd413-108">Attributes</span></span>

<span data-ttu-id="cd413-109">无。</span><span class="sxs-lookup"><span data-stu-id="cd413-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd413-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cd413-110">Child elements</span></span>

<span data-ttu-id="cd413-111">无。</span><span class="sxs-lookup"><span data-stu-id="cd413-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd413-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cd413-112">Parent elements</span></span>

|<span data-ttu-id="cd413-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cd413-113">**Element**</span></span>|<span data-ttu-id="cd413-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cd413-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd413-115">操作</span><span class="sxs-lookup"><span data-stu-id="cd413-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="cd413-116">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="cd413-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cd413-117">文本值</span><span class="sxs-lookup"><span data-stu-id="cd413-117">Text value</span></span>

<span data-ttu-id="cd413-118">如果文本值为**true** ，则表示必须将邮件标记为永久删除。</span><span class="sxs-lookup"><span data-stu-id="cd413-118">A text value of **true** indicates that the message must be marked to be permanently deleted.</span></span> <span data-ttu-id="cd413-119">**如果值为 false** ，则表示邮件不一定被标记为永久删除。</span><span class="sxs-lookup"><span data-stu-id="cd413-119">A value of **false** indicates that the message must not be marked to be permanently deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cd413-120">说明</span><span class="sxs-lookup"><span data-stu-id="cd413-120">Remarks</span></span>

<span data-ttu-id="cd413-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cd413-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd413-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="cd413-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd413-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="cd413-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd413-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="cd413-124">Schema Name</span></span>  <br/> |<span data-ttu-id="cd413-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="cd413-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cd413-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="cd413-126">Validation File</span></span>  <br/> |<span data-ttu-id="cd413-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cd413-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cd413-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="cd413-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd413-129">True</span><span class="sxs-lookup"><span data-stu-id="cd413-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd413-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cd413-130">See also</span></span>



- [<span data-ttu-id="cd413-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cd413-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

