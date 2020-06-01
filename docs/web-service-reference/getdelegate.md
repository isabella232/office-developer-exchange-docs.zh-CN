---
title: GetDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegate
api_type:
- schema
ms.assetid: 6d5efe59-596f-46f8-bdc6-ca9cded9bb8e
description: GetDelegate 元素定义一个请求，以获取有关邮箱的代理的信息。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: bd7fb55800b51eb2d69184bc4e04cdef3e6b9a89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461028"
---
# <a name="getdelegate"></a><span data-ttu-id="8f7bc-104">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="8f7bc-104">GetDelegate</span></span>

<span data-ttu-id="8f7bc-105">**GetDelegate**元素定义一个请求，以获取有关邮箱的代理的信息。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-105">The **GetDelegate** element defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="8f7bc-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 <span data-ttu-id="8f7bc-107">**GetDelegateType**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-107">**GetDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8f7bc-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8f7bc-108">Attributes and elements</span></span>

<span data-ttu-id="8f7bc-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8f7bc-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="8f7bc-110">Attributes</span></span>

|<span data-ttu-id="8f7bc-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-111">**Attribute**</span></span>|<span data-ttu-id="8f7bc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8f7bc-113">**IncludePermissions**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-113">**IncludePermissions**</span></span> <br/> |<span data-ttu-id="8f7bc-114">指示响应是否包含每个代理用户的权限设置。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-114">Indicates whether the response contains permission settings for each delegate user.</span></span>  <br/> |
   
#### <a name="includepermissions-attribute-values"></a><span data-ttu-id="8f7bc-115">IncludePermissions 属性值</span><span class="sxs-lookup"><span data-stu-id="8f7bc-115">IncludePermissions attribute values</span></span>

|<span data-ttu-id="8f7bc-116">**值**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-116">**Value**</span></span>|<span data-ttu-id="8f7bc-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8f7bc-118">**True**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-118">**True**</span></span> <br/> |<span data-ttu-id="8f7bc-119">除了在[UserId](userid.md)元素中返回的代理用户信息之外，还返回委派用户权限。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-119">Delegate user permissions are returned in addition to the delegate user information that is returned in the [UserId](userid.md) element.</span></span>  <br/> |
|<span data-ttu-id="8f7bc-120">**False**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-120">**False**</span></span> <br/> |<span data-ttu-id="8f7bc-121">将返回[UserId](userid.md)信息。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-121">[UserId](userid.md) information is returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8f7bc-122">子元素</span><span class="sxs-lookup"><span data-stu-id="8f7bc-122">Child elements</span></span>

|<span data-ttu-id="8f7bc-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-123">**Element**</span></span>|<span data-ttu-id="8f7bc-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="8f7bc-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f7bc-125">Mailbox</span><span class="sxs-lookup"><span data-stu-id="8f7bc-125">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="8f7bc-126">标识主体的邮箱。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-126">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="8f7bc-127">UserIds</span><span class="sxs-lookup"><span data-stu-id="8f7bc-127">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="8f7bc-128">包含要从主体邮箱获取的代理用户的数组。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-128">Contains an array of delegate users to get from a principal's mailbox.</span></span> <span data-ttu-id="8f7bc-129">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8f7bc-130">父元素</span><span class="sxs-lookup"><span data-stu-id="8f7bc-130">Parent elements</span></span>

<span data-ttu-id="8f7bc-131">无。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8f7bc-132">说明</span><span class="sxs-lookup"><span data-stu-id="8f7bc-132">Remarks</span></span>

<span data-ttu-id="8f7bc-133">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8f7bc-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f7bc-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="8f7bc-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f7bc-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="8f7bc-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8f7bc-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="8f7bc-136">Schema Name</span></span>  <br/> |<span data-ttu-id="8f7bc-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="8f7bc-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8f7bc-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="8f7bc-138">Validation File</span></span>  <br/> |<span data-ttu-id="8f7bc-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8f7bc-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8f7bc-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="8f7bc-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="8f7bc-141">False</span><span class="sxs-lookup"><span data-stu-id="8f7bc-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8f7bc-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8f7bc-142">See also</span></span>



[<span data-ttu-id="8f7bc-143">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="8f7bc-143">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="8f7bc-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8f7bc-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

