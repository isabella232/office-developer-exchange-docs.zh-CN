---
title: ExcludeConflicts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExcludeConflicts
api_type:
- schema
ms.assetid: ec33ef23-8537-41eb-8d89-7eb906a1fad7
description: ExcludeConflicts 元素指定是否为在与会者之间发生冲突的日历时间返回建议的时间。
ms.openlocfilehash: d20c594ae600abf110681ea678b2d95a23bf7809
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456974"
---
# <a name="excludeconflicts"></a><span data-ttu-id="53f8a-103">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="53f8a-103">ExcludeConflicts</span></span>

<span data-ttu-id="53f8a-104">**ExcludeConflicts**元素指定是否为在与会者之间发生冲突的日历时间返回建议的时间。</span><span class="sxs-lookup"><span data-stu-id="53f8a-104">The **ExcludeConflicts** element specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span> 
  
[<span data-ttu-id="53f8a-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="53f8a-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="53f8a-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="53f8a-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
[<span data-ttu-id="53f8a-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="53f8a-107">MailboxData</span></span>](mailboxdata.md)
  
[<span data-ttu-id="53f8a-108">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="53f8a-108">ExcludeConflicts</span></span>](excludeconflicts.md)
  
```xml
<ExcludeConflicts>true or false</ExcludeConflicts>
```

 <span data-ttu-id="53f8a-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="53f8a-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53f8a-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="53f8a-110">Attributes and elements</span></span>

<span data-ttu-id="53f8a-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="53f8a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53f8a-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="53f8a-112">Attributes</span></span>

<span data-ttu-id="53f8a-113">无。</span><span class="sxs-lookup"><span data-stu-id="53f8a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53f8a-114">子元素</span><span class="sxs-lookup"><span data-stu-id="53f8a-114">Child elements</span></span>

<span data-ttu-id="53f8a-115">无。</span><span class="sxs-lookup"><span data-stu-id="53f8a-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="53f8a-116">父元素</span><span class="sxs-lookup"><span data-stu-id="53f8a-116">Parent elements</span></span>

|<span data-ttu-id="53f8a-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="53f8a-117">**Element**</span></span>|<span data-ttu-id="53f8a-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="53f8a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53f8a-119">MailboxData</span><span class="sxs-lookup"><span data-stu-id="53f8a-119">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="53f8a-120">代表单个邮箱用户以及有关邮箱用户要返回的数据类型的选项。</span><span class="sxs-lookup"><span data-stu-id="53f8a-120">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="53f8a-121">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="53f8a-121">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="53f8a-122">文本值</span><span class="sxs-lookup"><span data-stu-id="53f8a-122">Text value</span></span>

<span data-ttu-id="53f8a-123">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="53f8a-123">A text value is required.</span></span> <span data-ttu-id="53f8a-124">可能的值为布尔值**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="53f8a-124">The possible values are a Boolean **true** or **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53f8a-125">备注</span><span class="sxs-lookup"><span data-stu-id="53f8a-125">Remarks</span></span>

<span data-ttu-id="53f8a-126">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="53f8a-126">This element is required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="53f8a-127">描述此元素的架构位于运行 MicrosoftExchange Server 2007 且安装了客户端访问服务器角色的计算机的/EWS/目录中。</span><span class="sxs-lookup"><span data-stu-id="53f8a-127">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="53f8a-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="53f8a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53f8a-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="53f8a-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="53f8a-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="53f8a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="53f8a-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="53f8a-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="53f8a-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="53f8a-132">Validation File</span></span>  <br/> |<span data-ttu-id="53f8a-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="53f8a-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="53f8a-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="53f8a-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="53f8a-135">False</span><span class="sxs-lookup"><span data-stu-id="53f8a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53f8a-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="53f8a-136">See also</span></span>



[<span data-ttu-id="53f8a-137">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="53f8a-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="53f8a-138">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="53f8a-138">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)


[<span data-ttu-id="53f8a-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="53f8a-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

