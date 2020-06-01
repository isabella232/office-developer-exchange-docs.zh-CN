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
description: MailboxData 元素表示单个邮箱用户，以及有关邮箱用户要返回的数据类型的选项。
ms.openlocfilehash: bfcb8c01d40af81097c7d9868006fe9b7b5519d4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467247"
---
# <a name="mailboxdata"></a><span data-ttu-id="ccc1a-103">MailboxData</span><span class="sxs-lookup"><span data-stu-id="ccc1a-103">MailboxData</span></span>

<span data-ttu-id="ccc1a-104">**MailboxData**元素表示单个邮箱用户，以及有关邮箱用户要返回的数据类型的选项。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-104">The **MailboxData** element represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span> 
  
- [<span data-ttu-id="ccc1a-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="ccc1a-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="ccc1a-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="ccc1a-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="ccc1a-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="ccc1a-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

<span data-ttu-id="ccc1a-108">**MailboxData**</span><span class="sxs-lookup"><span data-stu-id="ccc1a-108">**MailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ccc1a-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ccc1a-109">Attributes and elements</span></span>

<span data-ttu-id="ccc1a-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccc1a-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="ccc1a-111">Attributes</span></span>

<span data-ttu-id="ccc1a-112">无。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccc1a-113">子元素</span><span class="sxs-lookup"><span data-stu-id="ccc1a-113">Child elements</span></span>

|<span data-ttu-id="ccc1a-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="ccc1a-114">**Element**</span></span>|<span data-ttu-id="ccc1a-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="ccc1a-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccc1a-116">电子邮件（EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="ccc1a-116">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="ccc1a-117">表示 GetUserAvailability 查询的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-117">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> |
|[<span data-ttu-id="ccc1a-118">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="ccc1a-118">AttendeeType</span></span>](attendeetype.md) <br/> |<span data-ttu-id="ccc1a-119">表示在[Email （EmailAddressType）](email-emailaddresstype.md)元素中标识的与会者的类型。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-119">Represents the type of attendee identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="ccc1a-120">这用于会议建议的请求。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-120">This is used in requests for meeting suggestions.</span></span>  <br/> |
|[<span data-ttu-id="ccc1a-121">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="ccc1a-121">ExcludeConflicts</span></span>](excludeconflicts.md) <br/> |<span data-ttu-id="ccc1a-122">指定是否为日历时间返回在与会者之间发生冲突的建议时间。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-122">Specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ccc1a-123">父元素</span><span class="sxs-lookup"><span data-stu-id="ccc1a-123">Parent elements</span></span>

|<span data-ttu-id="ccc1a-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="ccc1a-124">**Element**</span></span>|<span data-ttu-id="ccc1a-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="ccc1a-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccc1a-126">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="ccc1a-126">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="ccc1a-127">包含要查询可用性信息的邮箱的列表。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-127">Contains a list of mailboxes to query for availability information.</span></span>  <br/> <span data-ttu-id="ccc1a-128">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="ccc1a-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ccc1a-129">备注</span><span class="sxs-lookup"><span data-stu-id="ccc1a-129">Remarks</span></span>

<span data-ttu-id="ccc1a-130">客户端应用程序可以定义一个到多个**MailboxData**元素。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-130">A client application can define one to many **MailboxData** elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ccc1a-131">描述此元素的架构位于运行 Exchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ccc1a-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ccc1a-132">示例</span><span class="sxs-lookup"><span data-stu-id="ccc1a-132">Example</span></span>

```xml
<MailboxDataArray>
  <MailboxData xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="ccc1a-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="ccc1a-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccc1a-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="ccc1a-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ccc1a-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="ccc1a-135">Schema Name</span></span>  <br/> |<span data-ttu-id="ccc1a-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="ccc1a-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="ccc1a-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="ccc1a-137">Validation File</span></span>  <br/> |<span data-ttu-id="ccc1a-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ccc1a-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ccc1a-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="ccc1a-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccc1a-140">False</span><span class="sxs-lookup"><span data-stu-id="ccc1a-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccc1a-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ccc1a-141">See also</span></span>

- [<span data-ttu-id="ccc1a-142">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="ccc1a-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="ccc1a-143">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="ccc1a-143">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="ccc1a-144">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="ccc1a-144">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

