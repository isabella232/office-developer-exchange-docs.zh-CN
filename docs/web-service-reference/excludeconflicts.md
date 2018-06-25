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
description: ExcludeConflicts 元素指定是否返回建议与会者之间发生冲突的日历时间的时间。
ms.openlocfilehash: 66b69d57246942e551de2f683949870823e2e4e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754186"
---
# <a name="excludeconflicts"></a><span data-ttu-id="80069-103">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="80069-103">ExcludeConflicts</span></span>

<span data-ttu-id="80069-104">**ExcludeConflicts**元素指定是否返回建议与会者之间发生冲突的日历时间的时间。</span><span class="sxs-lookup"><span data-stu-id="80069-104">The **ExcludeConflicts** element specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span> 
  
[<span data-ttu-id="80069-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="80069-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="80069-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="80069-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
[<span data-ttu-id="80069-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="80069-107">MailboxData</span></span>](mailboxdata.md)
  
[<span data-ttu-id="80069-108">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="80069-108">ExcludeConflicts</span></span>](excludeconflicts.md)
  
```xml
<ExcludeConflicts>true or false</ExcludeConflicts>
```

 <span data-ttu-id="80069-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="80069-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80069-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="80069-110">Attributes and elements</span></span>

<span data-ttu-id="80069-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="80069-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80069-112">属性</span><span class="sxs-lookup"><span data-stu-id="80069-112">Attributes</span></span>

<span data-ttu-id="80069-113">无。</span><span class="sxs-lookup"><span data-stu-id="80069-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80069-114">子元素</span><span class="sxs-lookup"><span data-stu-id="80069-114">Child elements</span></span>

<span data-ttu-id="80069-115">无。</span><span class="sxs-lookup"><span data-stu-id="80069-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="80069-116">父元素</span><span class="sxs-lookup"><span data-stu-id="80069-116">Parent elements</span></span>

|<span data-ttu-id="80069-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="80069-117">**Element**</span></span>|<span data-ttu-id="80069-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="80069-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80069-119">MailboxData</span><span class="sxs-lookup"><span data-stu-id="80069-119">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="80069-120">代表单个邮箱用户和类型的数据的选项，将返回有关邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="80069-120">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="80069-121">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="80069-121">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="80069-122">文本值</span><span class="sxs-lookup"><span data-stu-id="80069-122">Text value</span></span>

<span data-ttu-id="80069-123">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="80069-123">A text value is required.</span></span> <span data-ttu-id="80069-124">可能的值为布尔值**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="80069-124">The possible values are a Boolean **true** or **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80069-125">注解</span><span class="sxs-lookup"><span data-stu-id="80069-125">Remarks</span></span>

<span data-ttu-id="80069-126">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="80069-126">This element is required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80069-127">描述此元素的架构位于运行 MicrosoftExchange Server 2007 的安装了客户端访问服务器角色的计算机的 /EWS/ 目录中。</span><span class="sxs-lookup"><span data-stu-id="80069-127">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="80069-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="80069-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80069-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="80069-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="80069-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="80069-130">Schema Name</span></span>  <br/> |<span data-ttu-id="80069-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="80069-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="80069-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="80069-132">Validation File</span></span>  <br/> |<span data-ttu-id="80069-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="80069-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="80069-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="80069-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="80069-135">False</span><span class="sxs-lookup"><span data-stu-id="80069-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80069-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80069-136">See also</span></span>



[<span data-ttu-id="80069-137">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="80069-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="80069-138">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="80069-138">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)


[<span data-ttu-id="80069-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="80069-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

