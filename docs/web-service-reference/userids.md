---
title: UserIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserIds
api_type:
- schema
ms.assetid: 78a09c3a-1646-4c55-95a2-1109fb11e1c6
description: UserIds 元素包含要从主体邮箱中获取或删除的委派用户的数组。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: de4661226c154ef0d2d5ac55c57405e20c4d2aee
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459775"
---
# <a name="userids"></a><span data-ttu-id="debb7-104">UserIds</span><span class="sxs-lookup"><span data-stu-id="debb7-104">UserIds</span></span>

<span data-ttu-id="debb7-105">**UserIds**元素包含要从主体邮箱中获取或删除的委派用户的数组。</span><span class="sxs-lookup"><span data-stu-id="debb7-105">The **UserIds** element contains an array of delegate users to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="debb7-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="debb7-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 <span data-ttu-id="debb7-107">**ArrayOfUserIdType**</span><span class="sxs-lookup"><span data-stu-id="debb7-107">**ArrayOfUserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="debb7-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="debb7-108">Attributes and elements</span></span>

<span data-ttu-id="debb7-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="debb7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="debb7-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="debb7-110">Attributes</span></span>

<span data-ttu-id="debb7-111">无。</span><span class="sxs-lookup"><span data-stu-id="debb7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="debb7-112">子元素</span><span class="sxs-lookup"><span data-stu-id="debb7-112">Child elements</span></span>

|<span data-ttu-id="debb7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="debb7-113">**Element**</span></span>|<span data-ttu-id="debb7-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="debb7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="debb7-115">UserId</span><span class="sxs-lookup"><span data-stu-id="debb7-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="debb7-116">标识要从主体邮箱中获取或删除的代理。</span><span class="sxs-lookup"><span data-stu-id="debb7-116">Identifies a delegate to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="debb7-117">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="debb7-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="debb7-118">父元素</span><span class="sxs-lookup"><span data-stu-id="debb7-118">Parent elements</span></span>

|<span data-ttu-id="debb7-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="debb7-119">**Element**</span></span>|<span data-ttu-id="debb7-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="debb7-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="debb7-121">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="debb7-121">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="debb7-122">定义请求以获取有关委派给邮箱的信息。</span><span class="sxs-lookup"><span data-stu-id="debb7-122">Defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="debb7-123">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="debb7-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="debb7-124">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="debb7-124">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="debb7-125">定义请求以从邮箱删除代理人。</span><span class="sxs-lookup"><span data-stu-id="debb7-125">Defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="debb7-126">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="debb7-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="debb7-127">说明</span><span class="sxs-lookup"><span data-stu-id="debb7-127">Remarks</span></span>

<span data-ttu-id="debb7-128">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="debb7-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="debb7-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="debb7-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="debb7-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="debb7-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="debb7-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="debb7-131">Schema Name</span></span>  <br/> |<span data-ttu-id="debb7-132">消息架构</span><span class="sxs-lookup"><span data-stu-id="debb7-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="debb7-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="debb7-133">Validation File</span></span>  <br/> |<span data-ttu-id="debb7-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="debb7-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="debb7-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="debb7-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="debb7-136">False</span><span class="sxs-lookup"><span data-stu-id="debb7-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="debb7-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="debb7-137">See also</span></span>



[<span data-ttu-id="debb7-138">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="debb7-138">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="debb7-139">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="debb7-139">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="debb7-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="debb7-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

