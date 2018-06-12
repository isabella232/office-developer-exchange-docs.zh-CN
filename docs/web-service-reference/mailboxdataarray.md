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
description: MailboxDataArray 元素包含要查询的可用性信息的邮箱列表。
ms.openlocfilehash: b76e71ee9127dc2221e0065a27d3c781f8b5786a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826283"
---
# <a name="mailboxdataarray"></a><span data-ttu-id="6ff16-103">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="6ff16-103">MailboxDataArray</span></span>

<span data-ttu-id="6ff16-104">**MailboxDataArray**元素包含要查询的可用性信息的邮箱列表。</span><span class="sxs-lookup"><span data-stu-id="6ff16-104">The **MailboxDataArray** element contains a list of mailboxes to query for availability information.</span></span> 
  
- [<span data-ttu-id="6ff16-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="6ff16-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="6ff16-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="6ff16-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="6ff16-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="6ff16-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxDataArray>
   <MailboxData>...</MailboxData>
</MailboxDataArray>
```

<span data-ttu-id="6ff16-108">**ArrayOfMailboxData**</span><span class="sxs-lookup"><span data-stu-id="6ff16-108">**ArrayOfMailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6ff16-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6ff16-109">Attributes and elements</span></span>

<span data-ttu-id="6ff16-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6ff16-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ff16-111">属性</span><span class="sxs-lookup"><span data-stu-id="6ff16-111">Attributes</span></span>

<span data-ttu-id="6ff16-112">无。</span><span class="sxs-lookup"><span data-stu-id="6ff16-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ff16-113">子元素</span><span class="sxs-lookup"><span data-stu-id="6ff16-113">Child elements</span></span>

|<span data-ttu-id="6ff16-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="6ff16-114">**Element**</span></span>|<span data-ttu-id="6ff16-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="6ff16-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ff16-116">MailboxData</span><span class="sxs-lookup"><span data-stu-id="6ff16-116">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="6ff16-117">代表单个邮箱用户和类型的数据的选项，将返回有关邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="6ff16-117">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6ff16-118">父元素</span><span class="sxs-lookup"><span data-stu-id="6ff16-118">Parent elements</span></span>

|<span data-ttu-id="6ff16-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="6ff16-119">**Element**</span></span>|<span data-ttu-id="6ff16-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="6ff16-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ff16-121">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="6ff16-121">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="6ff16-122">包含用于获取用户的可用性信息的参数。</span><span class="sxs-lookup"><span data-stu-id="6ff16-122">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="6ff16-123">这是根元素。</span><span class="sxs-lookup"><span data-stu-id="6ff16-123">This is a root element.</span></span>  <br/> <span data-ttu-id="6ff16-124">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="6ff16-124">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ff16-125">备注</span><span class="sxs-lookup"><span data-stu-id="6ff16-125">Remarks</span></span>

<span data-ttu-id="6ff16-126">描述此元素的架构位于运行 Microsoft® Exchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6ff16-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ff16-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="6ff16-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ff16-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="6ff16-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6ff16-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="6ff16-129">Schema Name</span></span>  <br/> |<span data-ttu-id="6ff16-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="6ff16-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6ff16-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="6ff16-131">Validation File</span></span>  <br/> |<span data-ttu-id="6ff16-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6ff16-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6ff16-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="6ff16-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ff16-134">False</span><span class="sxs-lookup"><span data-stu-id="6ff16-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ff16-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6ff16-135">See also</span></span>

- [<span data-ttu-id="6ff16-136">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="6ff16-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="6ff16-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="6ff16-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="6ff16-138">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="6ff16-138">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

