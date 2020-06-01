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
description: DelegateUsers 元素包含要添加到邮箱或在邮箱中进行更新的代理的标识。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 69f5aab65634f41ec0f820da05dee79a300fb32e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457373"
---
# <a name="delegateusers"></a><span data-ttu-id="faf6b-104">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="faf6b-104">DelegateUsers</span></span>

<span data-ttu-id="faf6b-105">**DelegateUsers**元素包含要添加到邮箱或在邮箱中进行更新的代理的标识。</span><span class="sxs-lookup"><span data-stu-id="faf6b-105">The **DelegateUsers** element contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="faf6b-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="faf6b-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUsers>
   <DelegateUser>
</DelegateUsers>
```

<span data-ttu-id="faf6b-107">**ArrayOfDelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="faf6b-107">**ArrayOfDelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="faf6b-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="faf6b-108">Attributes and elements</span></span>

<span data-ttu-id="faf6b-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="faf6b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="faf6b-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="faf6b-110">Attributes</span></span>

<span data-ttu-id="faf6b-111">无。</span><span class="sxs-lookup"><span data-stu-id="faf6b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="faf6b-112">子元素</span><span class="sxs-lookup"><span data-stu-id="faf6b-112">Child elements</span></span>

|<span data-ttu-id="faf6b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="faf6b-113">**Element**</span></span>|<span data-ttu-id="faf6b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="faf6b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="faf6b-115">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="faf6b-115">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="faf6b-116">标识要在邮箱中添加或更新的单个代理。</span><span class="sxs-lookup"><span data-stu-id="faf6b-116">Identifies a single delegate to add to or update in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="faf6b-117">父元素</span><span class="sxs-lookup"><span data-stu-id="faf6b-117">Parent elements</span></span>

|<span data-ttu-id="faf6b-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="faf6b-118">**Element**</span></span>|<span data-ttu-id="faf6b-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="faf6b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="faf6b-120">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="faf6b-120">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="faf6b-121">定义请求以将代理人添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="faf6b-121">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="faf6b-122">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="faf6b-122">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="faf6b-123">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="faf6b-123">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="faf6b-124">定义请求以更新邮箱中的代理人。</span><span class="sxs-lookup"><span data-stu-id="faf6b-124">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="faf6b-125">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="faf6b-125">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="faf6b-126">说明</span><span class="sxs-lookup"><span data-stu-id="faf6b-126">Remarks</span></span>

<span data-ttu-id="faf6b-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="faf6b-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="faf6b-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="faf6b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="faf6b-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="faf6b-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="faf6b-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="faf6b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="faf6b-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="faf6b-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="faf6b-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="faf6b-132">Validation File</span></span>  <br/> |<span data-ttu-id="faf6b-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="faf6b-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="faf6b-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="faf6b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="faf6b-135">False</span><span class="sxs-lookup"><span data-stu-id="faf6b-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="faf6b-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="faf6b-136">See also</span></span>

- [<span data-ttu-id="faf6b-137">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="faf6b-137">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="faf6b-138">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="faf6b-138">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="faf6b-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="faf6b-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="faf6b-140">添加委派</span><span class="sxs-lookup"><span data-stu-id="faf6b-140">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

