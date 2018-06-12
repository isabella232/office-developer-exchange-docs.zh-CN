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
description: GetDelegate 元素定义一个请求以获取有关委派给邮箱的信息。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: e31d6bd4f4387094beb467fcc4dff31ca7ec5d62
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754513"
---
# <a name="getdelegate"></a><span data-ttu-id="f4be9-104">GetDelegate</span><span class="sxs-lookup"><span data-stu-id="f4be9-104">GetDelegate</span></span>

<span data-ttu-id="f4be9-105">**GetDelegate**元素定义一个请求以获取有关委派给邮箱的信息。</span><span class="sxs-lookup"><span data-stu-id="f4be9-105">The **GetDelegate** element defines a request to get information about delegates to a mailbox.</span></span> <span data-ttu-id="f4be9-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f4be9-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<GetDelegate IncludePermissions="">
      <Mailbox/>
   <UserIds/>
</GetDelegate>
```

 <span data-ttu-id="f4be9-107">**GetDelegateType**</span><span class="sxs-lookup"><span data-stu-id="f4be9-107">**GetDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4be9-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f4be9-108">Attributes and elements</span></span>

<span data-ttu-id="f4be9-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f4be9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4be9-110">属性</span><span class="sxs-lookup"><span data-stu-id="f4be9-110">Attributes</span></span>

|<span data-ttu-id="f4be9-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="f4be9-111">**Attribute**</span></span>|<span data-ttu-id="f4be9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4be9-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4be9-113">**IncludePermissions**</span><span class="sxs-lookup"><span data-stu-id="f4be9-113">**IncludePermissions**</span></span> <br/> |<span data-ttu-id="f4be9-114">指示响应是否包含为每个委派用户的权限设置。</span><span class="sxs-lookup"><span data-stu-id="f4be9-114">Indicates whether the response contains permission settings for each delegate user.</span></span>  <br/> |
   
#### <a name="includepermissions-attribute-values"></a><span data-ttu-id="f4be9-115">IncludePermissions 属性值</span><span class="sxs-lookup"><span data-stu-id="f4be9-115">IncludePermissions attribute values</span></span>

|<span data-ttu-id="f4be9-116">**值**</span><span class="sxs-lookup"><span data-stu-id="f4be9-116">**Value**</span></span>|<span data-ttu-id="f4be9-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4be9-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4be9-118">**True**</span><span class="sxs-lookup"><span data-stu-id="f4be9-118">**True**</span></span> <br/> |<span data-ttu-id="f4be9-119">授予的用户权限返回除了[UserId](userid.md)元素中返回的委托用户信息。</span><span class="sxs-lookup"><span data-stu-id="f4be9-119">Delegate user permissions are returned in addition to the delegate user information that is returned in the [UserId](userid.md) element.</span></span>  <br/> |
|<span data-ttu-id="f4be9-120">**False**</span><span class="sxs-lookup"><span data-stu-id="f4be9-120">**False**</span></span> <br/> |<span data-ttu-id="f4be9-121">将返回[用户 Id](userid.md)信息。</span><span class="sxs-lookup"><span data-stu-id="f4be9-121">[UserId](userid.md) information is returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f4be9-122">子元素</span><span class="sxs-lookup"><span data-stu-id="f4be9-122">Child elements</span></span>

|<span data-ttu-id="f4be9-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="f4be9-123">**Element**</span></span>|<span data-ttu-id="f4be9-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4be9-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4be9-125">Mailbox</span><span class="sxs-lookup"><span data-stu-id="f4be9-125">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="f4be9-126">标识的主体的邮箱。</span><span class="sxs-lookup"><span data-stu-id="f4be9-126">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f4be9-127">UserIds</span><span class="sxs-lookup"><span data-stu-id="f4be9-127">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="f4be9-128">包含委派用户获取主体的邮箱的数组。</span><span class="sxs-lookup"><span data-stu-id="f4be9-128">Contains an array of delegate users to get from a principal's mailbox.</span></span> <span data-ttu-id="f4be9-129">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f4be9-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f4be9-130">父元素</span><span class="sxs-lookup"><span data-stu-id="f4be9-130">Parent elements</span></span>

<span data-ttu-id="f4be9-131">无。</span><span class="sxs-lookup"><span data-stu-id="f4be9-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4be9-132">备注</span><span class="sxs-lookup"><span data-stu-id="f4be9-132">Remarks</span></span>

<span data-ttu-id="f4be9-133">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f4be9-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4be9-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="f4be9-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4be9-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="f4be9-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f4be9-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="f4be9-136">Schema Name</span></span>  <br/> |<span data-ttu-id="f4be9-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="f4be9-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f4be9-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="f4be9-138">Validation File</span></span>  <br/> |<span data-ttu-id="f4be9-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f4be9-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f4be9-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="f4be9-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4be9-141">False</span><span class="sxs-lookup"><span data-stu-id="f4be9-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4be9-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f4be9-142">See also</span></span>



[<span data-ttu-id="f4be9-143">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="f4be9-143">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="f4be9-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f4be9-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

