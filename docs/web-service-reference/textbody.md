---
title: TextBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bd0c0bce-3e7c-47c7-af7f-5ee5f5ad9820
description: TextBody 元素指定文本正文。
ms.openlocfilehash: c0002785fb990a251267218f7a5f232e521db41a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459481"
---
# <a name="textbody"></a><span data-ttu-id="eb223-103">TextBody</span><span class="sxs-lookup"><span data-stu-id="eb223-103">TextBody</span></span>

<span data-ttu-id="eb223-104">**TextBody**元素指定文本正文。</span><span class="sxs-lookup"><span data-stu-id="eb223-104">The **TextBody** element specifies the text body.</span></span> 
  
```XML
<TextBody BodyTypeType=" HTML | Text" IsTruncated=" true | false"></TextBody>
```

 <span data-ttu-id="eb223-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="eb223-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb223-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eb223-106">Attributes and elements</span></span>

<span data-ttu-id="eb223-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eb223-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb223-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="eb223-108">Attributes</span></span>

|<span data-ttu-id="eb223-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="eb223-109">**Attribute**</span></span>|<span data-ttu-id="eb223-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb223-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb223-111">BodyTypeType</span><span class="sxs-lookup"><span data-stu-id="eb223-111">BodyTypeType</span></span>  <br/> |<span data-ttu-id="eb223-112">指示正文类型。</span><span class="sxs-lookup"><span data-stu-id="eb223-112">Indicates the body type.</span></span> <span data-ttu-id="eb223-113">**BodyTypeType**属性的**文本**值表示正文是纯文本格式。</span><span class="sxs-lookup"><span data-stu-id="eb223-113">The value of **Text** for the **BodyTypeType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="eb223-114">**BodyTypeType**属性的**HTML**值表示正文是 HTML 格式。</span><span class="sxs-lookup"><span data-stu-id="eb223-114">The value of **HTML** for the **BodyTypeType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="eb223-115">**BodyTypeType**属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="eb223-115">The **BodyTypeType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="eb223-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="eb223-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="eb223-117">指示正文内容已被截断。</span><span class="sxs-lookup"><span data-stu-id="eb223-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="eb223-118">**IsTruncated**属性的文本值为**false**表示正文内容尚未被截断。</span><span class="sxs-lookup"><span data-stu-id="eb223-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="eb223-119">如果文本正文长度长于在[MaximumBodySize](maximumbodysize.md)元素中设置的值，则将截断正常化正文。</span><span class="sxs-lookup"><span data-stu-id="eb223-119">The normalized body will be truncated if the text body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eb223-120">子元素</span><span class="sxs-lookup"><span data-stu-id="eb223-120">Child elements</span></span>

<span data-ttu-id="eb223-121">无。</span><span class="sxs-lookup"><span data-stu-id="eb223-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb223-122">父元素</span><span class="sxs-lookup"><span data-stu-id="eb223-122">Parent elements</span></span>

<span data-ttu-id="eb223-123">[项](item.md)  | [联系人](contact.md)  | [邮件](message-ex15websvcsotherref.md)  | [DistributionList](distributionlist.md)  | [CalendarItem](calendaritem.md)  | [PostItem](postitem.md)  | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="eb223-123">[Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="eb223-124">文本值</span><span class="sxs-lookup"><span data-stu-id="eb223-124">Text value</span></span>

<span data-ttu-id="eb223-125">**TextBody**元素的文本值是项目的文本正文。</span><span class="sxs-lookup"><span data-stu-id="eb223-125">The text value of the **TextBody** element is the text body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eb223-126">备注</span><span class="sxs-lookup"><span data-stu-id="eb223-126">Remarks</span></span>

<span data-ttu-id="eb223-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="eb223-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="eb223-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eb223-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb223-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="eb223-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb223-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="eb223-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb223-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="eb223-131">Schema name</span></span>  <br/> |<span data-ttu-id="eb223-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="eb223-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="eb223-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="eb223-133">Validation file</span></span>  <br/> |<span data-ttu-id="eb223-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb223-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb223-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="eb223-135">Can be empty</span></span>  <br/> ||
   

