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
description: NewBodyContent 元素表示邮件的新正文内容。
ms.openlocfilehash: dcfa927bb284ff00e510d8c7b4b31910a70b3cbb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466855"
---
# <a name="newbodycontent"></a><span data-ttu-id="31fda-103">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="31fda-103">NewBodyContent</span></span>

<span data-ttu-id="31fda-104">**NewBodyContent**元素表示邮件的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="31fda-104">The **NewBodyContent** element represents the new body content of a message.</span></span> 
  
```xml
<NewBodyContent BodyType=""/>
```

 <span data-ttu-id="31fda-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="31fda-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31fda-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="31fda-106">Attributes and elements</span></span>

<span data-ttu-id="31fda-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="31fda-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31fda-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="31fda-108">Attributes</span></span>

|<span data-ttu-id="31fda-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="31fda-109">**Attribute**</span></span>|<span data-ttu-id="31fda-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="31fda-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31fda-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="31fda-111">**BodyType**</span></span> <br/> |<span data-ttu-id="31fda-112">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="31fda-112">Represents the actual body content of a message.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="31fda-113">Office.mailboxenums.bodytype 属性</span><span class="sxs-lookup"><span data-stu-id="31fda-113">BodyType Attribute</span></span>

|<span data-ttu-id="31fda-114">**值**</span><span class="sxs-lookup"><span data-stu-id="31fda-114">**Value**</span></span>|<span data-ttu-id="31fda-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="31fda-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31fda-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="31fda-116">**HTML**</span></span> <br/> |<span data-ttu-id="31fda-117">将所有正文转换为 HTML。</span><span class="sxs-lookup"><span data-stu-id="31fda-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="31fda-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="31fda-118">**Text**</span></span> <br/> |<span data-ttu-id="31fda-119">将所有正文转换为纯文本。</span><span class="sxs-lookup"><span data-stu-id="31fda-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="31fda-120">子元素</span><span class="sxs-lookup"><span data-stu-id="31fda-120">Child elements</span></span>

<span data-ttu-id="31fda-121">无。</span><span class="sxs-lookup"><span data-stu-id="31fda-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31fda-122">父元素</span><span class="sxs-lookup"><span data-stu-id="31fda-122">Parent elements</span></span>

|<span data-ttu-id="31fda-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="31fda-123">**Element**</span></span>|<span data-ttu-id="31fda-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="31fda-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31fda-125">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="31fda-125">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="31fda-126">包含对 Exchange 存储中某个项目的发件人的答复。</span><span class="sxs-lookup"><span data-stu-id="31fda-126">Contains a reply to the sender of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31fda-127">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="31fda-127">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="31fda-128">包含对发件人和 Exchange 存储中某个项目的所有已标识收件人的答复。</span><span class="sxs-lookup"><span data-stu-id="31fda-128">Contains a reply to the sender and all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31fda-129">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="31fda-129">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="31fda-130">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="31fda-130">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="31fda-131">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="31fda-131">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="31fda-132">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="31fda-132">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="31fda-133">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="31fda-133">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="31fda-134">包含对帖子项的答复。</span><span class="sxs-lookup"><span data-stu-id="31fda-134">Contains a reply to a post item.</span></span> <span data-ttu-id="31fda-135">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="31fda-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31fda-136">文本值</span><span class="sxs-lookup"><span data-stu-id="31fda-136">Text value</span></span>

<span data-ttu-id="31fda-137">该文本值表示邮件的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="31fda-137">The text value represents the new body content of a message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31fda-138">备注</span><span class="sxs-lookup"><span data-stu-id="31fda-138">Remarks</span></span>

<span data-ttu-id="31fda-139">描述此元素的架构位于安装了客户端访问服务器角色的 Exchange 服务器的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="31fda-139">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31fda-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="31fda-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31fda-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="31fda-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31fda-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="31fda-142">Schema Name</span></span>  <br/> |<span data-ttu-id="31fda-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="31fda-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="31fda-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="31fda-144">Validation File</span></span>  <br/> |<span data-ttu-id="31fda-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="31fda-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31fda-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="31fda-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="31fda-147">False</span><span class="sxs-lookup"><span data-stu-id="31fda-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31fda-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="31fda-148">See also</span></span>



- [<span data-ttu-id="31fda-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="31fda-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

