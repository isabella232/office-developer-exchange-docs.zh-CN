---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: NormalizedBody 元素将项的 Body 属性的 HTML 表示形式指定为可以插入到另一个 HTML 正文中的片段。
ms.openlocfilehash: fb249794bccfeed198e7a3230ab53c66893dcf96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462666"
---
# <a name="normalizedbody"></a><span data-ttu-id="5ee21-103">NormalizedBody</span><span class="sxs-lookup"><span data-stu-id="5ee21-103">NormalizedBody</span></span>

<span data-ttu-id="5ee21-104">**NormalizedBody**元素将项的**BODY**属性的 HTML 表示形式指定为可以插入到另一个 HTML 正文中的片段。</span><span class="sxs-lookup"><span data-stu-id="5ee21-104">The **NormalizedBody** element specifies an HTML representation of the **Body** property of an item as a fragment that can be inserted into another HTML body.</span></span> 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 <span data-ttu-id="5ee21-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="5ee21-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5ee21-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5ee21-106">Attributes and elements</span></span>

<span data-ttu-id="5ee21-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5ee21-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ee21-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5ee21-108">Attributes</span></span>

|<span data-ttu-id="5ee21-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="5ee21-109">**Attribute**</span></span>|<span data-ttu-id="5ee21-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="5ee21-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ee21-111">BodyType</span><span class="sxs-lookup"><span data-stu-id="5ee21-111">BodyType</span></span>  <br/> |<span data-ttu-id="5ee21-112">指示正文类型。</span><span class="sxs-lookup"><span data-stu-id="5ee21-112">Indicates the body type.</span></span> <span data-ttu-id="5ee21-113">**Office.mailboxenums.bodytype**属性的**文本**值表示正文是纯文本格式。</span><span class="sxs-lookup"><span data-stu-id="5ee21-113">The value of **Text** for the **BodyType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="5ee21-114">**Office.mailboxenums.bodytype**属性的**HTML**值表示正文是 HTML 格式。</span><span class="sxs-lookup"><span data-stu-id="5ee21-114">The value of **HTML** for the **BodyType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="5ee21-115">**Office.mailboxenums.bodytype**属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="5ee21-115">The **BodyType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="5ee21-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="5ee21-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="5ee21-117">指示正文内容已被截断。</span><span class="sxs-lookup"><span data-stu-id="5ee21-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="5ee21-118">**IsTruncated**属性的文本值为**false**表示正文内容尚未被截断。</span><span class="sxs-lookup"><span data-stu-id="5ee21-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="5ee21-119">如果正常化的正文长度长于[MaximumBodySize](maximumbodysize.md)元素中设置的值，则将截断正常化的正文。</span><span class="sxs-lookup"><span data-stu-id="5ee21-119">The normalized body will be truncated if the normalized body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5ee21-120">子元素</span><span class="sxs-lookup"><span data-stu-id="5ee21-120">Child elements</span></span>

<span data-ttu-id="5ee21-121">无。</span><span class="sxs-lookup"><span data-stu-id="5ee21-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5ee21-122">父元素</span><span class="sxs-lookup"><span data-stu-id="5ee21-122">Parent elements</span></span>

<span data-ttu-id="5ee21-123">[项](item.md)  | [邮件](message-ex15websvcsotherref.md)  | [MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [MeetingCancellation](meetingcancellation.md)  | [任务](task.md)  | [PostItem](postitem.md)  | [CalendarItem](calendaritem.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)</span><span class="sxs-lookup"><span data-stu-id="5ee21-123">[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5ee21-124">文本值</span><span class="sxs-lookup"><span data-stu-id="5ee21-124">Text value</span></span>

<span data-ttu-id="5ee21-125">**NormalizedBody**元素的文本值是项目的规范化正文。</span><span class="sxs-lookup"><span data-stu-id="5ee21-125">The text value of the **NormalizedBody** element is the normalized body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5ee21-126">备注</span><span class="sxs-lookup"><span data-stu-id="5ee21-126">Remarks</span></span>

<span data-ttu-id="5ee21-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5ee21-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5ee21-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5ee21-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ee21-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="5ee21-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ee21-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="5ee21-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5ee21-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="5ee21-131">Schema name</span></span>  <br/> |<span data-ttu-id="5ee21-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="5ee21-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="5ee21-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="5ee21-133">Validation file</span></span>  <br/> |<span data-ttu-id="5ee21-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5ee21-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5ee21-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="5ee21-135">Can be empty</span></span>  <br/> ||
   

