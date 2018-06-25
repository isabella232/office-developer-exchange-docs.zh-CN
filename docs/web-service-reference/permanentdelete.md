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
description: PermanentDelete 元素表示邮件是否被永久删除和不保存到已删除邮件文件夹。
ms.openlocfilehash: 40cf80e054bb70a3f6d687e8d4361f1d4331a7f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826724"
---
# <a name="permanentdelete"></a><span data-ttu-id="33a93-103">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="33a93-103">PermanentDelete</span></span>

<span data-ttu-id="33a93-104">**PermanentDelete**元素表示邮件是否被永久删除和不保存到已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="33a93-104">The **PermanentDelete** element indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span> 
  
```XML
<PermanentDelete>true | false</PermanentDelete>
```

 <span data-ttu-id="33a93-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="33a93-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33a93-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="33a93-106">Attributes and elements</span></span>

<span data-ttu-id="33a93-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="33a93-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33a93-108">属性</span><span class="sxs-lookup"><span data-stu-id="33a93-108">Attributes</span></span>

<span data-ttu-id="33a93-109">无。</span><span class="sxs-lookup"><span data-stu-id="33a93-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="33a93-110">子元素</span><span class="sxs-lookup"><span data-stu-id="33a93-110">Child elements</span></span>

<span data-ttu-id="33a93-111">无。</span><span class="sxs-lookup"><span data-stu-id="33a93-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="33a93-112">父元素</span><span class="sxs-lookup"><span data-stu-id="33a93-112">Parent elements</span></span>

|<span data-ttu-id="33a93-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="33a93-113">**Element**</span></span>|<span data-ttu-id="33a93-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="33a93-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33a93-115">操作</span><span class="sxs-lookup"><span data-stu-id="33a93-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="33a93-116">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="33a93-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="33a93-117">文本值</span><span class="sxs-lookup"><span data-stu-id="33a93-117">Text value</span></span>

<span data-ttu-id="33a93-118">文本值为**true**指示必须标记邮件可被永久删除。</span><span class="sxs-lookup"><span data-stu-id="33a93-118">A text value of **true** indicates that the message must be marked to be permanently deleted.</span></span> <span data-ttu-id="33a93-119">如果值为**false**指示邮件必须不能标记要永久删除。</span><span class="sxs-lookup"><span data-stu-id="33a93-119">A value of **false** indicates that the message must not be marked to be permanently deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="33a93-120">备注</span><span class="sxs-lookup"><span data-stu-id="33a93-120">Remarks</span></span>

<span data-ttu-id="33a93-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="33a93-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33a93-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="33a93-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33a93-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="33a93-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="33a93-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="33a93-124">Schema Name</span></span>  <br/> |<span data-ttu-id="33a93-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="33a93-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="33a93-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="33a93-126">Validation File</span></span>  <br/> |<span data-ttu-id="33a93-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="33a93-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="33a93-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="33a93-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="33a93-129">True</span><span class="sxs-lookup"><span data-stu-id="33a93-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33a93-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="33a93-130">See also</span></span>



- [<span data-ttu-id="33a93-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="33a93-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

