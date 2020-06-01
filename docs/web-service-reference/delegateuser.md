---
title: DelegateUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegateUser
api_type:
- schema
ms.assetid: aac4e74e-f69b-4c41-a0c9-489610330fbf
description: DelegateUser 元素标识要在代理管理响应中返回的邮箱或委派中添加或更新的单个代理。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 40d9dacbd544436a3edf3213cf078cd33f961a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458801"
---
# <a name="delegateuser"></a><span data-ttu-id="6295d-104">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="6295d-104">DelegateUser</span></span>

<span data-ttu-id="6295d-105">**DelegateUser**元素标识要在代理管理响应中返回的邮箱或委派中添加或更新的单个代理。</span><span class="sxs-lookup"><span data-stu-id="6295d-105">The **DelegateUser** element identifies a single delegate to add or update in a mailbox or a delegate returned in a delegate management response.</span></span> <span data-ttu-id="6295d-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6295d-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUser>
   <UserId/>
   <DelegatePermissions/>
   <ReceiveCopiesOfMeetingMessages/>
   <ViewPrivateItems/>
</DelegateUser>
```

<span data-ttu-id="6295d-107">**DelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="6295d-107">**DelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6295d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6295d-108">Attributes and elements</span></span>

<span data-ttu-id="6295d-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6295d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6295d-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="6295d-110">Attributes</span></span>

<span data-ttu-id="6295d-111">无。</span><span class="sxs-lookup"><span data-stu-id="6295d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6295d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="6295d-112">Child elements</span></span>

|<span data-ttu-id="6295d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6295d-113">**Element**</span></span>|<span data-ttu-id="6295d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6295d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6295d-115">UserId</span><span class="sxs-lookup"><span data-stu-id="6295d-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="6295d-116">标识代理。</span><span class="sxs-lookup"><span data-stu-id="6295d-116">Identifies the delegate.</span></span> <span data-ttu-id="6295d-117">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6295d-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6295d-118">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="6295d-118">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="6295d-119">包含代理权限级别设置。</span><span class="sxs-lookup"><span data-stu-id="6295d-119">Contains the delegate permission level settings.</span></span> <span data-ttu-id="6295d-120">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6295d-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6295d-121">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="6295d-121">ReceiveCopiesOfMeetingMessages</span></span>](receivecopiesofmeetingmessages.md) <br/> |<span data-ttu-id="6295d-122">指示代理是否接收发往主体的与会议相关的邮件的副本。</span><span class="sxs-lookup"><span data-stu-id="6295d-122">Indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="6295d-123">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6295d-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="6295d-124">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="6295d-124">ViewPrivateItems</span></span>](viewprivateitems.md) <br/> |<span data-ttu-id="6295d-125">指示代理是否有权查看主体邮箱中的私人日历项目。</span><span class="sxs-lookup"><span data-stu-id="6295d-125">Indicates whether a delegate has permission to view private calendar items in the principal's mailbox.</span></span> <span data-ttu-id="6295d-126">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6295d-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6295d-127">父元素</span><span class="sxs-lookup"><span data-stu-id="6295d-127">Parent elements</span></span>

|<span data-ttu-id="6295d-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="6295d-128">**Element**</span></span>|<span data-ttu-id="6295d-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="6295d-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6295d-130">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="6295d-130">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="6295d-131">包含要在邮箱中添加或更新的代理的标识。</span><span class="sxs-lookup"><span data-stu-id="6295d-131">Contains the identities of delegates to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6295d-132">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="6295d-132">DelegateUserResponseMessageType</span></span>](delegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="6295d-133">包含用于委派管理操作的响应消息。</span><span class="sxs-lookup"><span data-stu-id="6295d-133">Contains response messages for delegate management operations.</span></span> <span data-ttu-id="6295d-134">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6295d-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6295d-135">说明</span><span class="sxs-lookup"><span data-stu-id="6295d-135">Remarks</span></span>

<span data-ttu-id="6295d-136">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6295d-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6295d-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="6295d-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6295d-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="6295d-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6295d-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="6295d-139">Schema Name</span></span>  <br/> |<span data-ttu-id="6295d-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="6295d-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="6295d-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="6295d-141">Validation File</span></span>  <br/> |<span data-ttu-id="6295d-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6295d-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6295d-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="6295d-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="6295d-144">False</span><span class="sxs-lookup"><span data-stu-id="6295d-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6295d-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6295d-145">See also</span></span>

- [<span data-ttu-id="6295d-146">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="6295d-146">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="6295d-147">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="6295d-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="6295d-148">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6295d-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="6295d-149">添加委派</span><span class="sxs-lookup"><span data-stu-id="6295d-149">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

