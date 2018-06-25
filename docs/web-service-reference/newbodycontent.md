---
title: NewBodyContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NewBodyContent
api_type:
- schema
ms.assetid: 0303600d-16d8-4685-88f2-980c5ca7e9a6
description: NewBodyContent 元素均表示一条消息的新正文内容。
ms.openlocfilehash: b87393e460b1eee1c13efebf38e898d17915bd71
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826516"
---
# <a name="newbodycontent"></a><span data-ttu-id="cb846-103">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="cb846-103">NewBodyContent</span></span>

<span data-ttu-id="cb846-104">**NewBodyContent**元素均表示一条消息的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="cb846-104">The **NewBodyContent** element represents the new body content of a message.</span></span> 
  
```xml
<NewBodyContent BodyType=""/>
```

 <span data-ttu-id="cb846-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="cb846-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb846-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cb846-106">Attributes and elements</span></span>

<span data-ttu-id="cb846-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cb846-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb846-108">属性</span><span class="sxs-lookup"><span data-stu-id="cb846-108">Attributes</span></span>

|<span data-ttu-id="cb846-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="cb846-109">**Attribute**</span></span>|<span data-ttu-id="cb846-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb846-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb846-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="cb846-111">**BodyType**</span></span> <br/> |<span data-ttu-id="cb846-112">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="cb846-112">Represents the actual body content of a message.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="cb846-113">BodyType 属性</span><span class="sxs-lookup"><span data-stu-id="cb846-113">BodyType Attribute</span></span>

|<span data-ttu-id="cb846-114">**值**</span><span class="sxs-lookup"><span data-stu-id="cb846-114">**Value**</span></span>|<span data-ttu-id="cb846-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb846-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb846-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="cb846-116">**HTML**</span></span> <br/> |<span data-ttu-id="cb846-117">将所有正文都转换为 HTML。</span><span class="sxs-lookup"><span data-stu-id="cb846-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="cb846-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="cb846-118">**Text**</span></span> <br/> |<span data-ttu-id="cb846-119">将所有正文都转换为纯文本。</span><span class="sxs-lookup"><span data-stu-id="cb846-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cb846-120">子元素</span><span class="sxs-lookup"><span data-stu-id="cb846-120">Child elements</span></span>

<span data-ttu-id="cb846-121">无。</span><span class="sxs-lookup"><span data-stu-id="cb846-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb846-122">父元素</span><span class="sxs-lookup"><span data-stu-id="cb846-122">Parent elements</span></span>

|<span data-ttu-id="cb846-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb846-123">**Element**</span></span>|<span data-ttu-id="cb846-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb846-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb846-125">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="cb846-125">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="cb846-126">包含对 Exchange 存储中的项目的发件人的回复。</span><span class="sxs-lookup"><span data-stu-id="cb846-126">Contains a reply to the sender of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cb846-127">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="cb846-127">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="cb846-128">包含对发件人和所有找出的 Exchange 存储中的项目的收件人的答复。</span><span class="sxs-lookup"><span data-stu-id="cb846-128">Contains a reply to the sender and all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cb846-129">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="cb846-129">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="cb846-130">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="cb846-130">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="cb846-131">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="cb846-131">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="cb846-132">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="cb846-132">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="cb846-133">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="cb846-133">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="cb846-134">包含一个公告项目答复。</span><span class="sxs-lookup"><span data-stu-id="cb846-134">Contains a reply to a post item.</span></span> <span data-ttu-id="cb846-135">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cb846-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb846-136">文本值</span><span class="sxs-lookup"><span data-stu-id="cb846-136">Text value</span></span>

<span data-ttu-id="cb846-137">文本值表示一条消息的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="cb846-137">The text value represents the new body content of a message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb846-138">注解</span><span class="sxs-lookup"><span data-stu-id="cb846-138">Remarks</span></span>

<span data-ttu-id="cb846-139">描述此元素的架构位于 Exchange 服务器已安装了客户端访问服务器角色的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cb846-139">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb846-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="cb846-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb846-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="cb846-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cb846-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="cb846-142">Schema Name</span></span>  <br/> |<span data-ttu-id="cb846-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="cb846-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="cb846-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="cb846-144">Validation File</span></span>  <br/> |<span data-ttu-id="cb846-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cb846-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cb846-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="cb846-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb846-147">False</span><span class="sxs-lookup"><span data-stu-id="cb846-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb846-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb846-148">See also</span></span>



- [<span data-ttu-id="cb846-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cb846-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

