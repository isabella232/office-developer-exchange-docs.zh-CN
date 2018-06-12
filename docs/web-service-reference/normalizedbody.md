---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: NormalizedBody 元素指定的 HTML 表示形式的项目的 Body 属性为可插入到另一个 HTML 正文的片段。
ms.openlocfilehash: 07c2176d2c8a7473c06b7e42f8bcbbe6670581ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826548"
---
# <a name="normalizedbody"></a><span data-ttu-id="d1a58-103">NormalizedBody</span><span class="sxs-lookup"><span data-stu-id="d1a58-103">NormalizedBody</span></span>

<span data-ttu-id="d1a58-104">**NormalizedBody**元素指定的 HTML 表示形式的项目的**Body**属性为可插入到另一个 HTML 正文的片段。</span><span class="sxs-lookup"><span data-stu-id="d1a58-104">The **NormalizedBody** element specifies an HTML representation of the **Body** property of an item as a fragment that can be inserted into another HTML body.</span></span> 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 <span data-ttu-id="d1a58-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="d1a58-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1a58-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d1a58-106">Attributes and elements</span></span>

<span data-ttu-id="d1a58-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d1a58-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1a58-108">属性</span><span class="sxs-lookup"><span data-stu-id="d1a58-108">Attributes</span></span>

|<span data-ttu-id="d1a58-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="d1a58-109">**Attribute**</span></span>|<span data-ttu-id="d1a58-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="d1a58-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1a58-111">BodyType</span><span class="sxs-lookup"><span data-stu-id="d1a58-111">BodyType</span></span>  <br/> |<span data-ttu-id="d1a58-112">指示将正文类型。</span><span class="sxs-lookup"><span data-stu-id="d1a58-112">Indicates the body type.</span></span> <span data-ttu-id="d1a58-113">**BodyType**属性的值的**文本**指示正文采用纯文本形式。</span><span class="sxs-lookup"><span data-stu-id="d1a58-113">The value of **Text** for the **BodyType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="d1a58-114">**BodyType**属性的值的**HTML**指示正文采用 HTML 窗体。</span><span class="sxs-lookup"><span data-stu-id="d1a58-114">The value of **HTML** for the **BodyType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="d1a58-115">**BodyType**属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="d1a58-115">The **BodyType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="d1a58-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="d1a58-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="d1a58-117">指示正文内容已被截断。</span><span class="sxs-lookup"><span data-stu-id="d1a58-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="d1a58-118">文本值为**false**的**IsTruncated**属性指示正文内容不被截断。</span><span class="sxs-lookup"><span data-stu-id="d1a58-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="d1a58-119">如果规范化的正文长度大于[MaximumBodySize](maximumbodysize.md)元素中设置的值，则将截断规范化的正文。</span><span class="sxs-lookup"><span data-stu-id="d1a58-119">The normalized body will be truncated if the normalized body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d1a58-120">子元素</span><span class="sxs-lookup"><span data-stu-id="d1a58-120">Child elements</span></span>

<span data-ttu-id="d1a58-121">无。</span><span class="sxs-lookup"><span data-stu-id="d1a58-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1a58-122">父元素</span><span class="sxs-lookup"><span data-stu-id="d1a58-122">Parent elements</span></span>

<span data-ttu-id="d1a58-123">[项目](item.md) | [消息](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [任务](task.md) | [PostItem](postitem.md)  | [日历项目](calendaritem.md) | [联系人](contact.md) | [DistributionList](distributionlist.md)</span><span class="sxs-lookup"><span data-stu-id="d1a58-123">[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d1a58-124">文本值</span><span class="sxs-lookup"><span data-stu-id="d1a58-124">Text value</span></span>

<span data-ttu-id="d1a58-125">**NormalizedBody**元素的文本值是规范化项目的正文。</span><span class="sxs-lookup"><span data-stu-id="d1a58-125">The text value of the **NormalizedBody** element is the normalized body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d1a58-126">备注</span><span class="sxs-lookup"><span data-stu-id="d1a58-126">Remarks</span></span>

<span data-ttu-id="d1a58-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d1a58-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d1a58-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d1a58-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1a58-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="d1a58-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1a58-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="d1a58-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1a58-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="d1a58-131">Schema name</span></span>  <br/> |<span data-ttu-id="d1a58-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="d1a58-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1a58-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="d1a58-133">Validation file</span></span>  <br/> |<span data-ttu-id="d1a58-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1a58-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1a58-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="d1a58-135">Can be empty</span></span>  <br/> ||
   

