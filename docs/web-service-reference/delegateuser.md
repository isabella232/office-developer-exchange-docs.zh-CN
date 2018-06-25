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
description: DelegateUser 元素标识要添加或更新的邮箱中的单个委托或委托管理响应中返回的代理人。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 72ddc313a5a76cd0345918cad63b7775ff85026b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753780"
---
# <a name="delegateuser"></a><span data-ttu-id="788d4-104">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="788d4-104">DelegateUser</span></span>

<span data-ttu-id="788d4-105">**DelegateUser**元素标识要添加或更新的邮箱中的单个委托或委托管理响应中返回的代理人。</span><span class="sxs-lookup"><span data-stu-id="788d4-105">The **DelegateUser** element identifies a single delegate to add or update in a mailbox or a delegate returned in a delegate management response.</span></span> <span data-ttu-id="788d4-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="788d4-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegateUser>
   <UserId/>
   <DelegatePermissions/>
   <ReceiveCopiesOfMeetingMessages/>
   <ViewPrivateItems/>
</DelegateUser>
```

<span data-ttu-id="788d4-107">**DelegateUserType**</span><span class="sxs-lookup"><span data-stu-id="788d4-107">**DelegateUserType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="788d4-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="788d4-108">Attributes and elements</span></span>

<span data-ttu-id="788d4-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="788d4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="788d4-110">属性</span><span class="sxs-lookup"><span data-stu-id="788d4-110">Attributes</span></span>

<span data-ttu-id="788d4-111">无。</span><span class="sxs-lookup"><span data-stu-id="788d4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="788d4-112">子元素</span><span class="sxs-lookup"><span data-stu-id="788d4-112">Child elements</span></span>

|<span data-ttu-id="788d4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="788d4-113">**Element**</span></span>|<span data-ttu-id="788d4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="788d4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="788d4-115">用户 Id</span><span class="sxs-lookup"><span data-stu-id="788d4-115">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="788d4-116">标识该委托。</span><span class="sxs-lookup"><span data-stu-id="788d4-116">Identifies the delegate.</span></span> <span data-ttu-id="788d4-117">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="788d4-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="788d4-118">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="788d4-118">DelegatePermissions</span></span>](delegatepermissions.md) <br/> |<span data-ttu-id="788d4-119">包含委派权限级别设置。</span><span class="sxs-lookup"><span data-stu-id="788d4-119">Contains the delegate permission level settings.</span></span> <span data-ttu-id="788d4-120">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="788d4-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="788d4-121">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="788d4-121">ReceiveCopiesOfMeetingMessages</span></span>](receivecopiesofmeetingmessages.md) <br/> |<span data-ttu-id="788d4-122">指示是否代理接收发往主体的会议相关邮件的副本。</span><span class="sxs-lookup"><span data-stu-id="788d4-122">Indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="788d4-123">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="788d4-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="788d4-124">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="788d4-124">ViewPrivateItems</span></span>](viewprivateitems.md) <br/> |<span data-ttu-id="788d4-125">指示代理人是否有权查看的主体的邮箱中的个人日历项目。</span><span class="sxs-lookup"><span data-stu-id="788d4-125">Indicates whether a delegate has permission to view private calendar items in the principal's mailbox.</span></span> <span data-ttu-id="788d4-126">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="788d4-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="788d4-127">父元素</span><span class="sxs-lookup"><span data-stu-id="788d4-127">Parent elements</span></span>

|<span data-ttu-id="788d4-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="788d4-128">**Element**</span></span>|<span data-ttu-id="788d4-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="788d4-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="788d4-130">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="788d4-130">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="788d4-131">包含代理人来添加或更新的邮箱中的标识。</span><span class="sxs-lookup"><span data-stu-id="788d4-131">Contains the identities of delegates to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="788d4-132">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="788d4-132">DelegateUserResponseMessageType</span></span>](delegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="788d4-133">包含委派管理操作的响应消息。</span><span class="sxs-lookup"><span data-stu-id="788d4-133">Contains response messages for delegate management operations.</span></span> <span data-ttu-id="788d4-134">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="788d4-134">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="788d4-135">备注</span><span class="sxs-lookup"><span data-stu-id="788d4-135">Remarks</span></span>

<span data-ttu-id="788d4-136">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="788d4-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="788d4-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="788d4-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="788d4-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="788d4-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="788d4-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="788d4-139">Schema Name</span></span>  <br/> |<span data-ttu-id="788d4-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="788d4-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="788d4-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="788d4-141">Validation File</span></span>  <br/> |<span data-ttu-id="788d4-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="788d4-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="788d4-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="788d4-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="788d4-144">False</span><span class="sxs-lookup"><span data-stu-id="788d4-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="788d4-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="788d4-145">See also</span></span>

- [<span data-ttu-id="788d4-146">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="788d4-146">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="788d4-147">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="788d4-147">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="788d4-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="788d4-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="788d4-149">添加代理人</span><span class="sxs-lookup"><span data-stu-id="788d4-149">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

