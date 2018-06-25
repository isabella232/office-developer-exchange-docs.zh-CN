---
title: MailboxData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxData
api_type:
- schema
ms.assetid: e9e3f50c-5a7b-49c7-a9ea-117959c08352
description: MailboxData 元素均表示单个邮箱用户和类型的数据的选项，将返回有关邮箱用户。
ms.openlocfilehash: df60294e7d83b1459e5cca7d75c2b6b4bb9d931d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826281"
---
# <a name="mailboxdata"></a><span data-ttu-id="be575-103">MailboxData</span><span class="sxs-lookup"><span data-stu-id="be575-103">MailboxData</span></span>

<span data-ttu-id="be575-104">**MailboxData**元素均表示单个邮箱用户和类型的数据的选项，将返回有关邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="be575-104">The **MailboxData** element represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span> 
  
- [<span data-ttu-id="be575-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="be575-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="be575-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="be575-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="be575-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="be575-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

<span data-ttu-id="be575-108">**MailboxData**</span><span class="sxs-lookup"><span data-stu-id="be575-108">**MailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="be575-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="be575-109">Attributes and elements</span></span>

<span data-ttu-id="be575-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="be575-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be575-111">属性</span><span class="sxs-lookup"><span data-stu-id="be575-111">Attributes</span></span>

<span data-ttu-id="be575-112">无。</span><span class="sxs-lookup"><span data-stu-id="be575-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be575-113">子元素</span><span class="sxs-lookup"><span data-stu-id="be575-113">Child elements</span></span>

|<span data-ttu-id="be575-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="be575-114">**Element**</span></span>|<span data-ttu-id="be575-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="be575-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be575-116">电子邮件 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="be575-116">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="be575-117">表示 GetUserAvailability 查询的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="be575-117">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> |
|[<span data-ttu-id="be575-118">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="be575-118">AttendeeType</span></span>](attendeetype.md) <br/> |<span data-ttu-id="be575-119">表示与会者的[电子邮件 (EmailAddressType)](email-emailaddresstype.md)元素中标识的类型。</span><span class="sxs-lookup"><span data-stu-id="be575-119">Represents the type of attendee identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="be575-120">这是请求中使用的会议建议。</span><span class="sxs-lookup"><span data-stu-id="be575-120">This is used in requests for meeting suggestions.</span></span>  <br/> |
|[<span data-ttu-id="be575-121">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="be575-121">ExcludeConflicts</span></span>](excludeconflicts.md) <br/> |<span data-ttu-id="be575-122">指定是否返回建议与会者之间发生冲突的日历时间的时间。</span><span class="sxs-lookup"><span data-stu-id="be575-122">Specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="be575-123">父元素</span><span class="sxs-lookup"><span data-stu-id="be575-123">Parent elements</span></span>

|<span data-ttu-id="be575-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="be575-124">**Element**</span></span>|<span data-ttu-id="be575-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="be575-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be575-126">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="be575-126">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="be575-127">包含要查询的可用性信息的邮箱列表。</span><span class="sxs-lookup"><span data-stu-id="be575-127">Contains a list of mailboxes to query for availability information.</span></span>  <br/> <span data-ttu-id="be575-128">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="be575-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be575-129">注解</span><span class="sxs-lookup"><span data-stu-id="be575-129">Remarks</span></span>

<span data-ttu-id="be575-130">客户端应用程序可以定义一个许多**MailboxData**元素。</span><span class="sxs-lookup"><span data-stu-id="be575-130">A client application can define one to many **MailboxData** elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="be575-131">描述此元素的架构位于运行 Exchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="be575-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="be575-132">示例</span><span class="sxs-lookup"><span data-stu-id="be575-132">Example</span></span>

```xml
<MailboxDataArray>
  <MailboxData xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
    <Email>
      <Name></Name>
      <Address>someone@ExServer.example.com</Address>
      <RoutingType>SMTP</RoutingType>
    </Email>
    <AttendeeType>Organizer</AttendeeType>
    <ExcludeConflicts>false</ExcludeConflicts>
  </MailboxData>
</MailboxDataArray>
```

## <a name="element-information"></a><span data-ttu-id="be575-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="be575-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be575-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="be575-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="be575-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="be575-135">Schema Name</span></span>  <br/> |<span data-ttu-id="be575-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="be575-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="be575-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="be575-137">Validation File</span></span>  <br/> |<span data-ttu-id="be575-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="be575-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="be575-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="be575-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="be575-140">False</span><span class="sxs-lookup"><span data-stu-id="be575-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be575-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="be575-141">See also</span></span>

- [<span data-ttu-id="be575-142">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="be575-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="be575-143">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="be575-143">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="be575-144">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="be575-144">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

