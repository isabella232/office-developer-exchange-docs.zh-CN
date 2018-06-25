---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: TextBody 元素指定的文本正文。
ms.openlocfilehash: 78b18b27891d571605d2eeeeffb5c252cc790c11
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838200"
---
# <a name="textbody"></a><span data-ttu-id="799f2-103">TextBody</span><span class="sxs-lookup"><span data-stu-id="799f2-103">TextBody</span></span>

<span data-ttu-id="799f2-104">**TextBody**元素指定的文本正文。</span><span class="sxs-lookup"><span data-stu-id="799f2-104">The **TextBody** element specifies the text body.</span></span> 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 <span data-ttu-id="799f2-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="799f2-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="799f2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="799f2-106">Attributes and elements</span></span>

<span data-ttu-id="799f2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="799f2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="799f2-108">属性</span><span class="sxs-lookup"><span data-stu-id="799f2-108">Attributes</span></span>

|<span data-ttu-id="799f2-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="799f2-109">**Attribute**</span></span>|<span data-ttu-id="799f2-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="799f2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="799f2-111">BodyTypeType</span><span class="sxs-lookup"><span data-stu-id="799f2-111">BodyTypeType</span></span>  <br/> |<span data-ttu-id="799f2-112">指示将正文类型。</span><span class="sxs-lookup"><span data-stu-id="799f2-112">Indicates the body type.</span></span> <span data-ttu-id="799f2-113">**Text** **BodyTypeType**属性的值指示正文采用纯文本形式。</span><span class="sxs-lookup"><span data-stu-id="799f2-113">The value of **Text** for the **BodyTypeType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="799f2-114">**BodyTypeType**属性的值的**HTML**指示正文采用 HTML 窗体。</span><span class="sxs-lookup"><span data-stu-id="799f2-114">The value of **HTML** for the **BodyTypeType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="799f2-115">**BodyTypeType**属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="799f2-115">The **BodyTypeType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="799f2-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="799f2-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="799f2-117">指示正文内容已被截断。</span><span class="sxs-lookup"><span data-stu-id="799f2-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="799f2-118">文本值为**false**的**IsTruncated**属性指示正文内容不被截断。</span><span class="sxs-lookup"><span data-stu-id="799f2-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="799f2-119">如果文本正文长度超过[MaximumBodySize](maximumbodysize.md)元素中设置的值，则将截断规范化的正文。</span><span class="sxs-lookup"><span data-stu-id="799f2-119">The normalized body will be truncated if the text body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="799f2-120">子元素</span><span class="sxs-lookup"><span data-stu-id="799f2-120">Child elements</span></span>

<span data-ttu-id="799f2-121">无。</span><span class="sxs-lookup"><span data-stu-id="799f2-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="799f2-122">父元素</span><span class="sxs-lookup"><span data-stu-id="799f2-122">Parent elements</span></span>

<span data-ttu-id="799f2-123">[项目](item.md) | [联系人](contact.md) | [消息](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [日历项目](calendaritem.md) | [PostItem](postitem.md) | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="799f2-123">[Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="799f2-124">文本值</span><span class="sxs-lookup"><span data-stu-id="799f2-124">Text value</span></span>

<span data-ttu-id="799f2-125">项目的文本正文的**TextBody**元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="799f2-125">The text value of the **TextBody** element is the text body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="799f2-126">备注</span><span class="sxs-lookup"><span data-stu-id="799f2-126">Remarks</span></span>

<span data-ttu-id="799f2-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="799f2-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="799f2-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="799f2-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="799f2-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="799f2-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="799f2-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="799f2-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="799f2-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="799f2-131">Schema name</span></span>  <br/> |<span data-ttu-id="799f2-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="799f2-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="799f2-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="799f2-133">Validation file</span></span>  <br/> |<span data-ttu-id="799f2-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="799f2-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="799f2-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="799f2-135">Can be empty</span></span>  <br/> ||
   

