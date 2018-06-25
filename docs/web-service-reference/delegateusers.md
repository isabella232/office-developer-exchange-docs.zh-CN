---
title: DelegateUsers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUsers
api_type:
- schema
ms.assetid: f30f80d9-20c8-41cc-afc7-a5eec1e0c5ea
description: DelegateUsers 元素包含代理人来添加或更新的邮箱中的标识。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: a078707ae6b1676ca5a32ba718add93debd498fe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753778"
---
# <a name="delegateusers"></a><span data-ttu-id="6c902-104">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="6c902-104">DelegateUsers</span></span>

<span data-ttu-id="6c902-105">**DelegateUsers**元素包含代理人来添加或更新的邮箱中的标识。</span><span class="sxs-lookup"><span data-stu-id="6c902-105">The **DelegateUsers** element contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="6c902-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6c902-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUsers>
   <DelegateUser>
</DelegateUsers>
```

<span data-ttu-id="6c902-107">**ArrayOfDelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="6c902-107">**ArrayOfDelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6c902-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6c902-108">Attributes and elements</span></span>

<span data-ttu-id="6c902-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6c902-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c902-110">属性</span><span class="sxs-lookup"><span data-stu-id="6c902-110">Attributes</span></span>

<span data-ttu-id="6c902-111">无。</span><span class="sxs-lookup"><span data-stu-id="6c902-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c902-112">子元素</span><span class="sxs-lookup"><span data-stu-id="6c902-112">Child elements</span></span>

|<span data-ttu-id="6c902-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c902-113">**Element**</span></span>|<span data-ttu-id="6c902-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c902-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c902-115">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="6c902-115">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="6c902-116">标识要添加或更新的邮箱中的单个委托。</span><span class="sxs-lookup"><span data-stu-id="6c902-116">Identifies a single delegate to add to or update in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6c902-117">父元素</span><span class="sxs-lookup"><span data-stu-id="6c902-117">Parent elements</span></span>

|<span data-ttu-id="6c902-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c902-118">**Element**</span></span>|<span data-ttu-id="6c902-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c902-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c902-120">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="6c902-120">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="6c902-121">定义请求以将代理人添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="6c902-121">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="6c902-122">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6c902-122">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="6c902-123">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="6c902-123">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="6c902-124">定义请求以更新邮箱中的代理人。</span><span class="sxs-lookup"><span data-stu-id="6c902-124">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="6c902-125">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6c902-125">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c902-126">备注</span><span class="sxs-lookup"><span data-stu-id="6c902-126">Remarks</span></span>

<span data-ttu-id="6c902-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6c902-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c902-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="6c902-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c902-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="6c902-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6c902-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="6c902-130">Schema Name</span></span>  <br/> |<span data-ttu-id="6c902-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="6c902-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6c902-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="6c902-132">Validation File</span></span>  <br/> |<span data-ttu-id="6c902-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6c902-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6c902-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="6c902-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c902-135">False</span><span class="sxs-lookup"><span data-stu-id="6c902-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c902-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c902-136">See also</span></span>

- [<span data-ttu-id="6c902-137">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="6c902-137">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="6c902-138">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="6c902-138">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="6c902-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6c902-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="6c902-140">添加代理人</span><span class="sxs-lookup"><span data-stu-id="6c902-140">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

