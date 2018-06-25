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
description: Userid 元素包含一个数组委派用户获取或删除主体的邮箱。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 277ae96fdbc30f1b39ef20553e10ff1de3ff7a8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838472"
---
# <a name="userids"></a><span data-ttu-id="c0448-104">UserIds</span><span class="sxs-lookup"><span data-stu-id="c0448-104">UserIds</span></span>

<span data-ttu-id="c0448-105">**Userid**元素包含一个数组委派用户获取或删除主体的邮箱。</span><span class="sxs-lookup"><span data-stu-id="c0448-105">The **UserIds** element contains an array of delegate users to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="c0448-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c0448-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UserIds>
   <UserId/>
</UserIds>
```

 <span data-ttu-id="c0448-107">**ArrayOfUserIdType**</span><span class="sxs-lookup"><span data-stu-id="c0448-107">**ArrayOfUserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0448-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c0448-108">Attributes and elements</span></span>

<span data-ttu-id="c0448-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c0448-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0448-110">属性</span><span class="sxs-lookup"><span data-stu-id="c0448-110">Attributes</span></span>

<span data-ttu-id="c0448-111">无。</span><span class="sxs-lookup"><span data-stu-id="c0448-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0448-112">子元素</span><span class="sxs-lookup"><span data-stu-id="c0448-112">Child elements</span></span>

|<span data-ttu-id="c0448-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0448-113">**Element**</span></span>|<span data-ttu-id="c0448-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0448-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0448-115">用户 Id</span><span class="sxs-lookup"><span data-stu-id="c0448-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="c0448-116">标识用于获取或删除主体的邮箱的代理人。</span><span class="sxs-lookup"><span data-stu-id="c0448-116">Identifies a delegate to get or remove from a principal's mailbox.</span></span> <span data-ttu-id="c0448-117">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c0448-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0448-118">父元素</span><span class="sxs-lookup"><span data-stu-id="c0448-118">Parent elements</span></span>

|<span data-ttu-id="c0448-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0448-119">**Element**</span></span>|<span data-ttu-id="c0448-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0448-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0448-121">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="c0448-121">GetDelegate</span></span>](getdelegate.md) <br/> |<span data-ttu-id="c0448-122">定义请求以获取有关委派给邮箱的信息。</span><span class="sxs-lookup"><span data-stu-id="c0448-122">Defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="c0448-123">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c0448-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="c0448-124">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="c0448-124">RemoveDelegate</span></span>](removedelegate.md) <br/> |<span data-ttu-id="c0448-125">定义请求以从邮箱删除代理人。</span><span class="sxs-lookup"><span data-stu-id="c0448-125">Defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="c0448-126">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c0448-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0448-127">备注</span><span class="sxs-lookup"><span data-stu-id="c0448-127">Remarks</span></span>

<span data-ttu-id="c0448-128">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c0448-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0448-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="c0448-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0448-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="c0448-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c0448-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="c0448-131">Schema Name</span></span>  <br/> |<span data-ttu-id="c0448-132">消息架构</span><span class="sxs-lookup"><span data-stu-id="c0448-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c0448-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="c0448-133">Validation File</span></span>  <br/> |<span data-ttu-id="c0448-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c0448-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0448-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="c0448-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0448-136">False</span><span class="sxs-lookup"><span data-stu-id="c0448-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0448-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0448-137">See also</span></span>



[<span data-ttu-id="c0448-138">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="c0448-138">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="c0448-139">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="c0448-139">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="c0448-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c0448-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

