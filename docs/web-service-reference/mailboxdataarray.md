---
title: MailboxDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxDataArray
api_type:
- schema
ms.assetid: a14af788-beee-452c-b5d0-37bcb4ef02ff
description: MailboxDataArray 元素包含要查询可用性信息的邮箱的列表。
ms.openlocfilehash: 894bf97a0d633d7eef0434331ccf1580fcba386e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468192"
---
# <a name="mailboxdataarray"></a><span data-ttu-id="9c98b-103">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="9c98b-103">MailboxDataArray</span></span>

<span data-ttu-id="9c98b-104">**MailboxDataArray**元素包含要查询可用性信息的邮箱的列表。</span><span class="sxs-lookup"><span data-stu-id="9c98b-104">The **MailboxDataArray** element contains a list of mailboxes to query for availability information.</span></span> 
  
- [<span data-ttu-id="9c98b-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="9c98b-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="9c98b-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="9c98b-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="9c98b-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="9c98b-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxDataArray>
   <MailboxData>...</MailboxData>
</MailboxDataArray>
```

<span data-ttu-id="9c98b-108">**ArrayOfMailboxData**</span><span class="sxs-lookup"><span data-stu-id="9c98b-108">**ArrayOfMailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9c98b-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9c98b-109">Attributes and elements</span></span>

<span data-ttu-id="9c98b-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9c98b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c98b-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="9c98b-111">Attributes</span></span>

<span data-ttu-id="9c98b-112">无。</span><span class="sxs-lookup"><span data-stu-id="9c98b-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9c98b-113">子元素</span><span class="sxs-lookup"><span data-stu-id="9c98b-113">Child elements</span></span>

|<span data-ttu-id="9c98b-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="9c98b-114">**Element**</span></span>|<span data-ttu-id="9c98b-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="9c98b-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c98b-116">MailboxData</span><span class="sxs-lookup"><span data-stu-id="9c98b-116">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="9c98b-117">代表单个邮箱用户以及有关邮箱用户要返回的数据类型的选项。</span><span class="sxs-lookup"><span data-stu-id="9c98b-117">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9c98b-118">父元素</span><span class="sxs-lookup"><span data-stu-id="9c98b-118">Parent elements</span></span>

|<span data-ttu-id="9c98b-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="9c98b-119">**Element**</span></span>|<span data-ttu-id="9c98b-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="9c98b-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c98b-121">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="9c98b-121">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="9c98b-122">包含用于获取用户可用性信息的参数。</span><span class="sxs-lookup"><span data-stu-id="9c98b-122">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="9c98b-123">这是一个根元素。</span><span class="sxs-lookup"><span data-stu-id="9c98b-123">This is a root element.</span></span>  <br/> <span data-ttu-id="9c98b-124">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="9c98b-124">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c98b-125">备注</span><span class="sxs-lookup"><span data-stu-id="9c98b-125">Remarks</span></span>

<span data-ttu-id="9c98b-126">描述此元素的架构位于运行 Microsoft® Exchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9c98b-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c98b-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="9c98b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c98b-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="9c98b-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9c98b-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="9c98b-129">Schema Name</span></span>  <br/> |<span data-ttu-id="9c98b-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="9c98b-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9c98b-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="9c98b-131">Validation File</span></span>  <br/> |<span data-ttu-id="9c98b-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9c98b-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9c98b-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="9c98b-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="9c98b-134">False</span><span class="sxs-lookup"><span data-stu-id="9c98b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c98b-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9c98b-135">See also</span></span>

- [<span data-ttu-id="9c98b-136">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="9c98b-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="9c98b-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="9c98b-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="9c98b-138">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="9c98b-138">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

